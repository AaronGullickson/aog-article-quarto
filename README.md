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
  aog-article-pdf: default
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

The template uses two optional custom arguments, `shorttitle` and `shortauthors` to control a fancy top header. These can be specified in the yaml header like:

```yaml
title: The Full Really Long Title
shorttitle: A Short Title
shortauthors: Johnson, et. al.
```

This short authors argument will appear in the upper left of each page and the short title will appear in the upper right.

Because the template only uses custom headers and tex partials, all of the customization available to the regular PDF format will work with this template. In particular, here are all of the settings you could tweak in the YAML header:

```yaml
aog-article-pdf:
  papersize: letter
  mainfont: Baskerville 
  sansfont: Futura-Medium
  fontsize: 12pt   
  geometry: margin=1in
  fig-height: 4     # smaller fig heights make floating easier
  fig-width: 7.5    # set to the (full width - margins) of letter   
  fig-pos: "!t"
  colorlinks: true
  urlcolor: red
```

When replacing fonts, you should check `systemfonts::sytem_fonts()` to confirm which fonts are available on your local system.
