# 🚀 How to Push Server Folder to GitHub

## Step-by-Step Instructions

### Step 1: Create GitHub Repository First

1. Go to **https://github.com/new**
2. Repository name: `lms-backend`
3. Description: "LMS Backend API Server"
4. Make it **Public** ✅ (Important for Render free tier)
5. **DO NOT** initialize with README, .gitignore, or license
6. Click **"Create repository"**
7. **Copy the repository URL** (e.g., `https://github.com/YOUR_USERNAME/lms-backend.git`)

---

### Step 2: Open Terminal in Server Folder

1. Open PowerShell or Command Prompt
2. Navigate to your server folder:
   ```powershell
   cd C:\Projects\LMS\server
   ```

---

### Step 3: Initialize Git (if not already done)

```powershell
git init
```

---

### Step 4: Add All Files

```powershell
git add .
```

This adds:
- server.js
- package.json
- package-lock.json
- render.yaml
- .gitignore

(It will NOT add node_modules or .env files because of .gitignore)

---

### Step 5: Commit Files

```powershell
git commit -m "Initial commit - LMS backend server"
```

---

### Step 6: Add GitHub Remote

Replace `YOUR_USERNAME` with your actual GitHub username:

```powershell
git remote add origin https://github.com/YOUR_USERNAME/lms-backend.git
```

---

### Step 7: Push to GitHub

```powershell
git branch -M main
git push -u origin main
```

You may be asked to login to GitHub:
- Use your GitHub username and password
- Or use a Personal Access Token (if 2FA is enabled)

---

## ✅ Done!

Your server code is now on GitHub!

Next step: Go to Render.com and connect this repository.

---

## Troubleshooting

**Error: "remote origin already exists"**
```powershell
git remote remove origin
git remote add origin https://github.com/YOUR_USERNAME/lms-backend.git
```

**Error: "Authentication failed"**
- Use GitHub Personal Access Token instead of password
- Create token: GitHub → Settings → Developer settings → Personal access tokens → Generate new token

**Error: "Permission denied"**
- Make sure repository is **Public** (not private) on GitHub
- Check your GitHub username is correct

