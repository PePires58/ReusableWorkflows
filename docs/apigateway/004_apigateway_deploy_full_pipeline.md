# API Gateway deploy full pipeline

In this repository you will find how to use the workflow.

- 1 - Goals:
The goals of this workflow are to deploy your API in AWS and deploy your stage as well.

- 2 - Parameters:
<table>
    <thead>
        <tr>
            <td> 
                Name
            </td>
            <td>
                Type
            </td>
            <td>
                Is required
            </td>
            <td>
                Default value
            </td>
        <tr>
    </thead>
    <tbody>
        <tr>
            <td>
                aws-region
            </td>
            <td>
                string
            </td>
            <td>
                false
            </td>
            <td>
                sa-east-1
            </td>
        </tr>
        <tr>
            <td>
                stack-name
            </td>
            <td>
                string
            </td>
            <td>
                true
            </td>
            <td>
                -
            </td>
        </tr>
        <tr>
            <td>
                parameters-file-path
            </td>
            <td>
                string
            </td>
            <td>
                true
            </td>
            <td>
                -
            </td>
        </tr>
        <tr>
            <td>
               template-file
            </td>
            <td>
                string
            </td>
            <td>
                false
            </td>
            <td>
                template.yaml
            </td>
        </tr>
        <tr>
            <td>
                api-gateway-name
            </td>
            <td>
                string
            </td>
            <td>
                true
            </td>
            <td>
                -
            </td>
        </tr>
        <tr>
            <td>
                stage-name
            </td>
            <td>
                string
            </td>
            <td>
                false
            </td>
            <td>
                "dev"
            </td>
        </tr>
    <tbody>
</table>

- 3 - Examples

Check somes examples bellow

```
    Deploy-API-Pipe:
    uses: PePires58/ReusableWorkflows/.github/workflows/004_apigateway_deploy_full_pipeline.yaml@main
    with: 
      stack-name: "dev-escoladesoftware-usuarios-apigateway"
      parameters-file-path: "infra/dev.parameters.json"
      api-gateway-name: "Escola de Software - Usuarios - Api Gateway - dev"
    secrets:
      AWS_BUCKET_DEPLOY: ${{ secrets.AWS_BUCKET_DEPLOY }}
      AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
      AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
```

```
    Deploy-API-Pipe:
    uses: PePires58/ReusableWorkflows/.github/workflows/004_apigateway_deploy_full_pipeline.yaml@main
    with: 
      stack-name: "prod-escoladesoftware-usuarios-apigateway"
      parameters-file-path: "infra/prod.parameters.json"
      api-gateway-name: "Escola de Software - Usuarios - Api Gateway - prod"
      stage-name: "prod"
    secrets:
      AWS_BUCKET_DEPLOY: ${{ secrets.AWS_BUCKET_DEPLOY }}
      AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
      AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
```