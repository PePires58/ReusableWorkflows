# NodeJs deploy npm workflow doc

In this repository you will find how to use the workflow.

- 1 - Goals:
The goals of this workflow are to take the dependencies created and deploy your package to npm in a automated way. Don't forget to pass the NPM_TOKEN secret and to create it on your account at npm.

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
    <tbody>
</table>

- 3 - Examples:
Check some examples of use bellow

```
    Deploy-package:
    uses: PePires58/ReusableWorkflows/.github/workflows/001_nodejs_deploy_npm.yaml@main
    with:
      working-directory: "src/meudiretorio"
    secrets:
        NPM_TOKEN: ${{ secrets.NPM_TOKEN }}
```

```
    Deploy-package:
    uses: PePires58/ReusableWorkflows/.github/workflows/001_nodejs_deploy_npm.yaml@main
    secrets:
        NPM_TOKEN: ${{ secrets.NPM_TOKEN }}
```