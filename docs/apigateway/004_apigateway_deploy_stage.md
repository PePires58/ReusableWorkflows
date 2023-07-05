# API Gateway deploy stage pipeline

In this repository you will find how to use the workflow.

- 1 - Goals:
The goal of this workflow is to deploy your stage by name in AWS.

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
    uses: PePires58/ReusableWorkflows/.github/workflows/004_apigateway_deploy_stage.yaml@main
    with: 
      api-gateway-name: "Escola de Software - Usuarios - Api Gateway - dev"
    secrets:
      AWS_BUCKET_DEPLOY: ${{ secrets.AWS_BUCKET_DEPLOY }}
      AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
      AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
```

```
    Deploy-API-Pipe:
    uses: PePires58/ReusableWorkflows/.github/workflows/004_apigateway_deploy_stage.yaml@main
    with: 
      api-gateway-name: "Escola de Software - Usuarios - Api Gateway - prod"
      stage-name: "prod"
    secrets:
      AWS_BUCKET_DEPLOY: ${{ secrets.AWS_BUCKET_DEPLOY }}
      AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
      AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
```