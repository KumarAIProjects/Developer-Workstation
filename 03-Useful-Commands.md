# Useful Commands

This document contains commonly used commands for managing the Developer Workstation.

---

# Git

## Check Installation

```powershell
git --version
git config --list
```

## Repository Status

```powershell
git status
git log --oneline
git log
```

## Stage Changes

```powershell
git add .
git add <filename>
```

## Commit Changes

```powershell
git commit -m "Commit message"
```

## Push & Pull

```powershell
git push
git pull
```

## Repository Information

```powershell
git remote -v
git branch
```

---

# .NET

## Verify Installation

```powershell
dotnet --version
dotnet --list-sdks
dotnet --list-runtimes
```

## Create Projects

```powershell
dotnet new console
dotnet new webapi
dotnet new mvc
```

## Build & Run

```powershell
dotnet restore
dotnet build
dotnet run
```

---

# Python

## Verify Installation

```powershell
python --version
py --version
pip --version
```

## Package Management

```powershell
pip install <package>
pip list
pip freeze
```

## Virtual Environment

```powershell
python -m venv .venv
.venv\Scripts\activate
deactivate
```

---

# Node.js

## Verify Installation

```powershell
node --version
npm --version
```

## Package Management

```powershell
npm install
npm install <package>
npm update
npm list
```

## Project Commands

```powershell
npm init
npm run dev
npm start
```

---

---

# Windows Subsystem for Linux (WSL)

## Verify Installation

```powershell
wsl --version
wsl --list --verbose
```

## Manage WSL

```powershell
wsl
wsl --shutdown
```
---

# Docker

## Verify Installation

```powershell
docker --version
docker compose version
docker info
```

## Images

```powershell
docker images
docker pull <image-name>
```

## Containers

```powershell
docker ps
docker ps -a
docker run hello-world
docker run -it ubuntu bash
docker stop <container-id>
docker rm <container-id>
```

## Docker Compose

```powershell
docker compose version
docker compose up
docker compose down
```

# Visual Studio Code

## Open Current Folder

```powershell
code .
```

## Open Current Workspace

```powershell
code <workspace-name>.code-workspace
```

---

# Windows

## Current Folder

```powershell
pwd
Get-Location
```

## List Files

```powershell
dir
ls
```

## System Information

```powershell
systeminfo
```

## Find Executables

```powershell
where.exe git
where.exe python
where.exe node
```

---

# GitHub Workflow

```text
Edit Files
    ↓
git status
    ↓
git add .
    ↓
git commit -m "Meaningful message"
    ↓
git push
```

---

# Verification Checklist

Use these commands after installing new software:

```powershell
git --version
dotnet --version
python --version
pip --version
node --version
npm --version
wsl --version
docker --version
docker compose --version

```
