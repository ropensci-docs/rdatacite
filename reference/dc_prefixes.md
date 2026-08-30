# DataCite REST API: prefixes

DataCite REST API: prefixes

## Usage

``` r
dc_prefixes(include = NULL, limit = 25, page = 1, cursor = NULL, ...)
```

## Arguments

- include:

  (character) vector of fields to return

- limit:

  (numeric/integer) results per page

- page:

  (numeric/integer) result page, the record to start at

- cursor:

  (character) page cursor (used instead of `limit` param)

- ...:

  curl options passed on to
  [crul::HttpClient](https://docs.ropensci.org/crul/reference/HttpClient.html)

## Examples

``` r
if (FALSE) { # \dontrun{
if (dc_check()) {
x <- dc_prefixes()
x
dc_prefixes(limit = 3)
}} # }
```
