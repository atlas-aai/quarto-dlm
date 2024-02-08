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

Since this extension is a template for having slides that follow the DLM slides for PowerPoint, adding this extension will 

## Example

Here is the source code for a minimal example: [template.qmd](template.qmd).

