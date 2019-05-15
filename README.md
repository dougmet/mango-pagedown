# mango-pagedown

> Testing out css for a Mango Pagedown theme

## Getting started

You'll need to install [pagedown](https://github.com/rstudio/pagedown) in R.

```r
install.packages("pagedown")
```

To build the test Rmd you open it in RStudio and click the "knit" button, and this will knit and openthe file in your browser. Otherwise you can do:

```r
rmarkdown::render("test-pagedown.Rmd")
```

and this will build the html without opening the browser.


## Layout

Main assets are in:

```
css
img
templates
```

The `test-pagedown.Rmd` file is a working template. It explicitly sets the css to the files used here.

The `word` directory is an example of current materials. Probably should have added as pdf for fair comparison.

## Our current style

You can see what the material looks like now in `word/03 Getting Data into R.docx`. Some things would be nice to keep:

* I like the overall colours, company logo's in there.
* I quite like how page and section numbering works.

Other things can just go:

* We can play with fonts (although should check overall company branding).
* I hate how we do code right now so that can completely change. Default RMarkdown is already way better.
* Warnings, tips, and exercise boxes. Need to look better. We do have some icons somewhere, although I reckon some appropriate font-awesome icon would do.

But really there's no strict requirements. If it's super hard to do that chapter numbering then we can live without it, for example.
