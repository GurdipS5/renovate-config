# 🧰 renovate-config

> **Centralized configuration for [Mend Renovate](https://www.mend.io/free-developer-tools/renovate/)** — used to manage dependency updates across all `gssira` GitHub repositories.

---

### 📊 Status & Metadata

![Renovate](https://img.shields.io/badge/Renovate-enabled-brightgreen?logo=renovatebot)
![GitHub](https://img.shields.io/badge/Config-hosted_on_GitHub-blue?logo=github)
![License](https://img.shields.io/badge/license-MIT-green)
![Timezone](https://img.shields.io/badge/timezone-Europe%2FLondon-blue)
![Platform](https://img.shields.io/badge/platform-GitHub-darkgreen)

---

## 🧩 Overview

This repository defines **shared Renovate configuration presets** used across the `gssira` organization.  
It ensures consistent dependency management, automated PR handling, and unified update policies for:

- ⚙️ **Terraform modules & providers**
- 🪶 **.NET / NuGet dependencies**
- 🐳 **Docker base images**
- 🧱 **Frontend (Node.js / npm / yarn)**
- 🧰 **GitHub Actions workflows**

Each project simply **extends** one of the presets defined here — keeping configs clean, consistent, and DRY.

---

## 📂 Preset Configurations

| Preset File | Purpose | Example Extend Syntax |
|--------------|----------|------------------------|
| 🏗️ `default.json` | Base config (used by all) | `"extends": ["github>gssira/renovate-config:default.json"]` |
| ⚙️ `dotnet.json` | For .NET / NuGet projects | `"extends": ["github>gssira/renovate-config:dotnet.json"]` |
| ☁️ `terraform.json` | For Terraform infrastructure | `"extends": ["github>gssira/renovate-config:terraform.json"]` |
| 🐳 `docker.json` | For Docker images / containers | `"extends": ["github>gssira/renovate-config:docker.json"]` |
| 🖥️ `frontend.json` | For web / JavaScript projects | `"extends": ["github>gssira/renovate-config:frontend.json"]` |

---

## 🚀 How to Use

### 1️⃣ Add to your repository
Create a `renovate.json` in the root of your project repo:

```json
{
  "extends": ["github>gssira/renovate-config:dotnet.json"]
}
