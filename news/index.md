# Changelog

## rdatacite 0.5.4

CRAN release: 2023-02-05

#### MAINTAINER CHANGE

- maintainer changed from Scott Chamberlain to Bianca Kramer
  ([\#32](https://github.com/ropensci/rdatacite/issues/32))

## rdatacite 0.5.2

CRAN release: 2020-03-04

#### MINOR IMPROVEMENTS

- fix breaking test on one of the cran checks
  ([\#30](https://github.com/ropensci/rdatacite/issues/30))

## rdatacite 0.5.0

CRAN release: 2020-01-08

#### NEW FEATURES

- Major refactor to work with the new DataCite API: all functions from
  the previous version are defunct; all OAI-PMH functions are gone; new
  functions all start with `dc_`
  ([\#24](https://github.com/ropensci/rdatacite/issues/24))
  ([\#29](https://github.com/ropensci/rdatacite/issues/29))

#### MINOR IMPROVEMENTS

- all examples check if DataCite API is up before running
  ([\#28](https://github.com/ropensci/rdatacite/issues/28))

## rdatacite 0.4.2

CRAN release: 2019-05-07

#### MINOR IMPROVEMENTS

- fix to two fixtures that had non-ascii text in them, that were causing
  tests to fail
  ([\#25](https://github.com/ropensci/rdatacite/issues/25))

## rdatacite 0.4.0

CRAN release: 2018-05-27

#### MINOR IMPROVEMENTS

- pagination fixes
  ([\#18](https://github.com/ropensci/rdatacite/issues/18))
- fix unused httr package warning, flagged by cran team
  ([\#21](https://github.com/ropensci/rdatacite/issues/21))
- add .github PR and issue templates

## rdatacite 0.3.0

CRAN release: 2017-11-03

#### NEW FEATURES

- Gains new functions for working with the DataCite REST API:
  `dc_data_center`, `dc_data_centers`, `dc_member`, `dc_members`,
  `dc_work`, `dc_works`
  ([\#13](https://github.com/ropensci/rdatacite/issues/13))
- Now using new version of solrium package - users shouldn’t see any
  differences ([\#16](https://github.com/ropensci/rdatacite/issues/16))

#### BUG FIXES

- Fix scientific notation
  ([\#15](https://github.com/ropensci/rdatacite/issues/15))
- Fix `vapply` error
  ([\#14](https://github.com/ropensci/rdatacite/issues/14))

## rdatacite 0.1.0

CRAN release: 2016-02-12

#### NEW FEATURES

- Released to CRAN.
