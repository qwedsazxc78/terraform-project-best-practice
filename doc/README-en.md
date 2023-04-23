<!-- language: lang-en -->
# Terraform project best practice

## The Terraform Best Practices Template is a widely accepted standard project structure that can reduce errors and improve readability

### project root directory: types of folders that should be placed in the project


| Type | Description | Folder Location |
| --- | --- | --- |
| Main Code | Contains the main Terraform code | application |
| Documentation | Contains all project-related files and data type files | doc |
| Scripts | Contains main script files | script |
| .gitignore | Excludes unnecessary files from being uploaded to git | . |
| README | Provides instructions and usage details for the Terraform project | . |

### Application: the folder where the main code is placed

Type | Description | Directory Location
---- | ----------- | ------------------
Module Directory | Separates different resources into different modules for easy reuse and management | application/module
Configuration Files | Separates configuration files for different environments for improved readability and maintainability | application/infra
Variable | Outputs important information for user reference | application/1-variables.tf
Output | Outputs important information for user reference | application/1-output.tf
Main | Main shared code | application/2-main.tf
Code | Corresponding code based on resource generation order | application/3-gke.tf
Variable Override | Variable lookup table to store sensitive data locally and not upload to git | application/terraform.tfvars
Variable Override Example | Example variable lookup table to inform other developers which variables are used | application/terraform.tfvars.example
