# DataCite REST API: client prefixes

DataCite REST API: client prefixes

## Usage

``` r
dc_client_prefixes(
  query = NULL,
  year = NULL,
  client_id = NULL,
  prefix_id = NULL,
  sort = NULL,
  include = NULL,
  limit = 25,
  page = 1,
  cursor = NULL,
  ...
)
```

## Arguments

- query:

  (character) Query string

- year:

  (integer/numeric/character) a year

- client_id:

  a client ID

- prefix_id:

  a prefix ID

- sort:

  (character) variable to sort by

- include:

  (character) vector of fields to return

- limit:

  (numeric/integer) results per page

- page:

  (numeric/integer) the page to get results for. default: 1

- cursor:

  (character) page cursor (used instead of `limit` param). to use cursor
  pagination, set `cursor = 1`, then use the link in `$links$next`

- ...:

  curl options passed on to
  [crul::verb-GET](https://docs.ropensci.org/crul/reference/verb-GET.html)

## Examples

``` r
if (FALSE) { # \dontrun{
if (dc_check()) {
x <- dc_client_prefixes()
x
}} # }
```
