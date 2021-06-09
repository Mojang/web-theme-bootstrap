# web-theme-bootstrap

[![Build Status](https://travis-ci.org/Mojang/web-theme-bootstrap.svg?branch=main)](https://travis-ci.org/Mojang/web-theme-bootstrap)

Contains the theme used on minecraft.net based on Bootstrap 4

## Install

```cli
> npm i @mojang/web-theme-bootstrap --save
```

## Included in the package

This package includes two parts:

### 1. SCSS files needed to generate your minecraft.net look and feel.

These files can be found under the scss folder. In your main scss file, include the following to get started:

```scss
$freyja-asset-path: "[path_to_public_folder]";
$master-head-height-lg: 112px;
$master-head-height-md: 87px;
$global-menu-height: 27px;

@import "~@mojang/web-theme-bootstrap/scss/styles";
```

Note that the theme takes care of including bootstrap the way it needs to be included so you do not need to @import it yourself.

### 2. Generic image assets used in several places, including an icon-set

In order to use the image assets and svg icons included in this package you need to have a build step in your build that copies the image assets to your public folder.

The svg icons also needs to be converted into a [svg-sprite](https://css-tricks.com/svg-sprites-use-better-icon-fonts/) using [svgstore](https://github.com/svgstore/svgstore) or similar tool.

### Changelog

v6.4.0
- Added Minecraft Core Brand Logo
  
v6.3.1
- Fixes README Changelog

v6.3.0
- New primary color (buttons & links are based out of primary). New secondary and tertiary colors. Loader now uses tertiary colors on dark backgrounds. 

v6.2.10
  - Add Minecraft Java Edition Logo

v6.2.9
  - Remove use of `bg-variant` and `text-emphasis-variant` mixins, that are deprecated in bootstrap@4.4.0

v6.2.8
- High contrast fix for button

v6.2.7
- Add box-shadow for disabled button
- High contrast fix for nav bar

v6.2.6
- Rerelease due to publish issue of 6.2.5

v6.2.5
- Add highlight color on focus for link button

v6.2.4
- Add style for radio and link button on high contrast mode
- Add noto sans font assets

v6.2.3
- Fix duplicate id in svg and add button high contrast style

v6.2.2
- Fix radio buttons in high contrast mode

v6.2.1
- Add radio button high contrast style

v6.2.0
- Add Minecraft Dungeons Launcher icons

v6.1.0
- Add `.icon-cero-a`

v6.0.0
**BREAKING CHANGE**
- Rename following classes:
    * `mojang-footer` -> `mojang-studios-footer`
    * `icon-microsoft-studios` -> `icon-xbox-game-studios`
    * `icon-mojang` -> `icon-mojang-studios`

v5.1.0
- Add cero-a logo

v5.0.0

**BREAKING CHANGE**

- Replace logo svgs:
    * `mojang` with `mojang-studios-horizontal`
    * `mono-mojang` with `mono-mojang-studios-horizontal`


v4.5.0

- Add xbox game studios color logo

v4.4.0

- Add `font-mc-seven`

v4.3.1

- Fix cart icon size

v4.3.0

- Add pixelated cart icon

v4.2.0

- Add Windows logo
- Add new Minecraft Dungeons color

v4.1.0

- Add Minecraft Dungeons logo back

v4.0.0

- Remove Minecraft Dungeons logo

v3.3.1

- Namespace Minecraft Dungeons logo ids

v3.3.0

- Add Minecraft Dungeons logo

v3.2.0

- Darken link color 5%
- Add support for disabled radio button
- Add new checkbox

v3.1.1

- Set link color to primary (was `$primary-supportive`)

v3.1.0

- Update inverted link hover color
- Update `dropdown-menu` style
- Add Xbox Game Studios logo

v3.0.0

- Update primary and tertiary color
- **BREAKING CHANGE**: Remove `$primary-light-1`, `$primary-light-2`, `$primary-dark-1`, `$primary-dark-2`. Use `$primary-supportive` for dark and `$tertiary` for light.

v2.0.0

- Fix position of inline icons
- Add 4 new monochrome SVG logos
- Add a `.svg-logo` class that makes you able to control color through css
- **BREAKING CHANGE**: `#microsoft` and `#mojang` logos now inherit their text color from `currentColor`. Use `.svg-logo` class and set text color to override.
