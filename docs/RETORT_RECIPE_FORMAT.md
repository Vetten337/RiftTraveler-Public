# Temporal Retort Recipe Format

Temporal Retort recipes are JSON assets loaded from every installed mod domain:

```text
assets/<domain>/recipes/temporalretort/<recipe>.json
```

One file contains one recipe object. Third-party recipes use the normal Rift
Traveler loader, validator, registry, matcher, execution checker, and atomic
executor.

## Schema

```json
{
  "code": "example-reaction",
  "enabled": true,
  "requiresMods": ["examplemod"],
  "ingredients": [
    {
      "type": "item",
      "code": "game:clearquartz",
      "quantity": 4,
      "attributes": {},
      "allowMixedVariants": false
    }
  ],
  "liquid": null,
  "conditions": {
    "minimumTemperature": 200.0,
    "maximumTemperature": null,
    "durationSeconds": 30.0,
    "lid": "clamped"
  },
  "outputs": [
    {
      "type": "item",
      "code": "examplemod:result",
      "quantity": 1
    }
  ],
  "behavior": {
    "progressMode": "pause"
  }
}
```

## Root fields

- `code`: required path-only recipe code
- `enabled`: optional, defaults to `true`
- `requiresMods`: optional list of mod identifiers that must all be enabled;
  recipes with unmet requirements are skipped before registration
- `ingredients`: zero to three item or block requirements
- `liquid`: one optional liquid requirement; `null` requires an empty tank
- `conditions`: temperature, time, and lid requirements
- `outputs`: one or two solid outputs
- `behavior`: progress handling when execution becomes blocked

## Ingredients

- `type`: `item` or `block`
- `code`: exact or wildcard collectible code
- `quantity`: positive integer
- `attributes`: optional exact integer ItemStack attributes
- `allowMixedVariants`: allows multiple matching collectible variants to
  contribute to the required quantity

Matching is independent of input-slot order. Ingredient assignment is complete
and one-to-one, so one physical quantity cannot satisfy two requirements.

Current attribute support is intentionally narrow. The production use case is:

```json
"attributes": {
  "temporalDust": 8
}
```

on `rifttraveler:crystalgrowthmold-fired`.

## Liquid

```json
"liquid": {
  "code": "game:waterportion",
  "litres": 10.0,
  "consume": true
}
```

The Retort must contain the exact liquid code and at least the declared litres.
When `consume` is `false`, the liquid is required as a reaction medium but is
not removed on successful completion.

## Conditions

- `minimumTemperature`: finite non-negative Celsius value
- `maximumTemperature`: optional upper bound
- `durationSeconds`: finite positive processing time
- `lid`: `open`, `closed`, `clamped`, or `any`

## Outputs

Outputs support `item` or `block`, an exact collectible code, and a positive
quantity. Output ItemStack attributes are not part of Version 1.

Every output must fit before the executor consumes anything.

## Progress behavior

- `pause`: preserve accumulated progress while execution is blocked
- `reset`: return progress to zero when execution is blocked

Progress is bound to the active recipe code and cannot carry into another
protocol.

## Validation and duplicate handling

Malformed JSON is skipped independently. Structurally invalid definitions are
excluded by the production validator. Registry order is deterministic, and the
first definition of a recipe identifier wins; later duplicates are rejected.

Every enabled registered recipe automatically receives a generic Temporal
Discovery entry when no authored discovery definition references it. A custom
catalog entry may replace the generated lead with tailored lore and triggers.

