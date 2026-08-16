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

Every enabled registered Temporal Retort recipe participates automatically. If
a recipe has no authored Discovery Catalog entry, Rift Traveler creates a
generic lead at startup. Possessing any of that recipe's solid ingredients
unlocks the lead.

## Confirmed protocols

When the player successfully completes a catalogued process, the server marks
that protocol as confirmed. The complete ingredients, outputs, and operating
conditions then appear in the Temporal Discoveries Handbook section.

The overview gives each visible discovery its own page. Confirmed protocol pages
serve as a Retort recipe viewer with quantities, liquids, outputs, temperatures,
duration, lid state, and processing behavior. Exact collectibles link directly
to their standard Handbook pages; wildcard requirements link to a search for the
valid family.

New leads use a gold on-screen notification and confirmed protocols use a cyan
notification. Both retain the existing chat record and play a subtle sound once.
Login synchronization is silent, so previously learned discoveries do not replay.

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

A recipe defines mechanical processing. The Discovery Catalog connects that
recipe to lead triggers, clues, completion, localization, and Handbook
presentation.

Snapshot-generated and manually added Retort recipes automatically receive a
generic research lead and Handbook entry after restart. Authors may still add
an explicit Discovery Catalog definition to replace the generated lead with
custom lore or a specialized trigger. Authored entries always take priority.

