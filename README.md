## Reusable Workflows

Welcome to the Pepires58 reusable workflows, in this repository you can find some workflows that can help you in your development proccess.

# NodeJs Workflows

- 1 - Nodejs build: in this workflow you can restore dependencies, test and zip the node_modules as artifacts to other proccess. You will need to download the artifacts in order to restore node_modules.

Check more informations and how to use in: [NodeJs build documentation](https://github.com/PePires58/ReusableWorkflows/blob/main/docs/nodejs/001_nodejs_build_doc.md)

- 2 - NodeJs deploy: in this workflow you can restore dependencies (store as artifact), unzip node_modules, build a SAM template and deploy your code with cloudformation.

Check more informations and how to use in: [NodeJs deploy documentation](https://github.com/PePires58/ReusableWorkflows/blob/main/docs/nodejs/001_nodejs_deploy_doc.md)

- 3 - Nodejs deploy full pipeline: in this workflow you can restore dependencies, run tests, build sam template and deploy your code with cloudformation. Use this workflow and don't worry about your workflow, just use and let it deploy your code.

Check more information and how to use in: [NodeJs deploy full pipeline](https://github.com/PePires58/ReusableWorkflows/blob/main/docs/nodejs/001_nodejs_deploy_pipeline_doc.md)

# CloudFormation workflows

- 1 - CloudFormation deploy pipeline: in this workflow you can deploy your infrastructure as code, using CloudFormation template. Don't worry about to create the pipeline to it, just pass the keys, the bucket to package and build the template and that is it.

Check more informations and how to use in: [CloudFormation deploy pipeline](https://github.com/PePires58/ReusableWorkflows/blob/main/docs/cloudformation/002_cloudformation_deploy_pipeline_doc.md)

# CloudWatch - Log Group - Workflows

- 1 - CloudWatch LogGroup Put Retention workflow: in this workflow you can update your LogGroup retention period after create it. You only need to pass the log group name and the retention day if you want (default is 3 days).

Check more informations and how to use in: [CloudWatch LogGroup PutRetentionDays](https://github.com/PePires58/ReusableWorkflows/blob/main/docs/cloudwatch_log_group/003_cloudwatch_log_group_put_retention_doc.md)

# API Gateway - Workflows

- 1 - API Gateway deploy full pipeline: in this workflow you can deploy your API and deploy your stage in a once. You just need to pass the parameters and that is it.

Check more informations and how to use in: [API Gateway deploy full pipeline](https://github.com/PePires58/ReusableWorkflows/blob/main/docs/apigateway/004_apigateway_deploy_full_pipeline.md)

Thanks a lot