# Installation History

## Purpose

This document records the installation history of the Developer Workstation, including issues encountered and how they were resolved.

---

# Session 1 – Visual Studio Code & Git

## Visual Studio Code

### Installed

- Visual Studio Code 1.126.x

### Verification

- VS Code launched successfully.
- Signed in using GitHub account.

---

## Git

### Installed

- Git for Windows

### Installation Options Selected

- Git Credential Manager enabled.
- Symbolic Links enabled.

### Issue

The `git` command was initially not recognized in PowerShell.

### Resolution

- Reinstalled Git.
- Verified PATH configuration.

### Verification

```powershell
git --version
git config --list
```

---

# Session 2 – .NET SDK

## Installed

- .NET SDK 8.0.422

### Issue

Initially downloaded the ZIP package instead of the installer.

### Resolution

Downloaded the official Windows installer and completed the installation.

### Verification

```powershell
dotnet --version
dotnet --list-sdks
dotnet --list-runtimes
```

---

# Session 3 – Python

## Installed

- Python 3.13.14
- Python Launcher
- pip

### Issue

`py` command worked, but `python` command was not recognized.

### Resolution

- Re-ran the Python installer using **Modify**.
- Added Python to the system PATH.

### Verification

```powershell
python --version
py --version
pip --version
where.exe python
where.exe py
```

---

# Session 4 – Node.js

## Installed

- Node.js 24.18.0
- npm 11.16.0

### Issue 1

`node` command was initially not recognized.

### Resolution

Restarted the terminal after installation.

### Issue 2

PowerShell blocked npm execution.

Error:

```
running scripts is disabled on this system
```

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

# Session 5 – VS Code Extensions

Installed the following extensions:

- ✅ C# Dev Kit (Microsoft)
- ✅ Python (Microsoft)
- ✅ Markdown All in One (Yu Zhang)
- ✅ GitLens (GitKraken)
- ✅ Error Lens (Alexander)
- ✅ EditorConfig (EditorConfig)

---

# Current Status

## Core Development Environment

- ✅ Visual Studio Code
- ✅ Git
- ✅ .NET SDK
- ✅ Python
- ✅ Node.js

## VS Code Extensions

- ✅ C# Dev Kit
- ✅ Python
- ✅ Markdown All in One
- ✅ GitLens
- ✅ Error Lens
- ✅ EditorConfig

---

# Next Phase

- Git & GitHub
- VS Code Workspace
- GitHub Spec Kit
- Sample Project 1