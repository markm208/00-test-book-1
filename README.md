# 00 Test Book 1

By Mark M

## Directory Structure

```
00-test-book-1/
  book.json       # Book metadata and table of contents
  index.html      # Generated table of contents page
  assets/js/      # Shared playback viewer code
  playbacks/      # Individual playback directories
```

## Editing the Book

To reorganize chapters or playbacks, edit `book.json` directly. After making changes, run the **Storyteller: Regenerate Book Index** command in VS Code to update `index.html`.

## Hosting on GitHub Pages

1. Create a new repository on GitHub named `00-test-book-1`
2. Push this directory to the repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/00-test-book-1.git
   git push -u origin main
   ```
3. Go to your repository on GitHub
4. Click **Settings** > **Pages**
5. Under "Source", select **Deploy from a branch**
6. Select the **main** branch and **/ (root)** folder
7. Click **Save**
8. Your book will be available at `https://YOUR_USERNAME.github.io/00-test-book-1/`

## Hosting on GitLab Pages

1. Create a new project on GitLab named `00-test-book-1`
2. Create a `.gitlab-ci.yml` file in the root with:
   ```yaml
   pages:
     stage: deploy
     script:
       - mkdir .public
       - cp -r * .public
       - mv .public public
     artifacts:
       paths:
         - public
   ```
3. Push this directory to the project:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://gitlab.com/YOUR_USERNAME/00-test-book-1.git
   git push -u origin main
   ```
4. GitLab will automatically build and deploy your site
5. Your book will be available at `https://YOUR_USERNAME.gitlab.io/00-test-book-1/`

Replace `YOUR_USERNAME` with your actual GitHub or GitLab username.

This book was created with [Storyteller](https://github.com/markm208/storyteller).
