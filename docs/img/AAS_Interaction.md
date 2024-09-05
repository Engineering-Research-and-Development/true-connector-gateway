# Asset Administration Shell Interaction

This short guide serves as a guide to retrieve and interact with AAS using the gateway.

There are two main BaSyx components that serves to browse an AAS through the [Basyx v1 APIs](https://app.swaggerhub.com/apis/BaSyx/basyx_asset_administration_shell_repository_http_rest_api/v1#/AssetAdministrationShellRepository/ShellRepo_GetSubmodelElementByIdShort)
- The [AAS Server](https://wiki.basyx.org/en/latest/content/user_documentation/basyx_components/v1/aas-server/index.html#) that apply CRUD operations to AAS
- The [AAS Registry](https://wiki.basyx.org/en/latest/content/user_documentation/basyx_components/v1/registry/index.html) that searches for AAS IDs


#### Short Guide:
- Call for the AAS server to browse all AASs registered in this server:
  - GET http://localhost:4001/aasServer/shells/
    ![image](https://github.com/user-attachments/assets/a9f71e53-c10a-4dc1-861a-657889b403ee)

- Call for the AAS registry to search the endpoints related to a specific AAS: GET http://localhost:4000/registry/api/v1/registry
  - GET http://localhost:4000/registry/api/v1/registry
  - Search for a specific endpoint, wheter it is the AAS Descriptor or a Submodel Descriptor
    ![image](https://github.com/user-attachments/assets/3755abfb-a651-4827-ada3-945e57fff539)
    ![image](https://github.com/user-attachments/assets/d2fdd29d-807f-4c3f-bff8-1d0c774eaaea)


- Call for the AAS server again, browsing the specific asset and interact:
  - GET "http://localhost:4001/aasServer/shells/http%3A%2F%2Fcustomer.com%2Faas%2F9175_7013_7091_9168/aas/submodels/OperationalData/submodel"
  - GET "http://localhost:4001/aasServer/shells/http%3A%2F%2Fcustomer.com%2Faas%2F9175_7013_7091_9168/aas/
