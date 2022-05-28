# @fireflysemantics/sass-logger

Utility functions for logging with SASS.

## Installation

`npm i @fireflysemantics/sass-logger`

## Usage

This demo will create a Angular Material Palette `$theme-primary` 
and log the contents by first using the `logger` to structure
the map data containing the result and then outputting that 
result with `@debug`.

```
@use '@angular/material' as mat;
@use '@fireflysemantics/sass-logger' as logger;

// ============================================
// Palettes: https://material.io/design/color/
// ============================================
$theme-primary: mat.define-palette(mat.$indigo-palette);
$result: logger.pretty-map($theme-primary);
@debug ($result);

$theme: mat.define-light-theme($theme-primary, $theme-primary, $theme-primary);
//$result: logger.pretty-map($theme);
```

## Output

The above usage demo will output the following:

```
         50: #e8eaf6,  
         100: #c5cae9,  
         200: #9fa8da,  
         300: #7986cb,  
         400: #5c6bc0,  
         500: #3f51b5,  
         600: #3949ab,  
         700: #303f9f,  
         800: #283593,  
         900: #1a237e,  
         A100: #8c9eff,  
         A200: #536dfe,  
         A400: #3d5afe,  
         A700: #304ffe,  
 contrast: (  
         50: rgba(0, 0, 0, 0.87),  
         100: rgba(0, 0, 0, 0.87),  
         200: rgba(0, 0, 0, 0.87),  
         300: white,  
         400: white,  
         500: white,  
         600: white,  
         700: white,  
         800: white,  
         900: white,  
         A100: rgba(0, 0, 0, 0.87),  
         A200: white,  
         A400: white,  
         A700: white,  
 ),  
         default: #3f51b5,  
         lighter: #c5cae9,  
         darker: #303f9f,  
         text: #3f51b5,  
         default-contrast: white,  
         lighter-contrast: rgba(0, 0, 0, 0.87),  
         darker-contrast: white,  
         50-contrast: rgba(0, 0, 0, 0.87),  
         100-contrast: rgba(0, 0, 0, 0.87),  
         200-contrast: rgba(0, 0, 0, 0.87),  
         300-contrast: white,  
         400-contrast: white,  
         500-contrast: white,  
         600-contrast: white,  
         700-contrast: white,  
         800-contrast: white,  
         900-contrast: white,  
         A100-contrast: rgba(0, 0, 0, 0.87),  
         A200-contrast: white,  
         A400-contrast: white,  
         A700-contrast: white,  
         contrast-contrast: , 
```

## Stackblitz

[Stackblitz Demo](https://stackblitz.com/edit/angular-r9tzuk-ov8kx4?file=src%2Fstyles.scss)

