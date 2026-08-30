# DataCite REST API: events

DataCite REST API: events

## Usage

``` r
dc_events(
  ids = NULL,
  query = NULL,
  subj_id = NULL,
  obj_id = NULL,
  doi = NULL,
  orcid = NULL,
  prefix = NULL,
  subtype = NULL,
  subject = NULL,
  source_id = NULL,
  registrant_id = NULL,
  relation_type_id = NULL,
  issn = NULL,
  publication_year = NULL,
  year_month = NULL,
  include = NULL,
  sort = NULL,
  limit = 25,
  page = 1,
  cursor = NULL,
  ...
)
```

## Arguments

- ids:

  (character) one or more event IDs

- query:

  (character) Query for any event information

- subj_id:

  (character) The identifier for the event subject, expressed as a URL.
  For example: `https://doi.org/10.7272/q6qn64nk`

- obj_id:

  (character) The identifier for the event object, expressed as a URL.
  For example: `https://doi.org/10.7272/q6qn64nk`

- doi:

  (character) The subj-id or obj-id of the event, expressed as a DOI.
  For example: `10.7272/q6qn64nk`

- orcid:

  (character) an ORCID, presumably

- prefix:

  (character) The DOI prefix of the subj-id or obj-id of the event. For
  example: `10.7272`

- subtype:

  (character) xxx

- subject:

  (character) xxx

- source_id:

  (character) a source ID. See Details

- registrant_id:

  (character)

- relation_type_id:

  (character) a relation-type ID. See Details

- issn:

  (character) an ISSN, presumably

- publication_year:

  (character) the publication year

- year_month:

  (character) The year and month in which the event occurred, in the
  format `YYYY-MM`. For example `2018-08`

- include:

  (character) vector of fields to return

- sort:

  (character) variable to sort by

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

See https://support.datacite.org/docs/eventdata-guide for details on
possible values for parameters

## Examples

``` r
if (FALSE) { # \dontrun{
if (dc_check()) {
# dc_events(query = "birds")
}} # }
```
