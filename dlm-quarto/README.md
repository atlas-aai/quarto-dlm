# DLM-Quarto Quarto Extension

This extension creates a template for R/Python users to create revealjs/html slides that follow the guidelines of the DLM template from PowerPoint.

Before adding the following extension, you will need to download Quarto. To use this extension, you will need Quarto 1.2.0 or later.

## Installation

```bash
quarto add atlas-aai/dlm-quarto
```

The code above can be added to your terminal to install the extension. This will install the extension under the `_extensions` subdirectory. If you're using version control (e.g., *Git*), you will want to check in this directory.

```bash
quarto add quarto-ext/pointer
```

In addition to using the `DLM-Quarto` extension, I would highly recommend running the code above as well to add the pointer quarto extension. You can read more about the extension [here](https://github.com/quarto-ext/pointer/tree/main) with a sample presentation [here](https://quarto-ext.github.io/pointer/#/title-slide). Once you add this extension there is nothing else that is needed with this extension. If you want to change the pointer options listed on that GitHub page, you can go into the `_extensions` folder to the `_extension.yml` file. There, you can change the *key*, pointer *color*, *pointerSize*, and whether you want the pointer to be *alwaysVisible*. 

```bash
quarto add atlas-aai/dlm-quarto
quarto add quarto-ext/pointer
```

The code above will run both the `dlm-quarto` extension and the `pointer` extension. 

## Use

Since this extension is a template for having slides that follow the DLM slides for PowerPoint, add this to an existing revealjs set of slides. The example uses parameters (`params`) that can be altered under the `params` in the template to include the author's name, GitHub, website, and sources for images included in the slides. The format needs to be included and the revealjs-plugins also need to be included so the template and the pointer will be included.

```bash
---
params:
  title: DLM Example Presentation
  subtitle: ""
  author: ATLAS Staff
  author_github: https://github.com/jpedroza1228
  author_website: ""
  dlm_website: https://dynamiclearningmaps.org/
  image1_source: https://www.pexels.com/photo/colored-liquids-on-beakers-and-flasks-5427862/
  image2_source: https://unsplash.com/photos/colored-pencil-lined-up-on-top-of-white-surface-l3N9Q27zULw
  image3_source: https://www.pexels.com/photo/person-holding-yellow-and-pink-lego-blocks-298825/
  image4_source: https://www.pexels.com/photo/photo-of-girl-reading-book-3755707/
  image5_source: https://www.pexels.com/photo/brother-and-sister-with-books-on-their-heads-5088188/
title: "`r params$title`"
subtitle: "`r params$subtitle`"
author: "`r params$author`"
date: "`r Sys.Date()`"
format:  
  dlm-quarto-revealjs: default
revealjs-plugins:
    - pointer
---
```

Within the `_extensions` folder, the `quarto-dlm.scss` file can be altered in the sections below. You can change the colors, font sizes, and background color of slides that contain a table. I would recommend not changing anything else unless the html code has failed and the slides are not correctly formatted.

```bash
//If you want, you can change these values to represent the colors you would like to use with your presentation
$theme-darkblue: #023047;
$theme-lightblue: #8ecae6;
$theme-white: #F7F8F9;
$theme-red: #d7263d;
$theme-code-red: #a80303;
$theme-heading-font-size: 40pt;
$theme-font-size: 30pt;
$theme-code-font-size: 20pt;
$theme-background-image: url("dlm_background.png");
$theme-font-family: "Trebuchet MS", sans-serif;
$theme-footer-font-size: 10pt;
$theme-body-font-color: #000000;
$theme-table-background-color: white; 
$theme-h2-text-location: center;
$theme-gt-table-font-size: 16pt;
$theme-plot-width: 80%;
```

## Example

Here is the source code for a minimal example: [template.qmd](template.qmd).


## Questions/Errors

If there are any questions or errors that you are facing, please leave a query in the `Issues` section, or if you appear to have a fix, you can create a `pull request` and I will incorporate it in the next version of the extension.
