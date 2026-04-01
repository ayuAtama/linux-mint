# 🔐 1. Stop Git from asking credentials every time

## ✅ Best option (recommended): SSH keys

This is the standard, secure, and one-time setup.

### Step-by-step

```bash
# 1. Generate SSH key
ssh-keygen -t ed25519 -C "your_email@example.com"

# 2. Start ssh agent
eval "$(ssh-agent -s)"

# 3. Add key
ssh-add ~/.ssh/id_ed25519
```

### Copy your public key

```bash
cat ~/.ssh/id_ed25519.pub
```

Then:

- Go to GitHub → Settings → SSH and GPG keys
- Add the key

### Change your repo remote to SSH

```bash
git remote set-url origin git@github.com:username/repo.git
```

### Test

```bash
ssh -T git@github.com
```

👉 After this, **no more password prompts ever**.

---

# ✨ 2. Get “Verified” badge on commits

This is NOT automatic — you must **sign your commits**.

---

## 🥇 Option A (recommended): SSH commit signing (modern & simple)

GitHub now supports signing commits using SSH keys.

### Enable it:

```bash
git config --global gpg.format ssh
git config --global user.signingkey ~/.ssh/id_ed25519.pub
git config --global commit.gpgsign true
```

Then:

- Go to GitHub → SSH keys
- Add your key also as **Signing key**

👉 Done. Every commit will be **Verified**.

---

# 🚀 Minimal setup (if you want fastest path)

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

git config --global gpg.format ssh
git config --global user.signingkey ~/.ssh/id_ed25519.pub
git config --global commit.gpgsign true
```

Add key to GitHub → done.

---
