
````markdown
# 🚀 Codespace Remote Dev Env (.NET 8) – 20250709

[![Status](https://img.shields.io/badge/Status-Completed-brightgreen)](https://github.com/)
[![Built With](https://img.shields.io/badge/Stack-C%23%20%7C%20.NET%208%20%7C%20Codespaces-blue)](https://learn.microsoft.com/)
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)
[![MSSA](https://img.shields.io/badge/MSSA-Cloud%20Application%20Development-green)](https://military.microsoft.com/)

> **Mission**: Stand up a cloud-powered, containerized development environment using GitHub Codespaces for consistent, fast, and collaborative .NET 8 development.

---

## 📌 Project Overview

This project showcases a hands-on implementation of GitHub Codespaces for remote .NET 8 development using Visual Studio Code. The Codespace was configured with a `.devcontainer.json` file for custom tooling and ran a minimal Web API with a `/weatherforecast` and `/health` endpoint.

---

## 🎯 MVP Goal

**What It Does**:  
Provisioned a remote development environment in GitHub Codespaces using .NET 8 and C#, with custom dev tools, and verified successful deployment of a simple API including a health check.

---

## 🔧 Tech Stack

| Layer       | Technology                              |
|-------------|------------------------------------------|
| Backend     | ASP.NET Core Web API (.NET 8)            |
| Tools       | GitHub Codespaces, VS Code in-browser    |
| Extensions  | C# for VS Code, GitHub Copilot           |
| Container   | Dev Container defined via `.devcontainer.json` |
| Hosting     | Forwarded port via Codespaces             |

---

## 🛠️ How to Run

### ✅ Prerequisites
- GitHub Codespaces enabled
- GitHub repo access
- Browser + GitHub login

### ▶️ Steps

1. Open the repo in GitHub.
2. Click `Code > Codespaces > Create codespace on main`.
3. Wait for the container to build and dependencies to install.
4. Run the API:

   ```bash
   dotnet run
````

5. Visit the forwarded port (e.g., `https://<your-codespace-id>.github.dev`).

6. Test endpoints:

   * `GET /` → "API is running..."
   * `GET /weatherforecast`
   * `GET /health` → "Healthy"

---

## 📦 devcontainer.json Example

```json
{
  "image": "mcr.microsoft.com/vscode/devcontainers/dotnet:8.0",
  "postCreateCommand": "dotnet tool restore",
  "customizations": {
    "vscode": {
      "extensions": [
        "ms-dotnettools.csharp",
        "GitHub.copilot"
      ]
    }
  }
}
```

---

## 🧠 Learning Objectives

* Automate development environment provisioning via Codespaces
* Work in feature branches and merge to main using Git
* Customize containerized environments for team consistency
* Validate .NET 8 APIs in the cloud using forwarded ports
* Use health check endpoints for runtime verification

---

## ✅ Git Branch Flow

```bash
git checkout -b feature/add-healthcheck-endpoint
# work...
git add .
git commit -m "Add healthcheck endpoint"
git push origin feature/add-healthcheck-endpoint

# merge to main
git checkout main
git pull origin main
git merge feature/add-healthcheck-endpoint
git push origin main

# delete old branch
git branch -d feature/add-healthcheck-endpoint
```

---

## 👥 Credits

* **Developer**: Anaizat Hereim (MSSA Cohort 19)
* **Mentor**: Marcin, MSSA Team

