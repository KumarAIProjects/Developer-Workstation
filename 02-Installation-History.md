# Installation History

## Purpose

This document records the installation and configuration history of the Developer Workstation, including issues encountered and how they were resolved.

---

# Phase 1 - Core Development Environment

## Visual Studio Code

### Status

* Installed successfully.
* Signed in using GitHub account.

### Verification

* VS Code launched successfully.
* Integrated terminal working correctly.

---

## Git

### Status

* Installed Git for Windows.

### Installation Options

* Git Credential Manager enabled.
* Symbolic Links enabled.

### Configuration

Configured:

* User Name
* GitHub Email
* Default branch (`main`)
* Visual Studio Code as Git editor

### Verification

Verified using:

```powershell
git --version
git config --list
```

---

## .NET SDK

### Status

Installed:

* .NET SDK 8.0.422

Installed Runtimes:

* ASP.NET Core Runtime 8.0.28
* .NET Runtime 8.0.28
* Windows Desktop Runtime 8.0.28

### Issue Encountered

Initially downloaded the compressed ZIP package instead of the Windows installer.

### Resolution

Downloaded and installed the official .NET SDK installer.

### Verification

```powershell
dotnet --version
dotnet --list-sdks
dotnet --list-runtimes
```

---

## Python

### Status

Installed:

* Python 3.13.14
* Python Launcher
* pip

### Issue Encountered

The `py` command worked, but the `python` command was not recognized because Python was not added correctly to the system PATH.

### Resolution

Re-ran the Python installer and enabled the option to add Python to the system PATH.

### Verification

```powershell
python --version
py --version
pip --version
where.exe python
where.exe py
```

---

## Node.js

### Status

Installed:

* Node.js 24.18.0
* npm 11.16.0

### Issue Encountered

PowerShell blocked npm execution due to the execution policy.

### Resolution

Executed:

```powershell
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

### Verification

```powershell
node --version
npm --version
```

---

# Phase 2 - VS Code Extensions

Installed the following extensions:

* C# Dev Kit
* Python
* Markdown All in One
* GitLens
* Error Lens
* EditorConfig

---

# Phase 3 - Git & GitHub

Completed:

* Configured Git user information.
* Created GitHub repository.
* Initialized local Git repository.
* Added GitHub remote (`origin`).
* Created the first commit.
* Successfully pushed the repository to GitHub.

---
# Phase 4 - Windows Subsystem for Linux (WSL 2)

### Status

Installed:

* Windows Subsystem for Linux (WSL) 2
* Linux Kernel 6.18.33.2-2

### Verification

Verified using:

```powershell
wsl --version
```

Confirmed:

* WSL Version: 2.7.10.0
* Linux Kernel: 6.18.33.2-2

---
# Phase 5 - Docker Desktop

### Status

Installed:

* Docker Desktop 29.6.1
* Docker Engine
* Docker Compose (built-in)

### Issue Encountered

After installation, Docker commands returned the following error when attempting to run a container:

```text
request returned 500 Internal Server Error for API route and version ...
```

This indicated that Docker Desktop could not communicate with the Docker Engine running on the WSL 2 backend.

### Resolution

Restarted the WSL environment by executing:

```powershell
wsl --shutdown
```

Restarted Docker Desktop and verified that the Docker Engine started successfully.

### Verification

Verified using:

```powershell
docker --version
docker compose version
docker run hello-world
docker run -it ubuntu bash
```

Successful verification confirmed:

* Docker Engine is running correctly.
* Docker Compose is available.
* Docker can pull images from Docker Hub.
* Linux containers execute successfully.

---

---

## PowerShell 7

### Status

Installed:

* PowerShell 7.6.3

### Verification

```powershell
pwsh --version
$PSVersionTable.PSVersion
```

---

## Windows Terminal

### Status

Windows Terminal was already installed on Windows 11.

### Configuration

Configured Visual Studio Code to use PowerShell 7 as the default integrated terminal.

### Verification

Verified by opening a new terminal in Visual Studio Code and confirming:

```powershell
$PSVersionTable.PSVersion
```
---

## GitHub CLI

### Status

Installed GitHub CLI.

### Authentication

Successfully authenticated with GitHub using HTTPS and browser-based login.

### Verification

```powershell
gh --version
gh auth status

```
| Date | Tool | Version | Status | Remarks |
|------|------|---------|--------|---------|
| 06-Jul-2026 | UV | 0.11.26 | ✅ Installed | Required for GitHub Spec Kit |

```

# Lessons Learned

* Always verify software installation using version commands.
* Download installers instead of compressed archives when appropriate.
* Configure Git before making the first commit.
* Keep documentation updated as the workstation evolves.
* Commit meaningful changes with descriptive commit messages.

---

# Current Status

The workstation is successfully configured with:

* Core development tools
* Programming languages
* Version control
* GitHub integration
* Professional VS Code extensions
* WSL 2
* Docker Desktop
* PowerShell 7
* Windows Terminal
* GitHub CLI

The workstation is ready for the next phase:

* VS Code Workspace
* GitHub Spec Kit
* Spec-Driven Development projects
    