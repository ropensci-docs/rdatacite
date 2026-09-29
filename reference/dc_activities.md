# DataCite REST API: activities

DataCite REST API: activities

## Usage

``` r
dc_activities(
  ids = NULL,
  query = NULL,
  limit = 25,
  page = 1,
  cursor = NULL,
  ...
)
```

## Arguments

- ids:

  (character) one or more activity IDs

- query:

  (character) Query string

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

## Details

for more info on the `/activities` route see
https://support.datacite.org/docs/tracking-provenance

## Examples

``` r
if (FALSE) { # \dontrun{
if (dc_check()) {
x <- dc_activities()
x
# dc_activities(x$data$id[1]) # FIXME: doesn't work, returns no data
# dc_activities(query = "ecology") # FIXME: this thlimit a 500 error
}} # }
```
