# DataCite REST API: providers

DataCite REST API: providers

## Usage

``` r
dc_providers(
  ids = NULL,
  query = NULL,
  year = NULL,
  region = NULL,
  organization_type = NULL,
  focus_area = NULL,
  include = NULL,
  limit = 25,
  page = 1,
  cursor = NULL,
  ...
)
```

## Arguments

- ids:

  (character) one or more provider IDs

- query:

  (character) query string

- year:

  (character) year

- region:

  (character) region name

- organization_type:

  (character) organization type

- focus_area:

  (character) focus area

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
x <- dc_providers()
x
dc_providers(limit = 3)
dc_providers(ids = x$data$id[1:5])
}} # }
```
