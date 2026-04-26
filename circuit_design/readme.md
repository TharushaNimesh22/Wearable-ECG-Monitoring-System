# Git Commands Reference Guide

A step-by-step guide to setting up and working with a Git repository.

---

## 1. Configure Git Username (for first time only)

```bash
git config --global user.name "Your user name"
```

Sets your **global Git username** to be associated with all commits made on this machine. This name will appear in the commit history.

---

## 2. Configure Git Email(for first time only)

```bash
git config --global user.email "ideacreatorslk@gmail.com"
```

Sets your **global Git email address**. This email is linked to your commits and should match the email used with your GitHub account.

---

## 3. Navigate to the Target Directory

```bash
cd ".\path"
```

Changes the current working directory to the specified path (replace `path` with your actual folder path). This is where you want to clone the repository.

---

## 4. Clone the Repository

```bash
git clone https://github.com/IdeaDP/Wearable-ECG-Monitoring-System.git
```

**Downloads (clones) a remote repository** from GitHub to your local machine. Creates a new folder named `Wearable-ECG-Monitoring-System` containing all the project files and history.

---

## 5. Check Repository Status

```bash
git status
```

Displays the **current state of the working directory and staging area**. Shows which files are modified, staged for commit, or untracked. Run this frequently to understand what has changed.

---

## 6. View a File's Contents

```bash
type circuit_design.gitignore
```

Displays the contents of the `circuit_design.gitignore` file in the terminal (Windows command). A `.gitignore` file specifies which files and folders Git should **intentionally ignore** and not track.

---

## 7. Check Remote Connection

```bash
git remote -v
```

Lists all **remote connections** associated with the local repository, along with their URLs. `origin` is the default name for the remote repository you cloned from. `-v` stands for verbose (shows URLs).

---

## 8. Enter the Cloned Repository Folder

```bash
cd ./Wearable-ECG-Monitoring-System
```

Navigates **into the cloned project directory** so subsequent Git commands are run within the correct repository.

---

## 9. Stage All Changes

```bash
git add .
```

**Stages all changed, new, and deleted files** in the current directory for the next commit. The `.` refers to all files in the current directory and its subdirectories.

---

## 10. Verify Staged Files

```bash
git status
```

Run `git status` again **after staging** to confirm which files are now staged (shown in green) and ready to be committed.

---

## 11. Commit the Changes

```bash
git commit -m "Move Altium project files into circuit_design folder"
```

**Saves the staged changes** to the local repository history with a descriptive message. The `-m` flag lets you write the commit message inline. Always write clear, meaningful messages.

> **Example messages:**
> - `"Add initial ECG sensor schematic"`
> - `"Fix resistor values in power circuit"`
> - `"Move Altium project files into circuit_design folder"`

---

## 12. Push to a Specific Branch

**Changing active branch to your branch**

```bash
git checkout -b <branch_name>
```


```bash
git push origin <branch_name>
```

**Uploads your local commits** to the specified branch on the remote repository (`origin`). Replace `<branch_name>` with the actual branch name (e.g., `main`, `develop`, `feature/ecg-filter`).

---

## 13. Push to the Default Branch

```bash
git push
```

Pushes commits to the **default tracked remote branch** (typically `origin main` or whichever branch was set as upstream). A shorthand for when the tracking branch is already configured.

---

## Summary Workflow

| Step | Command | Purpose |
|------|---------|---------|
| 1 | `git config --global user.name "..."` | Set global username |
| 2 | `git config --global user.email "..."` | Set global email |
| 3 | `cd ".\path"` | Navigate to target directory |
| 4 | `git clone <url>` | Clone remote repository |
| 5 | `git status` | Check current state |
| 6 | `type <file>` | View file contents |
| 7 | `git remote -v` | Verify remote connections |
| 8 | `cd ./Wearable-ECG-Monitoring-System` | Enter project folder |
| 9 | `git add .` | Stage all changes |
| 10 | `git status` | Confirm staged files |
| 11 | `git commit -m "message"` | Commit with a message |
| 12 | `git push origin <branch>` | Push to a specific branch |
| 13 | `git push` | Push to default branch |

---

*Generated for the Wearable ECG Monitoring System project by Dissanayaka D.M.D.P.*
