# NodeJs deploy workflow doc

In this repository you will find how to use the workflow.

- 1 - Goals:
The goals of this workflow are to download the artifact of node_modules, unzip it, build a sam template and deploy using cloudformation.
This workflow is only usable to deploy to AWS.

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
