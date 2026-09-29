# DataCite content negotation

DataCite content negotation

## Usage

``` r
dc_cn(dois, format = "bibtex", style = "apa", locale = "en-US", ...)
```

## Arguments

- dois:

  (character) one or more DOIs

- format:

  Name of the format. One of "rdf-xml", "turtle", "citeproc-json",
  "schemaorg", "codemeta", "text", "ris", "bibtex" (default),
  "datacite-xml", "datacite-json", "bibentry", or "jats".

- style:

  a CSL style (for text format only). See ‘rcrossref::get_styles()’ for
  options. Default: 'apa'. If there's a style that DataCite doesn't
  support you'll get a (500) Internal Server Error

- locale:

  Language locale. See ‘?Sys.getlocale’

- ...:

  curl options passed on to
  [crul::verb-GET](https://docs.ropensci.org/crul/reference/verb-GET.html)

## References

https://support.datacite.org/docs/datacite-content-resolver

## See also

see also `rcrossref::cr_cn` for a more general purpose content
negotation interface

## Examples

``` r
if (FALSE) { # \dontrun{
dc_cn("10.5281/zenodo.50213")
dc_cn(c("10.5281/zenodo.50213", "10.5281/zenodo.57081"), "text")
dc_cn(c("a-bad-doi", "10.5281/zenodo.50213", "10.5281/zenodo.57081"), "text")
} # }
```
