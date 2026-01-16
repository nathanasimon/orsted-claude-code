# Push to GitHub

## Create Repository on GitHub

1. Go to https://github.com/new
2. Create repository: `orsted-claude-code`
3. **Don't** initialize with README (we already have files)

## Push to GitHub

```bash
cd /Users/nathansimon/orsted-marketplace-1/orsted-claude-code-repo
git remote add origin https://github.com/nathanasimon/orsted-claude-code.git
git branch -M main
git push -u origin main
```

## Update README

After pushing, update the GitHub URLs in:
- `README.md` - Replace `nathanasimon` with your actual GitHub username
