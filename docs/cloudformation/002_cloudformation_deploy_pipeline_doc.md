# Cloudformation deploy full pipiline workflow doc

In this repository you will find how to use the workflow.

- 1 - Goals:
The goals of this workflow are to build a SAM template, package it into an S3 bucket and deploy your infrastructure creating a stack with cloudformation stacks. This workflow uses a CloudFormation template file.

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
    <tbody>
</table>

- 3 - Examples

Check somes examples bellow

```
    Deploy-infra:
    uses: PePires58/ReusableWorkflows/.github/workflows/002_cloudformation_deploy_pipeline.yaml@main
    with: 
      stack-name: "dev-escoladesoftware-cursos-bucketcursos"
      parameters-file-path: "infra/dev.parameters.json"
      aws-region: "us-east-1"
    secrets:
      AWS_BUCKET_DEPLOY: ${{ secrets.AWS_BUCKET_DEPLOY }}
      AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
      AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
```

```
    Deploy-infra:
    uses: PePires58/ReusableWorkflows/.github/workflows/002_cloudformation_deploy_pipeline.yaml@main
    with: 
      stack-name: "dev-escoladesoftware-cursos-bucketcursos"
      parameters-file-path: "infra/dev.parameters.json"
    secrets:
      AWS_BUCKET_DEPLOY: ${{ secrets.AWS_BUCKET_DEPLOY }}
      AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
      AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
```