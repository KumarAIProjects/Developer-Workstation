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

# Lessons Learned

* Always verify software installation using version commands.
* Download installers instead of compressed archives when appropriate.
* Configure Git before making the first commit.
* Keep documentation updated as the workstation evolves.
* Commit meaningful changes with descriptive commit messages.

---

# Current Status

The Developer Workstation is successfully configured with:

* Core development tools
* Programming languages
* Version control
* GitHub integration
* Professional VS Code extensions

The workstation is ready for the next phase:

* Docker Desktop
* VS Code Workspace
* GitHub Spec Kit
* Spec-Driven Development projects
    