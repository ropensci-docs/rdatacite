# DataCite REST API: dois

DataCite REST API: dois

## Usage

``` r
dc_dois(
  ids = NULL,
  query = NULL,
  created = NULL,
  registered = NULL,
  provider_id = NULL,
  client_id = NULL,
  person_id = NULL,
  resource_type_id = NULL,
  subject = NULL,
  schema_version = NULL,
  random = NULL,
  sample_size = NULL,
  sample_group = NULL,
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

  (character) one or more DOIs

- query:

  (character) Query string. See Querying below.

- created:

  (character) metadata where year of DOI creation is `created`. See
  Filtering Responses below.

- registered:

  (character) metadata where year of DOI registration is `year`. See
  Filtering Responses below.

- provider_id:

  (character) metadata associated with a specific DataCite provider. See
  Filtering Responses below.

- client_id:

  (character) metadata associated with a specific DataCite client. See
  Filtering Responses below.

- person_id:

  (character) metadata associated with a specific person's ORCID iD. See
  Filtering Responses below.

- resource_type_id:

  (character) metadata for a specific resourceTypeGeneral. See Filtering
  Responses below.

- subject:

  (character)

- schema_version:

  (character) metadata where schema version of the deposited metadata is
  `schema-version`. See Filtering Responses below.

- random:

  (logical) return random set of results, can be combined with any kind
  of query. default: `FALSE`.

- sample_size:

  (character)

- sample_group:

  (character)

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

## Querying

See https://support.datacite.org/docs/api-queries for details

## Filtering Responses

See
https://support.datacite.org/docs/api-queries#section-filtering-list-responses
for details

## Examples

``` r
if (FALSE) { # \dontrun{
if (dc_check()) {
x <- dc_dois()
x
dc_dois(query = "birds")
dc_dois(query = "climate change")
dc_dois(query = "publicationYear:2016")
x <- dc_dois(query = "creators.familyName:mil*", verbose = TRUE)
lapply(x$data$attributes$creators, "[[", "familyName")
x <- dc_dois(query = "titles.title:climate +change")
lapply(x$data$attributes$titles, "[[", "title")
dc_dois(client_id = "dryad.dryad")
dc_dois(x$data$id[1])
dc_dois(x$data$id[1:3])
dc_dois("10.5281/zenodo.1308060")

# pagination
dc_dois(limit = 1)
x <- dc_dois(cursor = 1)
x$links$`next`
}} # }
```
