# DataCite REST API: reports

DataCite REST API: reports

## Usage

``` r
dc_reports(
  ids = NULL,
  platform = NULL,
  report_name = NULL,
  report_id = NULL,
  release = NULL,
  created = NULL,
  created_by = NULL,
  include = NULL,
  limit = 25,
  page = 1,
  ...
)
```

## Arguments

- ids:

  (character) one or more report IDs

- platform:

  (character) Name of the Platform the usage is being requested for.
  This can be omitted if the service provides usage for only one
  platform.

- report_name:

  (character) The long name of the report

- report_id:

  (character) The report ID or code or shortname. Typically this will be
  the same code provided in the Report parameter of the request

- release:

  (character) The release or version of the report

- created:

  (character) Time the report was prepared. Format as defined by
  date-time - RFC3339

- created_by:

  (character) Name of the organization producing the report

- include:

  (character) vector of fields to return

- limit:

  (numeric/integer) results per page

- page:

  (numeric/integer) result page, the record to start at

- ...:

  curl options passed on to
  [crul::HttpClient](https://docs.ropensci.org/crul/reference/HttpClient.html)

## Examples

``` r
if (FALSE) { # \dontrun{
if (dc_check()) {
x <- dc_reports()
x
dc_reports(created = "2019-08-01T07:00:00.000Z")
dc_reports(created_by = "urn:node:GOA")
dc_reports(limit = 3)
# dc_reports(ids = x$reports$id[1:3]) # FIXME: doesn't work
}} # }
```
