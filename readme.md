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

---

## 4. Setting Up SSH on macOS

### 4.1 Generate an ED25519 SSH Key

In your terminal, run:
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```
- Press **Enter** to accept the default location (usually `~/.ssh/id_ed25519`).
- Enter a passphrase (or skip by pressing Enter), then confirm.

### 4.2 Add Your SSH Key to the ssh-agent

Start the ssh-agent (if not already running) and add your key:
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

### 4.3 Add the Public Key to Your GitHub Account

1. Copy the public key to your clipboard:
   ```bash
   pbcopy < ~/.ssh/id_ed25519.pub
   ```
2. Go to [GitHub.com](https://github.com), click your profile photo in the top-right corner, then **Settings**.
3. In the left sidebar, click **SSH and GPG keys**.
4. Click **New SSH key**, provide a descriptive title, and paste your public key into the *Key* field.
5. Click **Add SSH key**.

### 4.4 Test Your SSH Connection

Verify everything is working:
```bash
ssh -T git@github.com
```
You should see a message like:
```
Hi <username>! You've successfully authenticated, but GitHub does not provide shell access.
```

You’re all set to use SSH with GitHub!

---

## 5. Setting Up SSH on Windows

### 5.1 Generate an ED25519 SSH Key

In Git Bash or PowerShell, run:
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```
- Press **Enter** to accept the default location (usually `~/.ssh/id_ed25519`).
- Enter a passphrase (or skip by pressing Enter), then confirm.

### 5.2 Add Your SSH Key to the ssh-agent

Start the ssh-agent (if not already running) and add your key:
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

### 5.3 Add the Public Key to Your GitHub Account

1. Copy the public key to your clipboard. In Git Bash, run:
   ```bash
   clip < ~/.ssh/id_ed25519.pub
   ```
   Or in PowerShell:
   ```powershell
   Get-Content ~/.ssh/id_ed25519.pub | clip
   ```
2. Go to [GitHub.com](https://github.com), click your profile photo in the top-right corner, then **Settings**.
3. In the left sidebar, click **SSH and GPG keys**.
4. Click **New SSH key**, provide a descriptive title, and paste your public key into the *Key* field.
5. Click **Add SSH key**.

### 5.4 Test Your SSH Connection

Verify everything is working by running:
```bash
ssh -T git@github.com
```
You should see a message like:
```
Hi <username>! You've successfully authenticated, but GitHub does not provide shell access.
```

You’re all set to use SSH with GitHub!

