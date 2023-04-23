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

<!-- language: lang-zh -->
## Terraform 最佳模板是一個被廣泛接受的標準專案結構，可以減少錯誤和提高可讀性

### 專案根目錄：專案應該放置的資料夾類型

| 種類 | 描述 | 資料夾位置 |
| --- | --- | --- |
| 主要程式碼 | 存放terraform相關的主要程式碼 | application |
| 說明文件 | 專案相關的所有文件檔案與資料類型檔案 | doc |
| script | 存放主要的腳本檔案 | script |
| .gitignore | git不上傳非必要的文件 | . |
| README | 提供 Terraform 專案的說明和使用方法 | . |

### Application資料夾：主程式碼放置的資料夾

種類    | 描述                               | 資料夾位置
--------|------------------------------------|---------------------------
模組目錄 | 將不同的資源分為不同的模組，方便重複使用和管理 | application/module
配置文件 | 將不同環境的配置文件分開存放，提高可讀性和可維護性 | application/infra
Variable 變數 | 將重要的資訊輸出，方便使用者查看 | application/1-variables.tf
Output 輸出 | 將重要的資訊輸出，方便使用者查看 | application/1-output.tf
Main    | 主要共用程式碼                       | application/2-main.tf
程式碼   | 將對應程式碼，按照資源產生的順序做流水號 | application/3-gke.tf
變數複寫 | 變數對照表，將私密資料只存放在本機，不做git上傳 | application/terraform.tfvars
變數複寫範例 | 變數對照表，範例檔案，讓其他開發人員知道對應的變數有哪些 | application/terraform.tfvars.example
