# meddev-reg-path-checker

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Domain Profile](https://img.shields.io/badge/domain-meddev-blue.svg)](domain.manifest.json)
[![Status: RESERVED](https://img.shields.io/badge/status-RESERVED-orange.svg)](domain.manifest.json)
[![MCP Checker](https://img.shields.io/badge/checker-MCP%20tool-8a2be2.svg)](checker.io.json)

> **Status: RESERVED (placeholder · open for claiming)** — This repo holds the four-piece industry-access skeleton for the medical-device registration/filing route domain (reference domain).

We break "which class is this product, and which route should it take?" into verifiable attributes, so AI only suggests paths and never classifies or grants clearance.

**Keywords**: medical device classification · registration and filing route · UDI · domain profile · MCP checker

## Quick Start

This repo is a **domain configuration pack** (not a runnable SDK).

```bash
git clone https://github.com/SynomosAI/meddev-reg-path-checker.git
cd meddev-reg-path-checker
cat domain.manifest.json
cat checker.io.json
```

```bash
cat gate-map.json
cat privacy.json
```

## What this domain covers

Medical device classification and registration/filing route determination.

Devices are classified by risk into three classes: class I requires filing, classes II/III require registration. AI can lay out the classification factors and current license status; classification and registration authority always stays with the drug administration.

## Domain identity

| Item | Value |
|---|---|
| Domain ID | `meddev` |
| Domain name | Medical Device · Registration and Filing Route (reference domain) |
| Profile version | `domain/1.0` |
| Current status | `RESERVED` |

## Attribute list

| Attribute key | Type | Description |
|---|---|---|
| `meddev.device_class` | enum | Risk class per device classification rules · class_i/class_ii/class_iii/unclassified |
| `meddev.reg_path` | enum | Filing/registration/innovative/emergency/exempt/undetermined |
| `meddev.reg_status` | enum | Certificate/filing status per regulator · not_required/filed/approved/pending/expired/rejected |
| `meddev.license_scope` | string | Production/business license scope |
| `meddev.udi_status` | enum | UDI assignment · assigned/pending/not_required/unknown |

## Red lines (machine-readable)

1. Device class follows the regulator's classification determination; AI must not self-classify.
2. No "can launch" / "can sell" wording; certificate/filing record is the only basis.
3. No advice to evade registration by splitting kits, changing intended use, or lowering class.

## License

Code and configuration are under MIT. Prose content copyrights belong to SynomosAI.

© 2026 SynomosAI. All rights reserved.
