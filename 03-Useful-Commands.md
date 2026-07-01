# Useful Commands

This document contains frequently used commands for software development.

---

# Git

## Display Git Version

```powershell
git --version
```

Displays the installed Git version.

---

## Display Git Configuration

```powershell
git config --list
```

Displays the current Git configuration.

---

## Check Repository Status

```powershell
git status
```

Shows the current status of the Git repository.

Example:
- Modified files
- New files
- Deleted files
- Files waiting to be committed

---

## Display Commit History

```powershell
git log
```

Displays the complete commit history.

---

# .NET

## Display .NET SDK Version

```powershell
dotnet --version
```

Displays the installed .NET SDK version.

---

## Display Installed SDKs

```powershell
dotnet --list-sdks
```

Lists all installed .NET SDK versions.

---

## Display Installed Runtimes

```powershell
dotnet --list-runtimes
```

Lists all installed .NET runtimes.

---

# Python

## Display Python Version

```powershell
python --version
```

Displays the installed Python version.

---

## Display Python Launcher Version

```powershell
py --version
```

Displays the installed Python Launcher version.

---

## Display pip Version

```powershell
pip --version
```

Displays the installed pip version.

---

## Display Python Executable

```powershell
where.exe python
```

Displays the location of the Python executable.

---

## Display Python Launcher Location

```powershell
where.exe py
```

Displays the location of the Python Launcher.

---

# Node.js

## Display Node.js Version

```powershell
node --version
```

Displays the installed Node.js version.

---

## Display npm Version

```powershell
npm --version
```

Displays the installed npm version.

---

## Display Node.js Location

```powershell
where.exe node
```

Displays the location of the Node.js executable.

---

# Visual Studio Code

## Display VS Code Version

```powershell
code --version
```

Displays the installed Visual Studio Code version.

---

# Windows PowerShell

## Display Environment PATH

```powershell
$env:Path
```

Displays the current PATH environment variable.

---

## Change Execution Policy

```powershell
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

Allows locally created PowerShell scripts to run.

Used to resolve the npm PowerShell execution policy issue.

---

# Notes

This document will continue to grow as new tools and commands are introduced during the Spec-Driven Development learning journey.