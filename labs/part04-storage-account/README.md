# Lab Part 4: Azure Storage Account with Customer-Managed Keys (CMK)

> 🧭 **Navigation**: [⬅️ Previous: Part 3 - Key Vault](../part03-key-vault/README.md) | [🏠 Main Lab Guide](../../README.md) | [➡️ Next: Part 5 - Virtual Machine](../part05-virtual-machine/README.md)

> 🎥 **Related Multimedia Sessions**:
> - ⚡ [**How Azure Verified Modules Automate CMK Encryption**](https://www.youtube.com/shorts/-Bo6tLrseDo) (`1:20`, 🇬🇧 English CC 20+) — *Automating Customer-Managed Key (CMK) encryption and Key Vault RBAC permission handshakes in one block.*
> - ⚡ [**How Managed Identities Kill Passwords**](https://www.youtube.com/shorts/2YlxRtiYll4) (`1:12`, 🇬🇧 English CC 20+) — *Replacing static storage account keys and connection strings with User-Assigned Managed Identities.*

---

## Overview

In Part 4, you deploy a highly secure, enterprise-grade storage account:
- An **Azure Storage Account** with Customer-Managed Key (CMK) encryption enabled at rest.
- A **User-Assigned Managed Identity** dedicated to storage encryption with scoped Key Vault Crypto Service Encryption User permissions.
- A **Private Endpoint** and Private DNS Zone (`privatelink.blob.core.windows.net`) restricting blob access to private network routes.
- A baseline blob container named `demo` configured for passwordless application access.

## Deployed AVM Modules

| Module Name | Source | Purpose |
|---|---|---|
| `storage_account` | `Azure/avm-res-storage-storageaccount/azurerm` | Enterprise blob storage with CMK encryption and private endpoints |
| `user_assigned_identity` | `Azure/avm-res-managedidentity-userassignedidentity/azurerm` | Dedicated identity for Key Vault CMK encryption handshake |
| `private_dns` | `Azure/avm-res-network-privatednszone/azurerm` | Private DNS zone for Storage Blob Private Link resolution |

## Key Takeaways

- **Automated CMK Handshake**: The AVM module orchestrates the identity, Key Vault key reference, and crypto role assignment in a single declarative block.
- **Zero Shared Access Keys**: Storage account disables access keys (`shared_access_key_enabled = false`), enforcing Entra ID authentication.
