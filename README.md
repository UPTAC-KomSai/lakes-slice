# Lakes SLICE API Documentation

**Note**: 
*  - [ ] - endpoint has not yet been implemented
*  - [x] - endpoint implementation is finished

## Endpoints

### Observations Endpoints

Endpoints for viewing observations either by dataset, by project, etc.

 * - [x] [Show observations by dataset](observations/show-observations-by-dataset.md) : `GET /project/{projectId}/datasets/{datasetId}/observations`
 * - [x] [Show observations by dataset as flat w/ no groupings](observations/show-observations-as-flat.md) : `GET /project/{projectId}/datasets/{datasetId}/observations/flat`
 * - [x] [Show all observations for the project](observations/show-observations-by-project.md) : `GET /project/{projectId}/observations`

### Datasets Endpoints

Endpoints for viewing datasets either by project, specific dataset, etc.

 * - [x] [Show all datasets for the project](datasets/show-datasets-by-project.md) : `GET /project/{projectId}/datasets`