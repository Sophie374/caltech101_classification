# Step-by-Step Guide: Uploading to GitHub

Follow these steps to upload your repository to GitHub as a public repo:

## Step 1: Initialize Git Repository

Open your terminal and navigate to your project directory:

```bash
cd /Users/chufeipeng/Desktop/caltech101_classification
```

Initialize git (if not already done):

```bash
git init
```

## Step 2: Add Files to Git

Add all files to git:

```bash
git add .
```

This will add:
- `mini_project_1_colab.ipynb` (your notebook)
- `.gitignore` (to exclude unnecessary files)
- `README.md` (project documentation)

## Step 3: Make Your First Commit

Create your initial commit:

```bash
git commit -m "Initial commit: Caltech-101 image classification project"
```

## Step 4: Create a GitHub Repository

1. Go to [GitHub.com](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Repository name: `caltech101_classification` (or any name you prefer)
5. Description: "Image classification on Caltech-101 dataset comparing HOG+SVM, EfficientNet, and ResNet18"
6. **Select "Public"** (since you want a public repo)
7. **DO NOT** initialize with README, .gitignore, or license (we already have these)
8. Click "Create repository"

## Step 5: Connect Local Repository to GitHub

After creating the repository, GitHub will show you commands. Use these:

```bash
# Add the remote repository (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/caltech101_classification.git

# Rename the default branch to main (if needed)
git branch -M main

# Push your code to GitHub
git push -u origin main
```

If you're using SSH instead of HTTPS:

```bash
git remote add origin git@github.com:YOUR_USERNAME/caltech101_classification.git
git branch -M main
git push -u origin main
```

## Step 6: Verify

Go to your GitHub repository page and verify that all files are uploaded correctly.

## Troubleshooting

### If you get authentication errors:
- For HTTPS: You may need to use a Personal Access Token instead of password
- For SSH: Make sure your SSH key is set up with GitHub

### If you need to update files later:
```bash
git add .
git commit -m "Your commit message"
git push
```

## Notes

- The `.gitignore` file will prevent large files (models, datasets, outputs) from being uploaded
- Only your notebook and documentation will be pushed to GitHub
- This keeps the repository lightweight and fast
