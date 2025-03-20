# Quick Guide: Installing Git & Cloning Repo

## 1. Install Git

### macOS
- **Option 1**: Use [Homebrew](https://brew.sh/)
  - `brew install git`
- **Option 2**: Install [Xcode Command Line Tools](https://developer.apple.com/xcode/resources/)
  - `xcode-select --install`
- **Option 3**: Download from [git-scm.com](https://git-scm.com/download/mac)

### Windows
- **Option 1**: Download from [git-scm.com](https://git-scm.com/download/win) and run the installer.
- **Option 2**: Use Windows Package Manager (PowerShell)
  - `winget install --id Git.Git -e --source winget`

---

## 2. Clone This Repo

1. Open your terminal (macOS) or command prompt/PowerShell (Windows).
2. Navigate to the folder where you want to store the project.
3. Run:
   ```bash
   git clone {gh_url}/sofiechim/dtu-prob-modelling
   ```
4. Change into the new folder:
   ```bash
   cd dtu-prob-modelling
   ```

---

## 3. Basic Git Workflow

1. **Open Terminal & Check Status (Optional)**
   ```bash
   git status
   ```
   - See which files have changed.

2. **Make and Save Your Changes**
   - Edit your files in the repository.

3. **Add Changes to Staging**
   ```bash
   git add .
   ```
   - Stages all changed files.
   - Alternatively, use `git add <specific-file>` to stage individual files.

4. **Commit Your Changes**
   ```bash
   git commit -m "Your commit message"
   ```
   - The message should briefly explain the changes.

5. **Push Your Changes**
   ```bash
   git push
   ```
   - Sends your local commits to the remote repository (GitHub).

6. **Pull Updates**
   ```bash
   git pull
   ```
   - Brings in any changes others have pushed to the repository.

7. **Check Status Again (Optional)**
   ```bash
   git status
   ```
   - Confirms everything is up to date.

