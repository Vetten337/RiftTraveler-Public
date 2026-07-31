# Temporal Discoveries

The Discovery system gives experimentation a purpose beyond hiding recipes.
It records the difference between an observation, an active research lead, and
a process the player has personally proven.

## Research leads

Leads are triggered by meaningful gameplay events. For example, fully charging
a fired Crystal Growth Mold suggests a crystal-growth experiment, while
obtaining a Temporal Gear can inspire research into removing its unusual
coating.

Leads provide direction without listing every exact requirement. They are
intended to narrow the experiment space while preserving discovery.

## Confirmed protocols

When the player successfully completes a catalogued process, the server marks
that protocol as confirmed. The complete ingredients, outputs, and operating
conditions then appear in the Temporal Discoveries Handbook section.

Discoveries are persistent and maintained per player.

## Commands

Player review:

```text
/rt discoveries
```

Server operators also have developer commands for granting, revoking, and
resetting discoveries and leads. Run `/rtdev help` for the current privileged
command list.

## Recipe versus discovery content

A recipe defines mechanical processing. A Discovery Catalog entry connects
that recipe to lead triggers, clues, completion, localization, and Handbook
presentation.

Snapshot-generated recipes are functional after restart, but do not
automatically gain research leads or Handbook discovery text.

