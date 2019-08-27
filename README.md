# web-theme-bootstrap

[![Build Status](https://travis-ci.org/Mojang/web-theme-bootstrap.svg?branch=master)](https://travis-ci.org/Mojang/web-theme-bootstrap)

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
