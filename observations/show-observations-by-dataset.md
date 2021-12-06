# Observations endpoint


## `GET /project/{projectId}/datasets/{datasetId}/observations`


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
`http://<base_url>/project/1/datasets/1/observations`


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
            "TDS":null
        },
        {
            "pH":"7.180000",
            "Salinity":"0.000000",
            "Conductivity (mV)":"33.200000",
            "DO (%)":"68.600000",
            "Light (lux)":"75526.000000",
            "Temperature (C)":"25.300000",
            "TDS":null
        },
        {
            "pH":"7.170000",
            "Salinity":"0.000000",
            "Conductivity (mV)":"32.400000",
            "DO (%)":"46.200000",
            "Light (lux)":"69089.000000",
            "Temperature (C)":"25.300000",
            "TDS":null
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
| {datasetColumnName} | optional | Name of the dataset column w/ value to filter with. |

## Example Request 1
`http://<base_url>/project/1/datasets/1/observations?pH=7.170000`


## Sample response for filter query
```
{
  "data": {
    "observations" : [
        {
            "pH":"7.170000",
            "Salinity":"0.000000",
            "Conductivity (mV)":"32.400000",
            "DO (%)":"46.200000",
            "Light (lux)":"69089.000000",
            "Temperature (C)":"25.300000",
            "TDS":null
        },
        {
            "pH":"7.170000",
            "Salinity":"0.000000",
            "Conductivity (mV)":"49.700000",
            "DO (%)":"29.300000",
            "Light (lux)":"26790.000000",
            "Temperature (C)":"25.200000",
            "TDS":null
        }
    ]
  },
  "status": "success"
}
```


## Example Request 2
`http://<base_url>/project/1/datasets/1/observations?TDS=60`


## Sample response for filter query
```
{
  "data": {
    "observations" : [
        {
            "pH":"7.970000",
            "Salinity":"0.000000",
            "Conductivity (mV)":"27.000000",
            "DO (%)":"62.200000",
            "Light (lux)":"24831.000000",
            "Temperature (C)":"27.140000",
            "TDS":"62.000000"
        },
        {
            "pH":"7.950000",
            "Salinity":"0.000000",
            "Conductivity (mV)":"25.900000",
            "DO (%)":"61.400000",
            "Light (lux)":"24377.000000",
            "Temperature (C)":"27.710000",
            "TDS":"62.000000"
        },
        {
            "pH":"7.910000",
            "Salinity":"0.000000",
            "Conductivity (mV)":"25.000000",
            "DO (%)":"60.470000",
            "Light (lux)":"30255.000000",
            "Temperature (C)":"27.470000",
            "TDS":"62.000000"
        }
    ]
  },
  "status": "success"
}
```

