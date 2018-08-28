---
name: Twine
x-slug: twine
description: 'Twine Health is a cloud-based collaborative care platform for chronic
  disease management. It consists of a patient engagement portal, a peer support network,
  a care management solution, and an outcome analytics tool. The platform enables
  users to co-create personalized care plans that serve as common ground for collaboration
  with their care team: their own providers such as physicians and nurse practitioners;
  their family and friends; and coaches such as nurses, pharmacists, health coaches,
  and more.'
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
x-kinRank: "7"
x-alexaRank: "0"
tags: Patients
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/apis.md
specificationVersion: "0.14"
apis:
- name: Twine - List patients
  x-api-slug: patient-get
  description: Get a list of patients.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-get-openapi.md
- name: Twine - Create a patient
  x-api-slug: patient-post
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-post-openapi.md
- name: Twine - Get a patient
  x-api-slug: patientid-get
  description: Gets a patient record by id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patientid-get-openapi.md
- name: Twine - Update a patient
  x-api-slug: patientid-patch
  description: Update a patient record.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patientid-patch-openapi.md
- name: Twine - List coaches for a patient
  x-api-slug: patientidcoaches-get
  description: Get the list of coaches for a patient.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patientidcoaches-get-openapi.md
- name: Twine - List groups for a patient
  x-api-slug: patientidgroups-get
  description: Get the list of groups for a patient.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patientidgroups-get-openapi.md
- name: Twine - List patient health metrics
  x-api-slug: patient-health-metric-get
  description: Get a list of patient health metrics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-health-metric-get-openapi.md
- name: Twine - Create patient health metrics
  x-api-slug: patient-health-metric-post
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-health-metric-post-openapi.md
- name: Twine - Get a patient health metric
  x-api-slug: patient-health-metricid-get
  description: Get the plan summary for a patient.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-health-metricid-get-openapi.md
- name: Twine - List patient plan summaries
  x-api-slug: patient-plan-summary-get
  description: Get a list of patient plan summaries
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-plan-summary-get-openapi.md
- name: Twine - Get the plan summary for a patient
  x-api-slug: patient-plan-summaryid-get
  description: Get the plan summary for a patient.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-plan-summaryid-get-openapi.md
- name: Twine - Create a patient
  x-api-slug: patient-post
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-post-openapi.md
- name: Twine - Get a patient
  x-api-slug: patientid-get
  description: Gets a patient record by id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patientid-get-openapi.md
- name: Twine - Update a patient
  x-api-slug: patientid-patch
  description: Update a patient record.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patientid-patch-openapi.md
- name: Twine - List coaches for a patient
  x-api-slug: patientidcoaches-get
  description: Get the list of coaches for a patient.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patientidcoaches-get-openapi.md
- name: Twine - List groups for a patient
  x-api-slug: patientidgroups-get
  description: Get the list of groups for a patient.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patientidgroups-get-openapi.md
- name: Twine - List patient health metrics
  x-api-slug: patient-health-metric-get
  description: Get a list of patient health metrics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-health-metric-get-openapi.md
- name: Twine - Create patient health metrics
  x-api-slug: patient-health-metric-post
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-health-metric-post-openapi.md
- name: Twine - Get a patient health metric
  x-api-slug: patient-health-metricid-get
  description: Get the plan summary for a patient.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-health-metricid-get-openapi.md
- name: Twine - List patient plan summaries
  x-api-slug: patient-plan-summary-get
  description: Get a list of patient plan summaries
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-plan-summary-get-openapi.md
- name: Twine - Get the plan summary for a patient
  x-api-slug: patient-plan-summaryid-get
  description: Get the plan summary for a patient.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-plan-summaryid-get-openapi.md
- name: Twine - Get the plan summary for a patient
  x-api-slug: patient-plan-summaryid-get
  description: Get the plan summary for a patient.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-plan-summaryid-get-openapi.md
- name: Twine - List patient plan summaries
  x-api-slug: patient-plan-summary-get
  description: Get a list of patient plan summaries
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-plan-summary-get-openapi.md
- name: Twine - Get a patient health metric
  x-api-slug: patient-health-metricid-get
  description: Get the plan summary for a patient.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-health-metricid-get-openapi.md
- name: Twine - Create patient health metrics
  x-api-slug: patient-health-metric-post
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-health-metric-post-openapi.md
- name: Twine - List patient health metrics
  x-api-slug: patient-health-metric-get
  description: Get a list of patient health metrics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-health-metric-get-openapi.md
- name: Twine - List groups for a patient
  x-api-slug: patientidgroups-get
  description: Get the list of groups for a patient.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patientidgroups-get-openapi.md
- name: Twine - List coaches for a patient
  x-api-slug: patientidcoaches-get
  description: Get the list of coaches for a patient.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patientidcoaches-get-openapi.md
- name: Twine - Update a patient
  x-api-slug: patientid-patch
  description: Update a patient record.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patientid-patch-openapi.md
- name: Twine - Get a patient
  x-api-slug: patientid-get
  description: Gets a patient record by id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patientid-get-openapi.md
- name: Twine - Create a patient
  x-api-slug: patient-post
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/twinehealth.png
  humanURL: http://twinehealth.com
  baseURL: https://api.twinehealth.com//pub
  tags: Wearables, Healthcare, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/patients/master/_listings/twine/patient-post-openapi.md
x-common:
- type: x-api-gallery
  url: http://twilio.api.gallery.streamdata.io
- type: x-api-stack
  url: http://twine.stack.network
- type: x-authentication
  url: http://developer.twinehealth.com/#section/Authentication
- type: x-developer
  url: http://developer.twinehealth.com/
- type: x-website
  url: http://twinehealth.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---