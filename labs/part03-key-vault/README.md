# Lab Part 3: Azure Key Vault & Private DNS

> 🧭 **Navigation**: [⬅️ Previous: Part 2 - Virtual Network](../part02-virtual-network/README.md) | [🏠 Main Lab Guide](../../README.md) | [➡️ Next: Part 4 - Storage Account](../part04-storage-account/README.md)

> 🎥 **Related Multimedia Sessions**:
> - ⚡ [**How Azure Key Vault Secures Infrastructure**](https://www.youtube.com/shorts/-JlLcd-4CIs) (`1:14`, 🇬🇧 English CC 20+) — *Generating and storing VM SSH keys in Key Vault to eliminate plaintext secrets on local developer laptops.*
> - ⚡ [**How Azure Private Endpoints Lock Down Data**](https://www.youtube.com/shorts/xf5UNTUjYjY) (`1:18`, 🇬🇧 English CC 20+) — *Projecting Key Vault into private subnets using RFC 1918 private IPs and centralized Private DNS zones.*

---

## Overview

In Part 3, you introduce enterprise secret management and private name resolution:
- An **Azure Key Vault** deployed via `avm-res-keyvault-vault` with Azure RBAC authorization enabled.
- A **Private Endpoint** projecting the Key Vault into the private `subnet-pe` subnet.
- A **Private DNS Zone** (`privatelink.vaultcore.azure.net`) linked to the virtual network for seamless split-brain DNS resolution.
- An **SSH Key Pair** generated directly in the cloud and stored securely in Key Vault without local key file leaks.

## Deployed AVM Modules

| Module Name | Source | Purpose |
|---|---|---|
| `key_vault` | `Azure/avm-res-keyvault-vault/azurerm` | Secure secret and cryptographic key management |
| `private_dns` | `Azure/avm-res-network-privatednszone/azurerm` | Private DNS zone for Key Vault Private Link resolution |

## Key Security Features

- **RBAC-Based Access**: Uses modern Azure Key Vault RBAC permissions rather than legacy access policies.
- **Private Link Only**: Key Vault disables public network access, restricting access to private endpoints.
- **Automated SSH Generation**: Generates TLS private keys dynamically and stores them as Key Vault secrets.
