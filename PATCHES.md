# Local patches

This tree is based on st 0.9.3 and currently carries these patches.

## Alpha

The alpha patch adds ARGB window rendering and configurable background opacity.
Its source patch is stored as `patches/st-alpha-20240814-a0274bc.diff`.

## HarfBuzz ligatures

The upstream `st-ligatures-20251007-0.9.3.diff` patch shapes terminal line
segments with HarfBuzz while preserving st's fixed cell layout. A copy of the
upstream patch is stored under `patches/`.

Source: https://st.suckless.org/patches/ligatures/

## Emoji shaping

The ligatures patch is extended locally for emoji:

- Noto Color Emoji is loaded at the active terminal font size.
- Emoji runs are shaped with Noto instead of the primary monospace font.
- Skin-tone modifiers are retained in a wide emoji's dummy cell rather than
  consuming two extra terminal columns.
- Zero-width joiners and variation selectors are retained for shaping when a
  wide emoji provides a dummy cell.

Building requires HarfBuzz development headers in addition to st's normal
dependencies.
