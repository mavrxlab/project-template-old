# NSF Section Template

An R Markdown template for NSF proposals based on Matt Crump's [NSFrmarkdown](https://github.com/CrumpLab/NSFrmarkdown) package. This is a sub-project within the larger project template repository.

## Steps

- Rename `NSFRMarkdown.rproj` appropriately and open *that* `.rproj` file. The automation in this project *will not work* if you are working in the larger repository's `.rproj` file!
- Edit the .Rmd files for each of the sections of the grant. If you knit the document, a .pdf will be compiled into the doc folder.
- The standard Pandoc reference methods (`[@authorTitleYYYY]` citation keys, for example) work, so be sure to update `references.bib`.
- You can compile all of the .Rmd files at once by using the build tab, and clicking build website.

## Tweaking the style

The style folder contains `nsf2.cls` and  `preamble.tex`. Both of which can be edited to change aspects of the style.

### section numbering

Turn section numbering within a document on or off by setting `number_sections: true` or `number_sections: false` in the YAML. The style of section-numbering is controlled using the titlesec latex package in `nsf2.cls` (style folder)

## Embedding R graphs

The `Project_Description.Rmd` contains one example of embedding an R figure, and wrapping text around the figure.
