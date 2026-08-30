# DataCite REST API: clients

DataCite REST API: clients

## Usage

``` r
dc_clients(
  ids = NULL,
  query = NULL,
  year = NULL,
  provider_id = NULL,
  software = NULL,
  include = NULL,
  limit = 25,
  page = 1,
  cursor = NULL,
  ...
)
```

## Arguments

- ids:

  (character) one or more client IDs

- query:

  (character) Query string

- year:

  (integer/numeric/character) a year

- provider_id:

  a provider ID

- software:

  no idea what should go here, anyone?

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
x <- dc_clients()
x
dc_clients(x$data$id[1])
dc_clients(x$data$id[1:2], verbose = TRUE)
}} # }
```
