# Observations endpoint


## `GET /project/{projectId}/datasets/{datasetId}/observations/concepts/{conceptId}`


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
| conceptId | required | Id of the concept/column name of the dataset. |


## Example Request
`http://<base_url>/project/1/datasets/1/observations/concepts/1`


## Sample response
```
{
  "data": {
    "observations" : [
        {
            "pH":"7.210000",
            "Salinity":"0.000000",
            "Conductivity (mV)":"34.700000",
            "DO (%)":"56.000000",
            "Light (lux)":"74390.000000",
            "Temperature (C)":"25.300000",
            "TDS":null,
            "Date Collected":"2021-03-08 00:00:00"
        },
        {
            "pH":"7.180000",
            "Salinity":"0.000000",
            "Conductivity (mV)":"33.200000",
            "DO (%)":"68.600000",
            "Light (lux)":"75526.000000",
            "Temperature (C)":"25.300000",
            "TDS":null,
            "Date Collected":"2021-03-08 00:00:00"
        },
        {
            "pH":"7.170000",
            "Salinity":"0.000000",
            "Conductivity (mV)":"32.400000",
            "DO (%)":"46.200000",
            "Light (lux)":"69089.000000",
            "Temperature (C)":"25.300000",
            "TDS":null,
            "Date Collected":"2021-03-08 00:00:00"
        },
        ...
    ]
  },
  "status": "success"
}```
