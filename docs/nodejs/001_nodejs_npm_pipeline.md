# NodeJs npm deploy full pipiline workflow doc

In this repository you will find how to use the workflow.

- 1 - Goals:
The goals of this workflow are to restore dependencies, run unit tests, download the artifact of node_modules, unzip it, build a package and deploy using your token.
This workflow is only usable to deploy to npm packages.

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
               working-directory
            </td>
            <td>
                string
            </td>
            <td>
                false
            </td>
            <td>
                src
            </td>
        </tr>
        <tr>
            <td>
                execute-unit-tests
            </td>
            <td>
                string
            </td>
            <td>
                false
            </td>
            <td>
                "true"
            </td>
        </tr>
        <tr>
            <td>
                name-test-script
            </td>
            <td>
                string
            </td>
            <td>
                false
            </td>
            <td>
                test
            </td>
        </tr>
    <tbody>
</table>

- 3 - Examples

Check somes examples bellow

```
    Deploy-npm-package:
    uses: PePires58/ReusableWorkflows/.github/workflows/001_nodejs_npm_pipeline.yaml@main
    secrets:
        NPM_TOKEN: ${{ secrets.NPM_TOKEN }}

```

```
    Deploy-lambda:
    uses: PePires58/ReusableWorkflows/.github/workflows/001_nodejs_npm_pipeline.yaml@main
    with: 
      execute-unit-tests: "false"
    secrets:
        NPM_TOKEN: ${{ secrets.NPM_TOKEN }}

```