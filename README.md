# Celebal_project_Git-and-github
# 🚀 Git Workflow Project

A hands-on guide to mastering Git with real-world scenarios. This project includes mock files and demonstrates common Git tasks.

---

## 📁 Files in This Project

- `index.html` – Homepage file
- `login.js` – Handles login logic
- `style.css` – Basic styling
- `README.md` – Documentation

---

## ✅ 1. Stage All Changes & Commit
```bash
git add .
git commit -m "Initial commit with HTML, CSS, and JS files"
```

---

## ❌ 2. Move Commits to Correct Branch
### Scenario: You committed to `main` but wanted `feature/login`.
```bash
git checkout -b feature/login
git checkout main
git reset --hard HEAD~1
git push origin feature/login
```

---

## 🌿 3. Create New Branch, Make Changes, and Push
```bash
git checkout -b feature/ui-update
# Modify style.css

git add style.css
git commit -m "Improved dashboard UI responsiveness"
git push origin feature/ui-update
```

---

## 🤝 4. Contribute to Open Source
### Steps:
```bash
# Fork repo on GitHub

git clone https://github.com/your-username/project.git
cd project
git remote add upstream https://github.com/original-user/project.git
git checkout -b fix/typo-fix
# Make changes
git add .
git commit -m "Fix typo in login button text"
git push origin fix/typo-fix
```
Then go to GitHub and create a Pull Request.

---

## ⚔️ 5. Resolve Merge Conflicts
```bash
git checkout feature/payment
git fetch origin
git merge origin/main
```
- Fix conflict markers in affected files
- Then:
```bash
git add .
git commit -m "Resolved merge conflicts"
```

---

## 🌱 6. Create a Feature Branch Based on Main
```bash
git checkout main
git pull origin main
git checkout -b feature/invoice-module
```

---

## ⏪ 7. Revert to a Specific Commit
```bash
git log  # Copy commit hash
git reset --hard <commit-hash>
git push origin HEAD --force
```

---

## 🗃️ 8. Restore Deleted File
```bash
git checkout HEAD^ -- login.js
git add login.js
git commit -m "Restored deleted login.js"
```

---

## 📤 Optional Script
Create a `start-feature.sh`:
```bash
#!/bin/bash
echo "Enter your branch name:"
read branch
git checkout main
git pull origin main
git checkout -b $branch
echo "Switched to branch: $branch"
```
Run it with:
```bash
bash start-feature.sh
```

---

## 🧪 Mock File Contents
### index.html
```html
<!DOCTYPE html>
<html>
<head><title>Home</title></head>
<body>
  <h1>Welcome to Git Workflow Project</h1>
</body>
</html>
```

### login.js
```js
function login() {
  console.log("Logging in user...");
}
```

### style.css
```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}
```

---

## 📌 GitHub Setup
1. Create a GitHub repository
2. Push:
```bash
git remote add origin https://github.com/your-username/git-workflow-project.git
git push -u origin main
```

---

Happy Coding! 💻
