# rdatacite

DataCite R client

## HTTP Requests

All HTTP requests are GET requests, and are sent with the following
headers:

- `Accept: application/vnd.api+json; version=2`

- `User-Agent: r-curl/4.3 crul/0.9.0 rOpenSci(rdatacite/0.5.0)`

- `X-USER-AGENT: r-curl/4.3 crul/0.9.0 rOpenSci(rdatacite/0.5.0)`

The user-agent strings change as the versions of each package change.

## Methods in the package

- [`dc_providers()`](https://docs.ropensci.org/rdatacite/reference/dc_providers.md)

- [`dc_reports()`](https://docs.ropensci.org/rdatacite/reference/dc_reports.md)

- [`dc_check()`](https://docs.ropensci.org/rdatacite/reference/dc_check.md)

- [`dc_events()`](https://docs.ropensci.org/rdatacite/reference/dc_events.md)

- [`dc_dois()`](https://docs.ropensci.org/rdatacite/reference/dc_dois.md)

- [`dc_clients()`](https://docs.ropensci.org/rdatacite/reference/dc_clients.md)

- [`dc_client_prefixes()`](https://docs.ropensci.org/rdatacite/reference/dc_client_prefixes.md)

- [`dc_provider_prefixes()`](https://docs.ropensci.org/rdatacite/reference/dc_provider_prefixes.md)

- [`dc_status()`](https://docs.ropensci.org/rdatacite/reference/dc_status.md)

- [`dc_prefixes()`](https://docs.ropensci.org/rdatacite/reference/dc_prefixes.md)

- [`dc_activities()`](https://docs.ropensci.org/rdatacite/reference/dc_activities.md)

## rdatacite defunct functions

- `dc_data_center`

- `dc_data_centers`

- `dc_facet`

- `dc_member`

- `dc_members`

- `dc_mlt`

- `dc_oai_getrecord`

- `dc_oai_identify`

- `dc_oai_listidentifiers`

- `dc_oai_listmetadataformats`

- `dc_oai_listrecords`

- `dc_oai_listsets`

- `dc_search`

- `dc_stats`

- `dc_work`

- `dc_works`

## Content negotation

For content negotation see `rcrossref::cr_cn()`, which can be used for
Crossref, DataCite and Medra DOIs

## GraphGL API

rdatacite does not support the GraphGL API
https://support.datacite.org/docs/datacite-graphql-api-guide - we
suggest trying the `ghql` package (https://github.com/ropensci/ghql/)

## Author

Scott Chamberlain <myrmecocystus@gmail.com>
