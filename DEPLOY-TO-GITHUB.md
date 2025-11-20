# 📤 Deploy to GitHub

## ✅ App Created

Your simple Hello World app is ready at:
`/Users/kevinye/Documents/KevinYe/Openshift/myarticles/2025-11/hello-world-app/`

**Files:**
- `app.js` - Main application (Hello World web server)
- `package.json` - NPM configuration
- `README.md` - Basic documentation
- `.gitignore` - Git ignore file

## 🧪 Test Locally First

```bash
cd /Users/kevinye/Documents/KevinYe/Openshift/myarticles/2025-11/hello-world-app

# Run the app
node app.js

# In another terminal, test it:
curl http://localhost:8080

# Or open in browser:
open http://localhost:8080
```

You should see "Hello World!" displayed.

Press **Ctrl+C** to stop the server.

## 📤 Push to Your GitHub

### Step 1: Create GitHub Repo

1. Go to https://github.com/new
2. Repository name: `hello-world-app` (or your choice)
3. Keep it **Public** or **Private** (your choice)
4. **DO NOT** initialize with README (we already have one)
5. Click **Create repository**

### Step 2: Push to GitHub

```bash
cd /Users/kevinye/Documents/KevinYe/Openshift/myarticles/2025-11/hello-world-app

# Initialize git
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit: Hello World app"

# Add your GitHub repo as remote
# Replace YOUR-USERNAME with your actual GitHub username
git remote add origin https://github.com/YOUR-USERNAME/hello-world-app.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Verify

Go to your GitHub repo URL:
`https://github.com/YOUR-USERNAME/hello-world-app`

You should see all the files!

## 🚀 Use in Your DevSpace on ROSA HCP

Once pushed to GitHub, in your DevSpace instance:

```bash
# Clone the repo
git clone https://github.com/YOUR-USERNAME/hello-world-app.git
cd hello-world-app

# Run it
node app.js
```

Or if you want to access it via route, you'll need to create Kubernetes manifests (deployment, service, route).

## 📋 Quick Reference

**Local test:**
```bash
node app.js
# Open http://localhost:8080
```

**Git commands:**
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR-USERNAME/hello-world-app.git
git branch -M main
git push -u origin main
```

**Clone in DevSpace:**
```bash
git clone https://github.com/YOUR-USERNAME/hello-world-app.git
```

Done! ✅

