# mango-pagedown

> Testing out css for a Mango Pagedown theme

## Getting started

You'll need to install [pagedown](https://github.com/rstudio/pagedown) in R.

```r
install.packages("pagedown")
```

To build the test Rmd, `test-pagedown.Rmd`, you open it in RStudio and click the "knit" button, and this will knit and openthe file in your browser. Otherwise you can do:

```r
rmarkdown::render("test-pagedown.Rmd")
```

and this will build the html without opening the browser.


## Making changes

### CSS

in `css/`

Instead of adding on CSS I've copied through everything from pagedown. So we can change as much as we like there. There are three:

* `mango-fonts.css`: fonts
* `default.css`: some core css that I (Doug) don't understand
* `mango-page.css`: This is where we can tweak margins and footers and so on

### Images

in `img/`

There are some standard branding images, both png and svg, that we can use.

### Layout

in `templates/`

I think most of the layout changes will happen in `templates/mango-paged.html`. This is a template doc that pandoc uses to turn the markdown file into html. I (Doug) don't really know this templating language but I feel it may be key.

For example. We'll need to add new divs for exercise boxes. In markdown it'll be something like:

```
Exercise {#exercise}
```

And somehow that becomes a named div in html.

## Our current style

in `word/`

You can see what the material looks like now in `word/03 Getting Data into R.docx`. Some things would be nice to keep:

* I like the overall colours, company logo's in there.
* I quite like how page and section numbering works.

Other things can just go:

* We can play with fonts (although should check overall company branding).
* I hate how we do code right now so that can completely change. Default RMarkdown is already way better.
* Warnings, tips, and exercise boxes. Need to look better. We do have some icons somewhere, although I reckon some appropriate font-awesome icon would do.

But really there's no strict requirements. If it's super hard to do that chapter numbering then we can live without it, for example.
