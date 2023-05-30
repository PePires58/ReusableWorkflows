## Reusable Workflows

Welcome to the Pepires58 reusable workflows, in this repository you can find some workflows that can help you in your development proccess.

# NodeJs Workflows

- 1 - Nodejs build: in this workflow you can restore dependencies, test and zip the node_modules as artifacts to other proccess. You will need to download the artifacts in order to restore node_modules.

Check more informations and how to use in: [NodeJs build documentation](https://github.com/PePires58/ReusableWorkflows/blob/main/docs/nodejs/001_nodejs_build_doc.md)

- 2 - NodeJs deploy: in this workflow you can restore dependencies (store as artifact), unzip node_modules, build a SAM template and deploy your code with cloudformation.

Check more informations and how to use in: [NodeJs deploy documentation](https://github.com/PePires58/ReusableWorkflows/blob/main/docs/nodejs/001_nodejs_deploy_doc.md)

- 3 - Nodejs deploy full pipeline: in this workflow you can restore dependencies, run tests, build sam template and deploy your code with cloudformation. Use this workflow and don't worry about your workflow, just use and let it deploy your code.

Check more information and how to use in: [NodeJs deploy full pipeline](https://github.com/PePires58/ReusableWorkflows/blob/main/docs/nodejs/001_nodejs_deploy_pipeline_doc.md)

Thanks a lot