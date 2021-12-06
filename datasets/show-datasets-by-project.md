# Datasets endpoint


## `GET /project/{projectId}/datasets`


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


## Example Request
`http://<base_url>/project/1/datasets`


## Sample response
```
{
  "data": {
    "datasets" : [
      {
        "id":1,
        "concept_id":1,
        "name":"Physicochemical Parameters",
        "lake_id":1,
        "project_id":1,
        "description":"Dataset for Lake Danao",
        "created_at":"2021-09-12T10:33:56.000000Z",
        "updated_at":"2021-09-12T10:33:56.000000Z"
      },
      {
        "id":2,
        "concept_id":2,
        "name":"Total and Fecal Coliform",
        "lake_id":1,
        "project_id":1,
        "description":"Dataset for Lake Danao",
        "created_at":"2021-09-12T10:33:56.000000Z",
        "updated_at":"2021-09-12T10:33:56.000000Z"
      },
      {
        "id":3,
        "concept_id":3,
        "name":"Nutrient, Heavy Metal and Weather Data",
        "lake_id":1,
        "project_id":1,
        "description":"Dataset for Lake Danao",
        "created_at":"2021-09-12T10:33:57.000000Z",
        "updated_at":"2021-09-12T10:33:57.000000Z"
      },
      ...
    ]
  },
  "status": "success"
}```
