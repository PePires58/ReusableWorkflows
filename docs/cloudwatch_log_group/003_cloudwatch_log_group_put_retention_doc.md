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
                log-group-name
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
               retention-in-days
            </td>
            <td>
                number
            </td>
            <td>
                false
            </td>
            <td>
                3
            </td>
        </tr>
    <tbody>
</table>

- 3 - Examples

Check somes examples bellow

```
    Update-LogGroup:
    uses: PePires58/ReusableWorkflows/.github/workflows/003_cloudwatch_log_group_put_retention.yaml@main
    with: 
      log-group-name: "/aws/lambda/dev_escoladesoftware-autorizador-lambdarealizarloginfn"
      retention-in-days: 5
    secrets:
      AWS_BUCKET_DEPLOY: ${{ secrets.AWS_BUCKET_DEPLOY }}
      AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
      AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
```

```
    Update-LogGroup:
    uses: PePires58/ReusableWorkflows/.github/workflows/003_cloudwatch_log_group_put_retention.yaml@main
    with: 
      log-group-name: "/aws/lambda/dev_escoladesoftware-autorizador-lambdarealizarloginfn"
    secrets:
      AWS_BUCKET_DEPLOY: ${{ secrets.AWS_BUCKET_DEPLOY }}
      AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
      AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
```