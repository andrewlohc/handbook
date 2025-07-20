# SSH Setup for Git

## Overview
This document describes how to set up SSH authentication for Git repositories using ed25519 keys, including managing multiple accounts (personal and work).

## Steps Completed

### 1. Generate SSH Keys
Generated ed25519 SSH key pairs for different accounts:

**Personal account:**
```bash
ssh-keygen -t ed25519 -f ~/.ssh/id_ed25519_personal -C "personal@email.com"
```

**Work account:**
```bash
ssh-keygen -t ed25519 -f ~/.ssh/id_ed25519_work -C "work@company.com"
```

### 2. Configure SSH Config
Created `~/.ssh/config` to manage multiple keys:
```
# Personal GitHub
Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519_personal

# Work GitHub
Host github-work
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519_work
```

### 3. Start SSH Agent and Add Keys
Started the SSH authentication agent and added keys:
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519_personal
ssh-add ~/.ssh/id_ed25519_work
```

### 4. Add Public Keys to GitHub
- Copied public key content from respective `.pub` files
- Added to appropriate GitHub accounts under Settings → SSH and GPG keys
- Selected "Authentication key" type for both

### 5. Update Git Remotes
**For personal repositories:**
```bash
git remote set-url origin git@github.com:username/repository.git
```

**For work repositories:**
```bash
git remote set-url origin git@github-work:company/repository.git
```

### 6. Configure Git User Info Per Repository
Set appropriate user information for work repositories:
```bash
git config user.email "work@company.com"
git config user.name "Work Name"
```

## Verification
Test SSH connections:

**Personal:**
```bash
ssh -T git@github.com
```

**Work:**
```bash
ssh -T git@github-work
```

Both should show success messages confirming authentication.

## Checking SSH Credentials in Use

To verify which SSH credentials a project is using:

### Check Remote URL
```bash
git remote -v
```
This shows the remote URL format:
- `git@github.com:username/repo.git` → Uses personal key
- `git@github-work:company/repo.git` → Uses work key

### Check Git User Configuration
```bash
git config user.email
git config user.name
```
Shows the configured user for the current repository.

### Check SSH Key Being Used
```bash
ssh -T git@github.com
ssh -T git@github-work
```
Test which SSH key authenticates successfully for each host.

### View SSH Agent Keys
```bash
ssh-add -l
```
Lists all SSH keys currently loaded in the SSH agent.

## Benefits
- No need to enter credentials for Git operations
- More secure than HTTPS with tokens
- Easy management of multiple GitHub accounts
- Automatic key selection based on repository