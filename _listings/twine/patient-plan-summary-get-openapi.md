---
swagger: "2.0"
x-collection-name: Twine
x-complete: 0
info:
  title: Twine List patient plan summaries
  description: Get a list of patient plan summaries
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
    post:
      summary: Create a patient
      description: |-
        Create a patient record.

        Example for creating a patient with a group specified using `meta.query` instead of `id`:

        ```JSON
        {
          "data": {
            "type": "patient",
            "attributes": {
              "first_name": "Andrew",
              "last_name": "Smith"
            },
            "relationships": {
              "groups": {
                "data": [
                  {
                    "type": "group",
                    "meta": {
                      "query": {
                        "organization": "58c88de7c93eb96357a87033",
                        "name": "Patients Lead"
                      }
                    }
                  }
                ]
              }
            }
          }
        }
        ```
      operationId: createPatient
      x-api-path-slug: patient-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - Patient
  /patient/{id}:
    get:
      summary: Get a patient
      description: Gets a patient record by id.
      operationId: fetchPatient
      x-api-path-slug: patientid-get
      parameters:
      - in: path
        name: id
        description: Patient identifier
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - Patient
    patch:
      summary: Update a patient
      description: Update a patient record.
      operationId: updatePatient
      x-api-path-slug: patientid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: Patient identifier
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - Patient
  /patient/{id}/coaches:
    get:
      summary: List coaches for a patient
      description: Get the list of coaches for a patient.
      operationId: fetchPatientCoaches
      x-api-path-slug: patientidcoaches-get
      parameters:
      - in: path
        name: id
        description: Patient identifier
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - List
      - Coachesa
      - Patient
  /patient/{id}/groups:
    get:
      summary: List groups for a patient
      description: Get the list of groups for a patient.
      operationId: fetchPatientGroups
      x-api-path-slug: patientidgroups-get
      parameters:
      - in: path
        name: id
        description: Patient identifier
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - List
      - Groupsa
      - Patient
  /patient_health_metric:
    get:
      summary: List patient health metrics
      description: Get a list of patient health metrics.
      operationId: fetchPatientHealthMetrics
      x-api-path-slug: patient-health-metric-get
      parameters:
      - in: query
        name: filter[patient]
        description: Filter the patient health metrics for a specified patient
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
      - Patient
      - Health
      - Metrics
    post:
      summary: Create patient health metrics
      description: |-
        Create one or more patient health metrics.

        Example for creating a patient health result with a patient specified using `meta.query` instead of `id`:

        ```JSON
          {
            "data": {
              "type": "patient_health_metric",
               "attributes": {
                 "code": {
                   "system": "LOINC",
                   "value": "13457-7"
                 },
                 "type": "ldl_cholesterol",
                 "occurred_at": "2017-03-14T11:00:57.000Z",
                 "value": "121",
                 "unit": "mg/dl"
              },
              "relationships": {
                "patient": {
                  "data": {
                    "type": "patient",
                    "meta": {
                      "query": {
                        "identifier": {
                          "system": "medical-record-number",
                          "value": "121212"
                        },
                        "organization": "58c4554710123c5c40dbab81"
                      }
                    }
                  }
                }
              }
            }
          }
        ```
      operationId: createPatientHealthMetric
      x-api-path-slug: patient-health-metric-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - Patient
      - Health
      - Metrics
  /patient_health_metric/{id}:
    get:
      summary: Get a patient health metric
      description: Get the plan summary for a patient.
      operationId: fetchPatientHealthMetric
      x-api-path-slug: patient-health-metricid-get
      parameters:
      - in: path
        name: id
        description: Patient health metric identifier
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - Patient
      - Health
      - Metric
  /patient_plan_summary:
    get:
      summary: List patient plan summaries
      description: Get a list of patient plan summaries
      operationId: fetchPatientPlanSummaries
      x-api-path-slug: patient-plan-summary-get
      parameters:
      - in: query
        name: filter[patient]
        description: Patient id to fetch plan summary for
      - in: query
        name: include
        description: List of related resources to include in the response
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - List
      - Patient
      - Plan
      - Summaries
  /patient_plan_summary/{id}:
    get:
      summary: Get the plan summary for a patient
      description: Get the plan summary for a patient.
      operationId: fetchPatientPlanSummary
      x-api-path-slug: patient-plan-summaryid-get
      parameters:
      - in: path
        name: id
        description: Plan summary identifier
      - in: query
        name: include
        description: List of related resources to include in the response
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - Plan
      - Summarya
      - Patient
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