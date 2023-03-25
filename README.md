# AOG Article Template

This is my Quarto template to create a nice "published paper" quality PDF for scholarly work. The style is inspired by Steven V. Miller's R Markdown [article templates](https://github.com/svmiller/stevetemplates) which I used for many years and Andrew Heiss's [Hikmah templates](https://github.com/andrewheiss/hikmah-academic-quarto) and draws LaTeX code from both sources.  You can see a preview of the template at <https://aarongullickson.quarto.pub/demo-of-aog-article-template/>. 

## Installation

To install this template as an extension for an existing document, run the following command in your project working directory:

```bash
quarto install extension AaronGullickson/aog-article-quarto
```

To your quarto document yaml, add:

```yaml
format:
  aog-article-pdf:
    keep-tex: true
```

Or, alternatively, from the command line:

```bash
quarto render article.qmd --to aog-article-pdf
```

## Using the Template

If you want to start a new article from the template or just check out the existing test document, run the following command:

```bash
quarto use template AaronGullickson/aog-article-quarto
```

You can render the `template.qmd` provided to try it out.

## Customization

The template uses only one custom argument, `shorttitle`, which can be specified in the yaml header, like:

```yaml
title: The Full Really Long Title
shorttitle: A Short Title
```

This short title will appear in the upper left header of each page.

Because the template only uses custom headers and tex partials, all of the customization available to the regular PDF format will work with this template. In particular, here are all of the standard settings used by the template which can be overridden by the YAML in the user's document:

```yaml
pdf:
  papersize: letter
  # Replace fonts with any fonts available to the *system*
  mainfont: Baskerville 
  sansfont: Futura
  fontsize: 12pt   
  geometry: margin=1in
  fig-height: 4     # smaller fig heights make floating easier
  fig-width: 7.5    # set to the (full width - margins) of letter   
  fig-pos: "!t"
  colorlinks: true
  urlcolor: red
```
