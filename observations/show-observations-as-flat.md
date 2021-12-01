# Observations endpoint


## `GET /project/{projectId}/datasets/{datasetId}/observations/flat`


## Resource Information
|Property|Value|
|-----|------|
| Response Format | JSON |
| Requires Authentication? | No | 

## Parameters

### Path Parameters

| Name | Required | Description|
| ------ | ------ | ------ |
| projectId | required | Id of the project where the observations is from. |
| datasetId | required | Id of the dataset/record of the project. |


## Example Request
`http://<base_url>/project/1/datasets/1/observations/flat`


## Sample response
```
{
  "data": {
    "observations" : [
        {
            "id":1,
            "observation_group":"1_1",
            "concept_id":1,
            "value_numeric":"7.210000",
            "value_text":null,
            "value_coded":null,
            "date_collected":"2021-03-08 00:00:00",
            "location_geopoint":"Somewhere in Ormoc",
            "sample_id":1,
            "created_at":"2021-09-12 10:33:57",
            "updated_at":"2021-09-12 10:33:57"
        },
        {
            "id":2,
            "observation_group":"1_2",
            "concept_id":1,
            "value_numeric":"7.180000",
            "value_text":null,
            "value_coded":null,
            "date_collected":"2021-03-08 00:00:00",
            "location_geopoint":"Somewhere in Ormoc",
            "sample_id":2,
            "created_at":"2021-09-12 10:33:57",
            "updated_at":"2021-09-12 10:33:57"
        },
        {
            "id":3,
            "observation_group":"1_3",
            "concept_id":1,
            "value_numeric":"7.170000",
            "value_text":null,
            "value_coded":null,
            "date_collected":"2021-03-08 00:00:00",
            "location_geopoint":"Somewhere in Ormoc",
            "sample_id":3,
            "created_at":"2021-09-12 10:33:57",
            "updated_at":"2021-09-12 10:33:57"
        },
        ...
    ]
  },
  "status": "success"
}
```


### Query Parameters

| Name | Required | Description|
| ------ | ------ | ------ |
| {observationsTableColumnName} | optional | column name of Observations table w/ value being filtered. |


## Example Request 1
`http://<base_url>/project/1/datasets/1/observations/flat?value_numeric=7.21`


## Sample response 1
```
{
  "data": {
    "observations" : [
        {
            "id":1,
            "observation_group":"1_1",
            "dataset_id":1,
            "concept_id":1,
            "value_numeric":"7.210000",
            "value_text":null,
            "value_coded":null,
            "date_collected":"2021-03-08 00:00:00",
            "location_geopoint":"Somewhere in Ormoc",
            "sample_id":1,
            "created_at":"2021-09-12 10:33:57",
            "updated_at":"2021-09-12 10:33:57"
        },
        {
            "id":54,
            "observation_group":"1_54",
            "dataset_id":1,
            "concept_id":1,
            "value_numeric":"7.210000",
            "value_text":null,
            "value_coded":null,
            "date_collected":"2021-04-24 00:00:00",
            "location_geopoint":"Somewhere in Ormoc",
            "sample_id":54,
            "created_at":"2021-09-12 10:33:57",
            "updated_at":"2021-09-12 10:33:57"
        }
    ]
  },
  "status": "success"
}
```


## Example Request 2
`http://<base_url>/project/1/datasets/1/observations/flat?observation_group=1_4`


## Sample response 1
```
{
  "data": {
    "observations" : [
        {
            "id":4,
            "observation_group":"1_4",
            "dataset_id":1,
            "concept_id":1,
            "value_numeric":"7.110000",
            "value_text":null,
            "value_coded":null,
            "date_collected":"2021-03-08 00:00:00",
            "location_geopoint":"Somewhere in Ormoc",
            "sample_id":4,
            "created_at":"2021-09-12 10:33:57",
            "updated_at":"2021-09-12 10:33:57"
        },
        {
            "id":124,
            "observation_group":"1_4",
            "dataset_id":1,
            "concept_id":2,
            "value_numeric":"0.000000",
            "value_text":null,
            "value_coded":null,
            "date_collected":"2021-03-08 00:00:00",
            "location_geopoint":"Somewhere in Ormoc",
            "sample_id":124,
            "created_at":"2021-09-12 10:33:57",
            "updated_at":"2021-09-12 10:33:57"
        },
        {
            "id":244,
            "observation_group":"1_4",
            "dataset_id":1,
            "concept_id":3,
            "value_numeric":"29.700000",
            "value_text":null,
            "value_coded":null,
            "date_collected":"2021-03-08 00:00:00",
            "location_geopoint":"Somewhere in Ormoc",
            "sample_id":244,
            "created_at":"2021-09-12 10:33:58",
            "updated_at":"2021-09-12 10:33:58"
        },
        {
            "id":364,
            "observation_group":"1_4",
            "dataset_id":1,
            "concept_id":4,
            "value_numeric":"53.200000",
            "value_text":null,
            "value_coded":null,
            "date_collected":"2021-03-08 00:00:00",
            "location_geopoint":"Somewhere in Ormoc",
            "sample_id":364,
            "created_at":"2021-09-12 10:33:59",
            "updated_at":"2021-09-12 10:33:59"
        },
        {
            "id":469,
            "observation_group":"1_4",
            "dataset_id":1,
            "concept_id":5,
            "value_numeric":"36669.000000",
            "value_text":null,
            "value_coded":null,
            "date_collected":"2021-03-08 00:00:00",
            "location_geopoint":"Somewhere in Ormoc",
            "sample_id":469,
            "created_at":"2021-09-12 10:33:59",
            "updated_at":"2021-09-12 10:33:59"
        },
        {
            "id":589,
            "observation_group":"1_4",
            "dataset_id":1,
            "concept_id":6,
            "value_numeric":"25.400000",
            "value_text":null,
            "value_coded":null,
            "date_collected":"2021-03-08 00:00:00",
            "location_geopoint":"Somewhere in Ormoc",
            "sample_id":589,
            "created_at":"2021-09-12 10:34:00",
            "updated_at":"2021-09-12 10:34:00"
        }
    ]
  },
  "status": "success"
}
```