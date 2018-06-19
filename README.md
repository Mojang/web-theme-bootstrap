# web-theme-bootstrap

Contains the theme used on minecraft.net based on Boostrap 4

## Install

```cli
> npm i @mojang/web-theme-bootstrap --save
```

## Included in the package

This package includes two parts:

### 1. SCSS files needed to generate your minecraft.net look and feel.

These file scan be found under the scss folder. In your main scss file, include the following to get started:

```scss
$freyja-asset-path: "../theme/freyja";
$master-head-height-lg: 112px;
$master-head-height-md: 87px;
$global-menu-height: 27px;

@import "~@mojang/yggdrasil-web-freyja/scss/styles";
```

Note that the theme takes care of including bootstrap the way it needs to be included so you do not need to include it.

### 2. Generic image assets used in several places, including an icon-set

In order to use the image assets and svg icons included in this package you need to have a build step in your build that copies the image assets to your public folder.

The svg icons also needs to be converted into an [svg-sprite](https://css-tricks.com/svg-sprites-use-better-icon-fonts/) using [svgstore](https://github.com/svgstore/svgstore) or similar tool.
