# Lab Part 1: Base Files & Log Analytics Workspace

> 🧭 **Navigation**: [🏠 Main Lab Guide](../../README.md) | [➡️ Next: Part 2 - Virtual Network](../part02-virtual-network/README.md)

> 🎥 **Related Multimedia Sessions**:
> - ⚡ [**How Azure Centralizes Cloud Monitoring**](https://www.youtube.com/shorts/oBkA9k32ECQ) (`1:14`, 🇬🇧 English CC 20+) — *How establishing Log Analytics upfront provides automated diagnostic logging for all downstream AVM modules.*
> - ⚡ [**How Terraform Deploys Azure Verified Modules**](https://www.youtube.com/shorts/EsIyH6PSGrE) (`1:10`, 🇬🇧 English CC 20+) — *Understanding the Terraform lifecycle (init, plan, apply, destroy) with AVM building blocks.*
> - ⚡ [**How Local Code Builds Azure Clouds**](https://www.youtube.com/shorts/BnkctVGCD8A) (`1:10`, 🇬🇧 English CC 20+) — *Chaining VS Code, Azure CLI, and Terraform CLI to turn declarative code into cloud infrastructure.*

---

## Overview

In Part 1, you establish the Terraform root module foundation and deploy the core operational baseline for the entire architecture:
- An **Azure Resource Group** to contain all lab assets.
- A **Log Analytics Workspace** deployed using the official Azure Verified Module (`avm-res-log-analytics-workspace`).

The Log Analytics Workspace serves as the central diagnostic sink for all subsequent resources deployed in Parts 2 through 5.

## Deployed AVM Modules

| Module Name | Source | Purpose |
|---|---|---|
| `log_analytics_workspace` | `Azure/avm-res-operationalinsights-workspace/azurerm` | Centralized telemetry, logging, and operational analytics sink |

## File Structure

```plaintext
labs/part01-base/
├── avm.log_analytics_workspace.tf # AVM Log Analytics module configuration
├── locals.tf                      # Resource naming and tagging conventions
├── main.tf                        # Resource group definition
├── outputs.tf                     # Exported workspace ID and resource group name
├── terraform.tf                   # Required Terraform and AzureRM providers
└── variables.tf                   # Input variables (location, naming prefixes)
```

## How to Deploy

```bash
# 1. Set your target Azure region
export TF_VAR_location="eastus2"

# 2. Initialize Terraform and download AVM modules
terraform init

# 3. Review the speculative plan
terraform plan

# 4. Apply the base infrastructure
terraform apply -auto-approve
```
