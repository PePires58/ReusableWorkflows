# NodeJs build workflow doc

In this repository you will find how to use the workflow.

- 1 - Goals:
The goals of this workflow are to restore the dependencies, run the unit tests (if you want), zip the node_modules file and upload it as artifact in order to be used in another workflow.

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

- 3 - Examples:
Check some examples of use bellow

```
1 - Build-lambda:
    uses: PePires58/ReusableWorkflows/.github/workflows/001_nodejs_build.yaml@main
    with:
      working-directory: "src"
      execute-unit-tests: "false"
      name-test-script: "test-unit"

2 - Build-lambda:
    uses: PePires58/ReusableWorkflows/.github/workflows/001_nodejs_build.yaml@main

3 - Build-lambda:
    uses: PePires58/ReusableWorkflows/.github/workflows/001_nodejs_build.yaml@main
    with:
      working-directory: "src"
      name-test-script: "test-unit"
```