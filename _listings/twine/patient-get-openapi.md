---
swagger: "2.0"
x-collection-name: Twine
x-complete: 0
info:
  title: Twine List patients
  description: Get a list of patients.
  version: 7.18.0
host: api.twinehealth.com
basePath: /pub
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /patient:
    get:
      summary: List patients
      description: Get a list of patients.
      operationId: fetchPatients
      x-api-path-slug: patient-get
      parameters:
      - in: query
        name: filter[archived]
        description: If not specified, return all patients
      - in: query
        name: filter[created_at]
        description: The start (inclusive) and end (exclusive) dates are ISO date
          and time strings separated by `
      - in: query
        name: filter[groups]
        description: Comma-separated list of group ids
      - in: query
        name: filter[identifier][system]
        description: 'Identifier system (example: MyEHR) - requires a filter[identifier][value]
          parameter'
      - in: query
        name: filter[identifier][value]
        description: 'Identifier value (example: 12345) - requires a filter[identifier][system]
          parameter'
      - in: query
        name: filter[organization]
        description: Twine organization id
      - in: query
        name: filter[updated_at]
        description: The start (inclusive) and end (exclusive) dates are ISO date
          and time strings separated by `
      - in: query
        name: page[number]
        description: Page number
      - in: query
        name: page[size]
        description: Page size
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - List
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