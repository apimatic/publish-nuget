This workflow uses the APIMatic API to generate a .NET SDK for the specified API and publishes it to nuget.org.
In order to execute the workflow, you will first need to create the following **repository secrets**:
1. API_ENTITY_ID: The [ID of the API](https://docs.apimatic.io/manage-apis/get-api-keys/) imported into APIMatic.
2. APIMATIC_API_KEY: The [Authentication key](https://docs.apimatic.io/account-management/obtaining-auth-keys/) required to use APIMatic's API. 
3. NUGET_API_KEY: Your nuget.org [API Key]((https://docs.apimatic.io/manage-apis/get-api-keys/))  
4. PACKAGE_NAME: The Name of your Nuget Package
5. [Optional] PACKAGE_VERSION: The semantic version to be assigned to the package in the subsequent release. If this number is not provided, the workflow attempts to retrieve the current package version from nuget.org and increments the patch version. If the package is not yet published, it will be automatically assigned a version number of _1.0.1_.

With all the repository secrets in place, trigger the workflow to generate and publish a Nuget package.

