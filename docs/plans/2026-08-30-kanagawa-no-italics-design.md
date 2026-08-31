# Kanagawa No-Italics Variant Design

## Goal

Add a non-italic version of the `Kanagawa` theme variant, matching the existing non-italic Wave, Dragon, and Lotus variants.

## Design

Extend `themes/Kanagawa-no-italics.json` with a `Kanagawa - No Italics` theme entry. The entry will copy the existing `Kanagawa` theme exactly for colors, UI settings, syntax colors, and font weights. Every syntax declaration that uses an italic `font_style` will instead use `null`.

The new entry will follow the same variant ordering as `themes/Kanagawa.json`, immediately after `Kanagawa Wave - No Italics` and before `Kanagawa Dragon - No Italics`.

No changes are needed to the original `Kanagawa` theme, previews, README, or extension metadata.

## Validation

- Parse `themes/Kanagawa-no-italics.json` as JSON.
- Confirm the four expected no-italics variants are present.
- Compare the new entry with `Kanagawa` and verify that only the theme name and italic `font_style` declarations differ.
- Confirm no syntax declaration in the new entry has `font_style: "italic"`.
