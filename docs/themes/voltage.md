# Voltage — Moodle™ theme (Boost Union child)

Yellow and black, thick borders, hard shadows. It doesn't look like Moodle.

Voltage is a **child theme of Boost Union**. Every Boost Union setting and
feature keeps working (additional block regions, smart menus, flavours, login
and footer settings, custom fonts, raw SCSS, SCSS snippets...). This theme only
replaces the look.

## Requirements

- Moodle 5.2 or 5.3.
- [Boost Union](https://moodle.org/plugins/theme_boost_union) for your Moodle
  version (installed; it does not need to be the active theme).

## Installation

1. Site administration → Plugins → Install plugins → upload the zip (or unzip
   it into `public/theme/efvoltage`), then run the upgrade.
2. Site administration → Appearance → Themes → select **Voltage**.
3. Configure everything else in Site administration → Appearance → Boost Union,
   as usual. Leave Boost Union's *brandcolor* empty.

The fonts (Space Grotesk) are bundled with the theme (SIL Open Font License 1.1, see `fonts/` and `thirdpartylibs.xml`): there is nothing to upload.

## Customising

Colours and the other design tokens are the variables at the top of
`scss/preset.scss` (its INSTRUCTIONS block explains them). The variables marked
`!default` can also be overridden for one category or cohort only with a Boost
Union flavour (Boost Union → Flavours → *Raw initial SCSS*).

## Support and issues

Bug reports and feature requests: https://github.com/anarosiris/elearningfacil-support (public issue tracker). Customer support by email, updates and the number of sites covered are described in `COMMERCIAL-LICENCE.txt`. Developed and maintained by eLearning Fácil (https://elearningfacil.com).

## Licence

The code is licensed under the GNU GPL v3 or later (see `LICENSE`). The fonts use the SIL Open Font License 1.1 (see `fonts/` and `thirdpartylibs.xml`). See `COMMERCIAL-LICENCE.txt` for what the purchase includes (updates and support).
