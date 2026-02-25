# Push to GitHub: Dissertation-Pilot

Run these commands in your terminal from the project root (`/Users/tommaso/Desktop/Dissertation`).

## 1. Initialize Git and add the remote

```bash
cd /Users/tommaso/Desktop/Dissertation

git init
git remote add origin https://github.com/tommorbia333/Dissertation-Pilot.git
```

## 2. (Optional) Add a root .gitignore

If you don’t have a `.gitignore` at the project root, create one so you don’t commit `node_modules`, `.env`, OS files, etc. Then:

```bash
git add .
git status   # review what will be committed
```

## 3. First commit and push

```bash
git add .
git commit -m "Initial commit: local dissertation project"
git branch -M main
git push -u origin main
```

If the remote already has commits (e.g. README), either overwrite with your local history:

```bash
git push -u origin main --force
```

**Warning:** `--force` overwrites the remote `main` branch. Only use if you intend to replace the GitHub repo with your local copy.

Or pull and merge first, then push:

```bash
git pull origin main --allow-unrelated-histories
# resolve any conflicts, then:
git add .
git commit -m "Merge remote with local"
git push -u origin main
```

## Authentication

- **HTTPS:** Git will ask for your GitHub username and password. Use a [Personal Access Token](https://github.com/settings/tokens) instead of your account password.
- **SSH:** If you use SSH keys, add the remote with:
  ```bash
  git remote add origin git@github.com:tommorbia333/Dissertation-Pilot.git
  ```
  Then use `git push -u origin main` as above.
