# Lab Part 2: Virtual Network, Subnets & NAT Gateway

> 🧭 **Navigation**: [⬅️ Previous: Part 1 - Base](../part01-base/README.md) | [🏠 Main Lab Guide](../../README.md) | [➡️ Next: Part 3 - Key Vault](../part03-key-vault/README.md)

> 🎥 **Related Multimedia Sessions**:
> - ⚡ [**How Azure Bastion Secures Virtual Machines**](https://www.youtube.com/shorts/QeVoCsTMBOQ) (`1:14`, 🇬🇧 English CC 20+) — *Zero-trust network isolation: accessing private workloads through Azure Bastion without public IPs.*
> - ⚡ [**How Azure Private Endpoints Lock Down Data**](https://www.youtube.com/shorts/xf5UNTUjYjY) (`1:18`, 🇬🇧 English CC 20+) — *Projecting PaaS services into private subnets using RFC 1918 private IPs and centralized Private DNS zones.*

---

## Overview

In Part 2, you establish the core network infrastructure required for zero-trust compute and private data access:
- A **Virtual Network (VNet)** partitioned into dedicated subnets (`AzureBastionSubnet`, `subnet-vm`, `subnet-pe`).
- A **NAT Gateway** with a public IP for secure, outbound-only internet connectivity.
- A **Network Security Group (NSG)** associated with workload subnets to restrict lateral movement.

## Deployed AVM Modules

| Module Name | Source | Purpose |
|---|---|---|
| `virtual_network` | `Azure/avm-res-network-virtualnetwork/azurerm` | Core VNet and subnet partitioning |
| `nat_gateway` | `Azure/avm-res-network-natgateway/azurerm` | Secure outbound egress for private subnets |
| `network_security_group` | `Azure/avm-res-network-networksecuritygroup/azurerm` | L4 stateful firewall rules restricting subnet traffic |
| `public_ip` | `Azure/avm-res-network-publicipaddress/azurerm` | Static public IP address allocated to the NAT Gateway |

## File Structure

```plaintext
labs/part02-virtual-network/
├── avm.ip_addresses.tf           # Public IP for NAT Gateway
├── avm.log_analytics_workspace.tf# Centralized logging sink (from Part 1)
├── avm.nat_gateway.tf            # AVM NAT Gateway module
├── avm.network_security_group.tf # AVM NSG with security rules
├── avm.virtual_network.tf        # AVM VNet with subnet definitions
├── locals.tf                     # Subnet addressing and IP allocations
├── main.tf                       # Resource group definition
├── outputs.tf                    # VNet and Subnet ID outputs
├── terraform.tf                  # Provider requirements
└── variables.tf                  # Network configuration variables
```
