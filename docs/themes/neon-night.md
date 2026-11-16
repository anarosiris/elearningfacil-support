# Neon Night — Theme for Moodle™ (Boost Union child theme)

**Quick guide (PDF):** [English](QuickGuide_theme_efneonnight_en.pdf) · [Español](GuiaRapida_theme_efneonnight.pdf)

A true dark theme: all of Moodle in black with a teal glow.

Neon Night is a **child theme of Boost Union**. Every Boost Union setting and
feature keeps working (additional block regions, smart menus, flavours, login
and footer settings, custom fonts, raw SCSS, SCSS snippets...). This theme only
replaces the look.

## Requirements

- Moodle 5.2 or 5.3 (5.3 verified manually with Boost Union v5.2-r13).
- [Boost Union](https://moodle.org/plugins/theme_boost_union) for your Moodle
  version (installed; it does not need to be the active theme).
- Colour modes (experimental in Moodle 5.3): the theme has a single palette and
  keeps its own colours whatever colour mode the site or the user chooses.

## Installation

1. Site administration → Plugins → Install plugins → upload the zip (or unzip
   it into `public/theme/efneonnight`), then run the upgrade.
2. Site administration → Appearance → Themes → select **Neon Night**.
3. Configure everything else in Site administration → Appearance → Boost Union,
   as usual. Leave Boost Union's *Brand colour* setting empty.

The theme uses the system font stack: there are no fonts to upload.

## User guide

The full user guide, with screenshots, is in `docs/manual/` as a PDF:
`Guide_theme_efneonnight_en.pdf` (English) and `Guia_theme_efneonnight.pdf` (Spanish).

## Customising

Colours and the other design tokens are the variables at the top of
`scss/preset.scss` (its INSTRUCTIONS block explains them). The variables marked
`!default` can also be overridden for one category or cohort only with a Boost
Union flavour (Boost Union → Flavours → *Raw initial SCSS*).

## Privacy

The theme stores no personal data and makes no external requests: fonts and images are served from your own site. It implements Moodle's Privacy API with a null provider.

## Support and issues

Bug reports and feature requests: https://github.com/anarosiris/moodle-theme_efneonnight/issues (public issue tracker). Source code and documentation: https://github.com/anarosiris/moodle-theme_efneonnight.

## Licence

The code is licensed under the GNU GPL v3 or later (see `LICENSE`).

