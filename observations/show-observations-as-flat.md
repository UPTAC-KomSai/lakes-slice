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
        }
    ]
  },
  "status": "success"
}```
