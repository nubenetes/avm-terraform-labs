# Lab Part 5: Virtual Machine, Bastion & Passwordless Workload Access

> 🧭 **Navigation**: [⬅️ Previous: Part 4 - Storage Account](../part04-storage-account/README.md) | [🏠 Main Lab Guide](../../README.md)

> 🎥 **Related Multimedia Sessions**:
> - 📽️ [**Azure Verified Modules Lab: Complete Terraform End-to-End Walkthrough**](https://www.youtube.com/watch?v=I4s0A1uXEUg) (`7:02`, 🇬🇧 English CC 20+) — *Full architectural walkthrough of the entire 5-part lab from zero to complete deployment.*
> - ⚡ [**Deploying Secure Azure Architecture with Verified Modules**](https://www.youtube.com/shorts/xIkzOaSfB1c) (`1:16`, 🇬🇧 English CC 20+) — *Synthesizing modular AVM building blocks into a production-grade, zero-trust cloud foundation.*
> - ⚡ [**How Azure Bastion Secures Virtual Machines**](https://www.youtube.com/shorts/QeVoCsTMBOQ) (`1:14`, 🇬🇧 English CC 20+) — *Zero-trust network isolation: accessing private workloads through Azure Bastion without public IPs.*
> - ⚡ [**How Azure VMs Access Storage Without Passwords**](https://www.youtube.com/shorts/jwASueLUzhI) (`1:18`, 🇬🇧 English CC 20+) — *Authenticating directly with Entra ID via `az login --identity` using the VM System-Assigned Managed Identity.*

---

## Overview

In Part 5, you complete the end-to-end architecture by deploying the compute layer and private remote access:
- An **Azure Linux Virtual Machine (Ubuntu 22.04 LTS)** deployed without public IP addresses inside `subnet-vm`.
- An **Azure Bastion Host** deployed inside `AzureBastionSubnet` to provide browser-based SSH access.
- A **System-Assigned Managed Identity** attached to the VM, automatically granted `Storage Blob Data Contributor` permissions on the demo blob container.
- Remote login using the SSH private key stored securely in Key Vault.

## Deployed AVM Modules

| Module Name | Source | Purpose |
|---|---|---|
| `virtual_machine` | `Azure/avm-res-compute-virtualmachine/azurerm` | Linux VM with managed identity, private NIC, and Key Vault SSH secrets |
| `bastion_host` | `Azure/avm-res-network-bastionhost/azurerm` | Secure browser-based TLS proxy for SSH management without public IPs |
| `public_ip` | `Azure/avm-res-network-publicipaddress/azurerm` | Public IP allocated to Azure Bastion Host |

## Verifying Passwordless Data Plane Access (Parts 6–8)

1. Connect to the VM via Azure Bastion using the SSH key from Key Vault.
2. Inside the Bastion terminal, authenticate using the VM identity:
   ```bash
   az login --identity
   ```
3. Upload and download blobs without passwords:
   ```bash
   echo "hello world" > hello.txt
   az storage blob upload --account-name <storage-account-name> --container-name demo --file hello.txt --name hello.txt --auth-mode login
   az storage blob list --account-name <storage-account-name> --container-name demo --auth-mode login
   ```
