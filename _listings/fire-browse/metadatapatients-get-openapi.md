---
swagger: "2.0"
x-collection-name: Fire Browse
x-complete: 0
info:
  title: Fire Browse Beta API Retrieve list of all TCGA patients.
  description: This service returns a list of all TCGA patient barcodes in FireBrowse,
    optionally filtered by disease cohort.  The barcodes are obtained directy from
    the clinical data.
  version: 1.1.35 (2016-09-27 10:12:23 6a47e74011281b2aa
host: firebrowse.org
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Metadata/Patients:
    get:
      summary: Retrieve list of all TCGA patients.
      description: This service returns a list of all TCGA patient barcodes in FireBrowse,
        optionally filtered by disease cohort.  The barcodes are obtained directy
        from the clinical data.
      operationId: getMetadataPatients
      x-api-path-slug: metadatapatients-get
      parameters:
      - in: query
        name: cohort
        description: Narrow search to one or more TCGA disease cohorts from the scrollable
          list
      - in: query
        name: format
        description: Format of result
      - in: query
        name: page
        description: Which page (slice) of entire results set should be returned
      - in: query
        name: page_size
        description: Number of records per page of results
      - in: query
        name: sort_by
        description: Which column in the results should be used for sorting paginated
          results?
      responses:
        200:
          description: OK
      tags:
      - Metadata
      - Patients
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---