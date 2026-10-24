---
page_type: sample
languages:
- terraform
- hcl
name: Introduction to using Azure Verified Modules for Terraform
description: A walk through lab demonstrating how to use the Azure Verified Modules for Terraform.
products:
- azure
urlFragment: avm-terraform-labs
---

# Introduction to using Azure Verified Modules for Terraform

> [!NOTE]
> **Repository Context & Community Enhancements 🌐**:
> This repository [**nubenetes/avm-terraform-labs**](https://github.com/nubenetes/avm-terraform-labs) is an enhanced fork of the official Microsoft reference sample [**Azure-Samples/avm-terraform-labs**](https://github.com/Azure-Samples/avm-terraform-labs).
> 
> - **Upstream Reference**: [Azure-Samples/avm-terraform-labs](https://github.com/Azure-Samples/avm-terraform-labs) is the official Microsoft sample demonstrating step-by-step practical implementation of Azure Verified Modules (AVM) for Terraform.
> - **Active Fork**: [nubenetes/avm-terraform-labs](https://github.com/nubenetes/avm-terraform-labs) maintains updated module pins, automated CI/CD pipeline validation, modular lab sub-documentation, and a dedicated **11-session multimedia video series** synthesized with **Gemini NotebookLM**.


This is a lab based sample that demonstrates how to use the Azure Verified Modules for Terraform. The repository contains the full working solution, but you should follow the steps in the lab to understand how it fits together.

## Content

| File/folder | Description |
|-------------|-------------|
| `labs` | The files for the lab. |
| `.gitignore` | Define what to ignore at commit time. |
| `CHANGELOG.md` | List of changes to the sample. |
| `CONTRIBUTING.md` | Guidelines for contributing to the sample. |
| `README.md` | This README file. |
| `LICENSE.md` | The license for the sample. |

## Features

This sample deploys the following features:

* Log Analytics Workspace
* Virtual network
* Subnets
* Network security groups
* Virtual machines
* Azure Bastion Host
* Managed identities
* Key Vault
* Storage account with customer managed key
* Private end points and associated private DNS zones

![architecture diagram](./images/levelup-tf-lab-part05.jpg)

## 🎥 Video Guides, Technical Shorts & Multimedia Learning Sessions (YouTube)

The architecture, zero-trust network design, Key Vault secret orchestration, customer-managed key (CMK) encryption, and passwordless managed identity workflows of this lab are accompanied by a dedicated series of technical video guides and rapid architecture shorts synthesized with **Gemini NotebookLM**.

All sessions are hosted on the official YouTube channel [**@nubenetes**](https://youtube.com/@nubenetes).

> [!NOTE]
> **Multilingual Technical Content 🌐**:
> The architectural masterclasses and shorts feature native **English** technical narration with auto-generated subtitles (CC) in over **20 languages** to assist cloud platform teams, enterprise architects, and site reliability engineers worldwide.

### 📊 Technical Multimedia Catalog (11 Sessions)

#### 📽️ Deep-Dive Architectural Video Guide (1 Episode)

| Format | Title / Episode | Focus / Core Engineering Domain | Language | Duration | Direct YouTube Link |
| :---: | :--- | :--- | :---: | :---: | :--- |
| 📽️ **Video Guide** | [**Azure Verified Modules Lab: Complete Terraform End-to-End Walkthrough**](https://www.youtube.com/watch?v=I4s0A1uXEUg) | **End-to-End Architecture Walkthrough**: Full lab build from Part 0 to Part 8: Log Analytics, hardened VNet, NAT Gateway, Key Vault, CMK storage encryption, VM, and Bastion | 🇬🇧 English *(CC 20+)* | `7:02` | [▶️ Watch Video](https://www.youtube.com/watch?v=I4s0A1uXEUg) |

#### ⚡ Technical Shorts & Architecture Takeaways (10 Episodes)

| Format | Title / Episode | Focus / Lab Stage | Language | Duration | Direct YouTube Link |
| :---: | :--- | :--- | :---: | :---: | :--- |
| ⚡ **Short** | [**How Local Code Builds Azure Clouds**](https://www.youtube.com/shorts/BnkctVGCD8A) | **Part 0 & 1 (Toolchain)**: Chaining VS Code, Azure CLI, and Terraform CLI to turn declarative HCL files into cloud infrastructure | 🇬🇧 English *(CC 20+)* | `1:10` | [▶️ Watch Short](https://www.youtube.com/shorts/BnkctVGCD8A) |
| ⚡ **Short** | [**How Azure Centralizes Cloud Monitoring**](https://www.youtube.com/shorts/oBkA9k32ECQ) | **Part 1 (Log Analytics)**: Establishing `avm-res-log-analytics-workspace` upfront as the automated diagnostic sink for all resources | 🇬🇧 English *(CC 20+)* | `1:14` | [▶️ Watch Short](https://www.youtube.com/shorts/oBkA9k32ECQ) |
| ⚡ **Short** | [**How Terraform Deploys Azure Verified Modules**](https://www.youtube.com/shorts/EsIyH6PSGrE) | **Part 1 (IaC Lifecycle)**: Managing the Terraform provisioning lifecycle (init, plan, apply, destroy) with version-pinned AVM modules | 🇬🇧 English *(CC 20+)* | `1:10` | [▶️ Watch Short](https://www.youtube.com/shorts/EsIyH6PSGrE) |
| ⚡ **Short** | [**How Azure Bastion Secures Virtual Machines**](https://www.youtube.com/shorts/QeVoCsTMBOQ) | **Part 2, 5 & 6 (Bastion Security)**: Browser-based TLS proxying into deep subnets with zero public IPs or open management ports | 🇬🇧 English *(CC 20+)* | `1:14` | [▶️ Watch Short](https://www.youtube.com/shorts/QeVoCsTMBOQ) |
| ⚡ **Short** | [**How Azure Key Vault Secures Infrastructure**](https://www.youtube.com/shorts/-JlLcd-4CIs) | **Part 3 (Key Vault)**: Generating and storing VM SSH keys directly inside Key Vault using `avm-res-keyvault-vault` without local leaks | 🇬🇧 English *(CC 20+)* | `1:14` | [▶️ Watch Short](https://www.youtube.com/shorts/-JlLcd-4CIs) |
| ⚡ **Short** | [**How Azure Private Endpoints Lock Down Data**](https://www.youtube.com/shorts/xf5UNTUjYjY) | **Part 3 & 4 (Private PaaS)**: Projecting Key Vault and Storage into private subnets via RFC 1918 IPs and centralized Private DNS zones | 🇬🇧 English *(CC 20+)* | `1:18` | [▶️ Watch Short](https://www.youtube.com/shorts/xf5UNTUjYjY) |
| ⚡ **Short** | [**How Azure Verified Modules Automate CMK Encryption**](https://www.youtube.com/shorts/-Bo6tLrseDo) | **Part 4 (CMK Storage Encryption)**: Automating Storage Customer-Managed Key encryption and Key Vault RBAC handshakes in one block | 🇬🇧 English *(CC 20+)* | `1:20` | [▶️ Watch Short](https://www.youtube.com/shorts/-Bo6tLrseDo) |
| ⚡ **Short** | [**How Managed Identities Kill Passwords**](https://www.youtube.com/shorts/2YlxRtiYll4) | **Part 4 & 5 (Zero-Secret IAM)**: Eliminating static API tokens and connection strings with System and User-Assigned Managed Identities | 🇬🇧 English *(CC 20+)* | `1:12` | [▶️ Watch Short](https://www.youtube.com/shorts/2YlxRtiYll4) |
| ⚡ **Short** | [**How Azure VMs Access Storage Without Passwords**](https://www.youtube.com/shorts/jwASueLUzhI) | **Part 7 & 8 (Passwordless Access)**: Linux VM authenticating via `az login --identity` and executing blob uploads via RBAC | 🇬🇧 English *(CC 20+)* | `1:18` | [▶️ Watch Short](https://www.youtube.com/shorts/jwASueLUzhI) |
| ⚡ **Short** | [**Deploying Secure Azure Architecture with Verified Modules**](https://www.youtube.com/shorts/xIkzOaSfB1c) | **Part 5 (Architecture Synthesis)**: Assembling pre-vetted, supported AVM modules into a complete zero-trust enterprise topology | 🇬🇧 English *(CC 20+)* | `1:16` | [▶️ Watch Short](https://www.youtube.com/shorts/xIkzOaSfB1c) |

<details>
<summary>📂 <strong>Detailed Agendas, Transcripts & Engineering Takeaways</strong></summary>

<br/>

### Section A: Deep-Dive Architectural Video Guide (1 Session)

#### 1. Azure Verified Modules Lab: Complete Terraform End-to-End Walkthrough (7:02)
- 🔗 **Direct URL**: [https://www.youtube.com/watch?v=I4s0A1uXEUg](https://www.youtube.com/watch?v=I4s0A1uXEUg)
- ⏱️ **Duration**: 7:02 | 🌐 **Language**: 🇬🇧 English *(CC 20+)*
- 🏷️ **Domain**: End-to-End Architecture, AVM Lab Walkthrough, Zero-Trust Cloud Design
- 📝 **Technical Overview**:
> Comprehensive architectural walkthrough of the entire Azure Verified Modules (AVM) Terraform Lab. Details the progression from base telemetry (Log Analytics Workspace) to a hardened virtual network, secure Key Vault, Customer-Managed Key (CMK) encrypted storage, and an isolated virtual machine accessed passwordlessly via Azure Bastion and Managed Identities.

### Section B: Technical Shorts & Architecture Takeaways (10 Sessions)

#### 2. How Local Code Builds Azure Clouds (1:10)
- 🔗 **Direct URL**: [https://www.youtube.com/shorts/BnkctVGCD8A](https://www.youtube.com/shorts/BnkctVGCD8A)
- ⏱️ **Duration**: 1:10 | 🌐 **Language**: 🇬🇧 English *(CC 20+)*
- 🏷️ **Domain**: Toolchain Orchestration, VS Code, Azure CLI, Terraform CLI
- 📝 **Technical Overview**:
> Practical guide on chaining VS Code, Azure CLI, and Terraform CLI to turn local HCL declarations into verified Azure cloud infrastructure without manual portal interaction.

#### 3. How Azure Centralizes Cloud Monitoring (1:14)
- 🔗 **Direct URL**: [https://www.youtube.com/shorts/oBkA9k32ECQ](https://www.youtube.com/shorts/oBkA9k32ECQ)
- ⏱️ **Duration**: 1:14 | 🌐 **Language**: 🇬🇧 English *(CC 20+)*
- 🏷️ **Domain**: Telemetry Architecture, Log Analytics, Automated Diagnostics
- 📝 **Technical Overview**:
> Architectural takeaway explaining why establishing a central Log Analytics Workspace in Part 1 enables all downstream AVM modules to automatically wire diagnostic logs and metrics into a unified sink.

#### 4. How Terraform Deploys Azure Verified Modules (1:10)
- 🔗 **Direct URL**: [https://www.youtube.com/shorts/EsIyH6PSGrE](https://www.youtube.com/shorts/EsIyH6PSGrE)
- ⏱️ **Duration**: 1:10 | 🌐 **Language**: 🇬🇧 English *(CC 20+)*
- 🏷️ **Domain**: IaC Provisioning Lifecycle, Dependency Graphs, Clean Teardown
- 📝 **Technical Overview**:
> Guide to the four stages of the Terraform lifecycle (init, plan, apply, destroy) with Azure Verified Modules, highlighting how state-tracked teardown eliminates orphaned resources and cost leaks.

#### 5. How Azure Bastion Secures Virtual Machines (1:14)
- 🔗 **Direct URL**: [https://www.youtube.com/shorts/QeVoCsTMBOQ](https://www.youtube.com/shorts/QeVoCsTMBOQ)
- ⏱️ **Duration**: 1:14 | 🌐 **Language**: 🇬🇧 English *(CC 20+)*
- 🏷️ **Domain**: Perimeter Security, Azure Bastion, Zero Public IPs, TLS Proxying
- 📝 **Technical Overview**:
> Security breakdown of Azure Bastion providing browser-based TLS proxying into deep subnets, completely eliminating public IPs and open management ports (SSH/RDP).

#### 6. How Azure Key Vault Secures Infrastructure (1:14)
- 🔗 **Direct URL**: [https://www.youtube.com/shorts/-JlLcd-4CIs](https://www.youtube.com/shorts/-JlLcd-4CIs)
- ⏱️ **Duration**: 1:14 | 🌐 **Language**: 🇬🇧 English *(CC 20+)*
- 🏷️ **Domain**: Secret Management, Key Vault, Zero Local Private Keys
- 📝 **Technical Overview**:
> Security short explaining how `avm-res-keyvault-vault` generates and stores SSH private keys directly in the cloud, preventing credentials from leaking onto developer workstations.

#### 7. How Azure Private Endpoints Lock Down Data (1:18)
- 🔗 **Direct URL**: [https://www.youtube.com/shorts/xf5UNTUjYjY](https://www.youtube.com/shorts/xf5UNTUjYjY)
- ⏱️ **Duration**: 1:18 | 🌐 **Language**: 🇬🇧 English *(CC 20+)*
- 🏷️ **Domain**: PaaS Isolation, Private Link, Private DNS, RFC 1918 Addressing
- 📝 **Technical Overview**:
> Technical guide on projecting Azure PaaS services (Key Vault, Storage) into private subnets with RFC 1918 private IPs, cutting off public internet exposure and routing.

#### 8. How Azure Verified Modules Automate CMK Encryption (1:20)
- 🔗 **Direct URL**: [https://www.youtube.com/shorts/-Bo6tLrseDo](https://www.youtube.com/shorts/-Bo6tLrseDo)
- ⏱️ **Duration**: 1:20 | 🌐 **Language**: 🇬🇧 English *(CC 20+)*
- 🏷️ **Domain**: Customer-Managed Keys (CMK), Storage Encryption, Automated RBAC
- 📝 **Technical Overview**:
> Architectural demonstration of how `avm-res-storage-storageaccount` orchestrates customer-managed encryption, user-assigned managed identities, and Key Vault crypto permissions in a single declarative block.

#### 9. How Managed Identities Kill Passwords (1:12)
- 🔗 **Direct URL**: [https://www.youtube.com/shorts/2YlxRtiYll4](https://www.youtube.com/shorts/2YlxRtiYll4)
- ⏱️ **Duration**: 1:12 | 🌐 **Language**: 🇬🇧 English *(CC 20+)*
- 🏷️ **Domain**: Passwordless Identity, Entra ID, Managed Identities, Scoped RBAC
- 📝 **Technical Overview**:
> Explains how System and User-Assigned Managed Identities eradicate hardcoded connection strings and access keys through automatically rotated OAuth 2.0 tokens from Entra ID.

#### 10. How Azure VMs Access Storage Without Passwords (1:18)
- 🔗 **Direct URL**: [https://www.youtube.com/shorts/jwASueLUzhI](https://www.youtube.com/shorts/jwASueLUzhI)
- ⏱️ **Duration**: 1:18 | 🌐 **Language**: 🇬🇧 English *(CC 20+)*
- 🏷️ **Domain**: Passwordless Access, Azure CLI Identity, Blob Storage RBAC
- 📝 **Technical Overview**:
> Walkthrough of a virtual machine authenticating via `az login --identity` through IMDS and securely reading/writing blobs using Storage Blob Data Contributor permissions.

#### 11. Deploying Secure Azure Architecture with Verified Modules (1:16)
- 🔗 **Direct URL**: [https://www.youtube.com/shorts/xIkzOaSfB1c](https://www.youtube.com/shorts/xIkzOaSfB1c)
- ⏱️ **Duration**: 1:16 | 🌐 **Language**: 🇬🇧 English *(CC 20+)*
- 🏷️ **Domain**: Architecture Synthesis, Composable AVM Blocks, Production Zero-Trust
- 📝 **Technical Overview**:
> High-level synthesis illustrating how combining standardized AVM modules (VNet, Key Vault, Storage, VM, Bastion) deploys an enterprise-grade, zero-trust cloud foundation in minutes.

</details>


## Getting Started

### Prerequisites

* HashiCorp Terraform CLI Version 1.10 or higher: [Download](https://www.terraform.io/downloads)
* Git: [Download](https://git-scm.com/downloads)
* Visual Studio Code: [Download](https://code.visualstudio.com/)
  * Azure Terraform Extension for Visual Studio Code: [Install](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azureterraform)
  * HashiCorp Terraform Extension for Visual Studio Code: [Install](https://marketplace.visualstudio.com/items?itemName=HashiCorp.terraform)
* Azure CLI: [Download](https://learn.microsoft.com/cli/azure/install-azure-cli-windows?tabs=azure-cli#install-or-update)
* An Azure Subscription: [Free Account](https://azure.microsoft.com/pricing/purchase-options/azure-account?cid=msft_learn)

### Quickstart

The instructions for this sample are in the form of a Lab. Follow along with them to get up and running.

## Demo / Lab

### Part 0 - Get the lab files and login to Azure

> 🎥 **Related Multimedia Session**:
> - ⚡ [**How Local Code Builds Azure Clouds**](https://www.youtube.com/shorts/BnkctVGCD8A) (`1:10`, 🇬🇧 English CC 20+) — *Learn how chaining VS Code, Azure CLI, and Terraform turns declarative code into cloud infrastructure.*


In this part we are going to get a local copy of the lab files for use in the rest of the lab.

1. Create a new root folder for the lab in a location of your choice.
1. Open a terminal and navigate to the new folder.
1. Run `git clone https://github.com/Azure-Samples/avm-terraform-labs` to clone the lab files into the new folder, they will be in a subfolder called `avm-terraform-labs`.

      ```pwsh
      git clone https://github.com/Azure-Samples/avm-terraform-labs
      mkdir avm-lab
      ```

      Your file structure should now look like this:

      ```plaintext
      📂my-lab-folder
      ┣ 📂avm-lab
      ┗ 📂avm-terraform-labs
      ```

1. Open Visual Studio Code.

      ```pwsh
      code .
      ```

1. Open the VSCode Terminal and navigate to the `avm-lab` folder.

      ```pwsh
      cd avm-lab
      ```

1. Run `az login` to login to your Azure subscription.
1. Run `az account show` to show the current subscription. Run `az account set --subscription <subscription-id>` to set the subscription if it is not the one you want to use.

### Part 1 - Base files and resources

> 🎥 **Related Multimedia Sessions**:
> - ⚡ [**How Azure Centralizes Cloud Monitoring**](https://www.youtube.com/shorts/oBkA9k32ECQ) (`1:14`, 🇬🇧 English CC 20+) — *How establishing Log Analytics upfront provides automated diagnostic logging for all downstream AVM modules.*
> - ⚡ [**How Terraform Deploys Azure Verified Modules**](https://www.youtube.com/shorts/EsIyH6PSGrE) (`1:10`, 🇬🇧 English CC 20+) — *Understanding the Terraform lifecycle (init, plan, apply, destroy) with AVM building blocks.*


In this part we are going to setup our Terraform root module and deploy an Azure Resource Group and Log Analytics Workspace ready for the rest of the lab. In this part we introduce our first Azure Verified Module, the `avm-res-log-analytics-workspace` module.

The Log Analytics Workspace is used as the target for diagnostic settings for all our other resources. This is where we are sending our logging telemetry.

1. Copy the files from the [part 1](labs/part01-base/) folder into the `avm-lab` folder.

      ```pwsh
      copy ../avm-terraform-labs/labs/part01-base/* .
      ```

      Your file structure should look like this:

      ```plaintext
      📂my-lab-folder
      ┣ 📂avm-lab
      ┃ ┣ 📜.gitignore
      ┃ ┣ 📜avm.log_analytics_workspace.tf
      ┃ ┣ 📜locals.tf
      ┃ ┣ 📜main.tf
      ┃ ┣ 📜outputs.tf
      ┃ ┣ 📜terraform.tf
      ┃ ┗ 📜variables.tf
      ┗ 📂avm-terraform-labs
      ```

1. Examine the `terraform` block in `terraform.tf` and note that we are referencing the `azurerm` and `random` providers.
1. Examine the `locals.tf`, `variables.tf`, `outputs.tf` and `main.tf` files.
1. Examine the `avm.log_analytics_workspace.tf` file and note the `source` and `version` properties.
1. Create an environment variable to set the location variable:

      ```pwsh
      $env:TF_VAR_location = "<azure region>"
      ```

      Replace `<azure region>` with a valid Azure location of your choice (e.g. swedencentral).

      ```pwsh
      $env:TF_VAR_location = "swedencentral"
      ```

1. Create a file called `terraform.tfvars` and add the following code to it:

      ```hcl
      tags = {
        type = "avm"
        env  = "demo"
      }
      ```

1. Run `terraform init` to initialize the Terraform configuration.
1. Run `terraform plan -out tfplan` to see what resources will be created and create a plan file.
1. Run `terraform apply tfplan` to create the resources based on the plan file.
1. If your run is successful, you will see:

      ```plaintext
      Apply complete! Resources: 6 added, 0 changed, 0 destroyed.
      ```

1. Take note of the outputs from the `terraform apply` command, they should look like this:

      ```plaintext
      Outputs:

      resource_ids = {
        "log_analytics_workspace" = "/subscriptions/b857908d-3f5c-4477-91c1-0fbd08df4e88/resourceGroups/rg-demo-dev-swedencentral-001/providers/Microsoft.OperationalInsights/workspaces/law-demo-dev-swedencentral-001"
        "resource_group" = "/subscriptions/b857908d-3f5c-4477-91c1-0fbd08df4e88/resourceGroups/rg-demo-dev-swedencentral-001"
      }
      resource_names = {
        "log_analytics_workspace_name" = "law-demo-dev-swedencentral-001"
        "resource_group_name" = "rg-demo-dev-swedencentral-001"
      }
      ```

1. Navigate to the Azure Portal and review the resources that have been created.
1. Run `git init -b main` to initialize a new git repository.
1. Run `git add .` to stage the files.
1. Run `git commit -m "Initial commit"` to commit the files.
1. If you are prompted to set up a git Author identity, follow the instructions and then re-run the `git commit` command.

    ```pwsh
    git config --global user.email "first.last@domain.com"
    git config --global user.name "First Last"
    ```

### Part 2 - Virtual network and subnets

> 🎥 **Related Multimedia Session**:
> - ⚡ [**How Azure Bastion Secures Virtual Machines**](https://www.youtube.com/shorts/QeVoCsTMBOQ) (`1:14`, 🇬🇧 English CC 20+) — *Zero-trust network isolation: accessing private workloads through Azure Bastion without public IPs.*


In this part we are going to add a virtual network and subnets to our Terraform configuration by leveraging the Azure Verified Module for Virtual Network. The Virtual Network is going to be used to provide private connectivity between and to our virtual machine, key vault and storage account.

>IMPORTANT: This lab is incremental, you must not delete any files from the previous lab (especially the `terraform.tfstate` file). You must copy the files from the next lab into the `avm-lab` folder and only replace the existing files when prompted.

1. Copy the files from the [part 2](labs/part02-vnet/) folder into the `avm-lab` folder. This will add some new files and replace some files.

      ```pwsh
      copy ../avm-terraform-labs/labs/part02-virtual-network/* .
      ```

      Your file structure should now look like this if you have followed the instructions correctly (this structure will continue to grow as you progress through the lab):

      ```plaintext
      📂my-lab-folder
      ┣ 📂avm-lab
      ┃ ┣ 📂.git (hidden)
      ┃ ┣ 📂.terraform
      ┃ ┣ 📜.gitignore
      ┃ ┣ 📜.terraform.lock.hcl
      ┃ ┣ 📜avm.log_analytics_workspace.tf
      ┃ ┣ 📜avm.nat_gateway.tf
      ┃ ┣ 📜avm.network_security_group.tf
      ┃ ┣ 📜avm.virtual_network.tf
      ┃ ┣ 📜locals.tf
      ┃ ┣ 📜main.tf
      ┃ ┣ 📜outputs.tf
      ┃ ┣ 📜terraform.tf
      ┃ ┣ 📜terraform.tfstate
      ┃ ┣ 📜terraform.tfvars
      ┃ ┣ 📜tfplan
      ┃ ┗ 📜variables.tf
      ┗ 📂avm-terraform-labs
      ```

1. Open your `terraform.tfvars` and update it with the following code:

      ```hcl
      address_space = "10.0.0.0/22"
      subnets = {
        AzureBastionSubnet = {
          size                       = 26
          has_nat_gateway            = false
          has_network_security_group = false
        }
        private_endpoints = {
          size                       = 28
          has_nat_gateway            = false
          has_network_security_group = true
        }
        virtual_machines = {
          size                       = 24
          has_nat_gateway            = true
          has_network_security_group = false
        }
      }
      tags = {
        type = "avm"
        env  = "demo"
      }
      ```

1. Run `terraform init` to install the AVM module for Virtual Networks and other new resources related to networking.
1. Navigate to the `Source Control` tab in Visual Studio Code and review the changes to the files.
1. Open the `avm.ip_addresses.tf` file and note the use of a utility module here, pay close attention to the `source` and `version` properties. A utility module is a helper module that doesn't deploy anything itself, but is used to calculate common values.
1. Open the `avm.virtual-network.tf` file and look at each of the properties, paying close attention to the `source` and `version` properties.
1. Examine the diagnostics settings in `locals.tf` and take note that this same setting will be applied to all of the AVM modules in the lab.
1. In order to find more detail about AVM modules, you can navigate to their documentation. For example, you can find the documentation for the Virtual Network module [here](https://registry.terraform.io/modules/Azure/avm-res-network-virtualnetwork/azurerm/latest). From there you can navigate to the source code and see the module's implementation [here](https://github.com/Azure/terraform-azurerm-avm-res-network-virtualnetwork).
1. Apply the changes with Terraform: `terraform apply -auto-approve`.
1. Review the deployed resources in the Azure Portal.
1. Commit the changes to git: `git add . && git commit -m "Add virtual network and subnets"`.

### Part 3 - Key Vault

> 🎥 **Related Multimedia Sessions**:
> - ⚡ [**How Azure Key Vault Secures Infrastructure**](https://www.youtube.com/shorts/-JlLcd-4CIs) (`1:14`, 🇬🇧 English CC 20+) — *Generating and storing VM SSH keys in Key Vault to eliminate plaintext secrets on local developer laptops.*
> - ⚡ [**How Azure Private Endpoints Lock Down Data**](https://www.youtube.com/shorts/xf5UNTUjYjY) (`1:18`, 🇬🇧 English CC 20+) — *Projecting Key Vault into private subnets using RFC 1918 private IPs and centralized Private DNS zones.*


In this part we are going to add a Key Vault to our Terraform configuration by leveraging the Azure Verified Module for Key Vault. The Key Vault is going to be used to store the customer managed key for our storage account and the SSH private key for our virtual machine.

1. Copy the files from the [part 3](labs/part03-keyvault/) folder into the `avm-lab` folder, remembering to retain the existing files and just add and overwrite when prompted.

      ```pwsh
      copy ../avm-terraform-labs/labs/part03-key-vault/* .
      ```

1. Run `terraform init` to install the AVM module for Key Vault.
1. Navigate to the `Source Control` tab in Visual Studio Code and review the changes to the files.
1. Open the `avm.key-vault.tf` file and look at each of the properties, paying close attention to the `private_endpoints` and `role_assignments` variables.
1. Apply the changes with Terraform: `terraform apply -auto-approve`.
1. Review the deployed resources in the Azure Portal.
1. Commit the changes to git: `git add . && git commit -m "Add key vault"`.

### Part 4 - Storage account

> 🎥 **Related Multimedia Sessions**:
> - ⚡ [**How Azure Verified Modules Automate CMK Encryption**](https://www.youtube.com/shorts/-Bo6tLrseDo) (`1:20`, 🇬🇧 English CC 20+) — *Automating Customer-Managed Key (CMK) encryption and Key Vault RBAC permission handshakes in one block.*
> - ⚡ [**How Managed Identities Kill Passwords**](https://www.youtube.com/shorts/2YlxRtiYll4) (`1:12`, 🇬🇧 English CC 20+) — *Replacing static storage account keys and connection strings with User-Assigned Managed Identities.*


In this part we are going to add a Storage Account to our Terraform configuration by leveraging the Azure Verified Module for Storage Account. The Storage Account is the main component of our demo lab and we will interact with it later on.

1. Copy the files from the [part 4](labs/part04-storage-account/) folder into the `avm-lab` folder, remembering to retain the existing files and just add and overwrite when prompted.

      ```pwsh
      copy ../avm-terraform-labs/labs/part04-storage-account/* .
      ```

1. Run `terraform init` to install the AVM module for Storage Account.
1. Navigate to the `Source Control` tab in Visual Studio Code and review the changes to the files.
1. Open the `avm.storage-account.tf` file and look at each of the properties, paying close attention to the `managed_identities`, `customer_managed_key` and `containers` variables.
1. Note in the source control diff that we are adding a key to the Key Vault using the AVM module and assigning permissions for the user assigned managed identity to access the key.
1. Apply the changes with Terraform: `terraform apply -auto-approve`.
1. Review the deployed resources in the Azure Portal.
1. Commit the changes to git: `git add . && git commit -m "Add storage account"`.

### Part 5 - Virtual machine and Bastion

> 🎥 **Related Multimedia Sessions**:
> - 📽️ [**Azure Verified Modules Lab: Complete Terraform End-to-End Walkthrough**](https://www.youtube.com/watch?v=I4s0A1uXEUg) (`7:02`, 🇬🇧 English CC 20+) — *Full architectural walkthrough of the entire 5-part lab from zero to complete deployment.*
> - ⚡ [**Deploying Secure Azure Architecture with Verified Modules**](https://www.youtube.com/shorts/xIkzOaSfB1c) (`1:16`, 🇬🇧 English CC 20+) — *Synthesizing modular AVM building blocks into a production-grade, zero-trust cloud foundation.*


In this part we are going to add a Virtual Machine to our Terraform configuration by leveraging the Azure Verified Module for Virtual Machine. The Virtual Machine is going to be used to interact with the Storage Account later. We are also going to add a role assignment to the storage module to assign permissions to the managed identity of the virtual machine to the storage container.

1. Copy the files from the [part 5](labs/part05-vm/) folder into the `avm-lab` folder, remembering to retain the existing files and just add an overwrite when prompted.

      ```pwsh
      copy ../avm-terraform-labs/labs/part05-virtual-machine/* .
      ```

1. Add the following variables to your `terraform.tfvars` file:

      >NOTE: You may need to choose a different virtual machine sku depending on availability in your chosen region. If you are running this lab in Skillable, SKUs are restricted to names beginning with `Standard_B2*` or `Standard_D2*` only.

      ```hcl
      virtual_machine_sku = "Standard_D2s_v4"
      virtual_machine_image = {
        publisher = "Canonical"
        offer     = "0001-com-ubuntu-server-jammy"
        sku       = "22_04-lts-gen2"
        version   = "latest"
      }
      ```

1. Run `terraform init` to install the AVM modules for Virtual Machine and Role Assignments.
1. Apply the changes with Terraform. NOTE: We are applying this now, because the bastion can take a few minutes to deploy.
1. Navigate to the `Source Control` tab in Visual Studio Code and review the changes to the files.
1. Open the `avm.virtual-machine.tf` file and look at each of the properties, paying close attention to the `generated_secrets_key_vault_secret_config` and `network_interfaces` variables.
1. Apply the changes with Terraform: `terraform apply -auto-approve`.
1. Review the deployed resources in the Azure Portal.
1. Commit the changes to git: `git add . && git commit -m "Add virtual machine and bastion"`.

### Part 6 - Connect to the VM via Bastion

In this part we are going to connect to the virtual machine via the Azure Bastion service using the SSH private key stored in the Key Vault.

1. Open the Azure Portal and navigate to the VM.
1. Click on the `Connect` button and select `Bastion`.
1. Choose `SSH Private Key from Azure Key Vault` in the `Authentication Type` dropdown.
1. Enter `azureuser` in the `Username` field.
1. Select you subscription from the `Subscription` drop down.
1. Select the Key Vault you created in the lab in the `Azure Key Vault` drop down.
1. Select the secret you created in the lab in the `Azure Key Vault Secret` drop down.
1. Click `Connect`. You may see a pop-up blocked message, click on the pop-up blocked icon in the address bar and select `Always allow pop-ups and redirects from https://portal.azure.com`.
1. A new browser window will open with a terminal session to the VM.

### Part 7 - Install the Azure CLI and login

> 🎥 **Related Multimedia Session**:
> - ⚡ [**How Azure VMs Access Storage Without Passwords**](https://www.youtube.com/shorts/jwASueLUzhI) (`1:18`, 🇬🇧 English CC 20+) — *Authenticating directly with Entra ID via `az login --identity` using the VM System-Assigned Managed Identity.*


We are going to install the Azure CLI and login with the system assigned managed identity of the VM from the Azure Bastion SSH terminal.

1. Run `curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash` to install the Azure CLI.
1. Run `az login --identity` to login with the system assigned managed identity.

### Part 8 - Create a blob in the storage account

We are going to create a blob in the storage account using the Azure CLI form the Azure Bastion SSH terminal.

1. Run `echo "hello world" > hello.txt` to create a file with some content.
1. Run `az storage blob upload --account-name <storage-account-name> --container-name demo --file hello.txt --name hello.txt --auth-mode login` to upload the file to the storage account.
1. Run `az storage blob list --account-name <storage-account-name> --container-name demo --auth-mode login` to list the blobs in the container.
1. Run `az storage blob download --account-name <storage-account-name> --container-name demo --name hello.txt --file hello2.txt --auth-mode login` to download the blob to a new file.
1. Run `cat hello2.txt` to view the contents of the downloaded file.

      Here are the commands to run, so you can copy to notepad and replace the placeholder with the storage account name you created in the lab. Then run the commands in the terminal:

      ```bash
      echo "hello world" > hello.txt
      az storage blob upload --account-name replace_me --container-name demo --file hello.txt --name hello.txt --auth-mode login
      az storage blob list --account-name replace_me --container-name demo --auth-mode login
      az storage blob download --account-name replace_me --container-name demo --name hello.txt --file hello2.txt --auth-mode login
      cat hello2.txt
      ```

### Clean up

Finally we will clean up everything we have created in the lab.

1. Run `terraform destroy` from the Visual Studio Code terminal to remove the resources created by Terraform.
1. When prompted type `yes` and press `Enter` to confirm the destruction.
1. Run `$env:TF_VAR_location = $null` to remove the location environment variable.

## Resources

* AVM Documentation: [Azure Verified Modules](https://aka.ms/avm)
