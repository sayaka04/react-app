# React + GitHub Pages

A React + TypeScript project created with Vite and deployed to GitHub Pages.

## 1\. Create the React App

Create a new Vite React project:

```
npm create vite@latest my-react-app
```

Choose:

```
React
TypeScript
```

Enter the project:

```
cd my-react-app
```

Install dependencies:

```
npm install
```

## 2\. Run Locally

Start the development server:

```
npm run dev
```

Open the local URL shown by Vite, usually:

```
http://localhost:5173/
```

Stop the server with:

```
Ctrl + C
```

## 3\. Configure GitHub Pages

Install `gh-pages`:

```
npm install --save-dev gh-pages
```

Update `package.json`:

```
{
  "name": "my-react-app",
  "homepage": "https://username.github.io/my-react-app/",
  "private": true,
  "version": "0.0.0",
  "type": "module",
  "scripts": {
    "dev": "vite",
    "build": "tsc && vite build",
    "preview": "vite preview",
    "predeploy": "npm run build",
    "deploy": "gh-pages -d dist"
  }
}
```

## 4\. Configure Vite

Create:

```
vite.config.ts
```

Add:

```
import { defineConfig } from 'vite'

export default defineConfig({
  base: '/my-react-app/',
})
```

The `base` setting is important because the project is hosted at:

```
https://username.github.io/my-react-app/
```

## 5\. Build the Project

Create the production build:

```
npm run build
```

This creates:

```
dist/
```

The `dist` folder contains the files that will be published.

## 6\. Create the Git Repository

Initialize Git:

```
git init
```

Add the files:

```
git add .
```

Create the first commit:

```
git commit -m "Initial React project"
```

## 7\. Connect to GitHub

Create a repository on GitHub named:

```
my-react-app
```

Connect the local repository:

```
git remote add origin https://github.com/username/my-react-app.git
```

Set the main branch:

```
git branch -M main
```

Push the project:

```
git push -u origin main
```

## 8\. Deploy to GitHub Pages

Run:

```
npm run deploy
```

This runs:

```
npm run build
     ↓
dist/
     ↓
gh-pages -d dist
     ↓
GitHub Pages
```

The live website is:

```
https://username.github.io/my-react-app/
```

## 9\. Future Updates

After changing the React code:

```
npm run dev
```

Test the changes locally.

Then deploy:

```
npm run deploy
```

If you also want to save the source-code changes to the `main` branch:

```
git add .
git commit -m "Update React app"
git push
npm run deploy
```

## Useful Commands

```
# Install dependencies
npm install

# Run locally
npm run dev

# Build production files
npm run build

# Preview production build
npm run preview

# Deploy to GitHub Pages
npm run deploy

# Check Git status
git status

# Save changes
git add .
git commit -m "Describe changes"
git push
```

## Project Flow

```
React + TypeScript
       ↓
    Vite
       ↓
 npm run build
       ↓
     dist/
       ↓
  gh-pages -d dist
       ↓
 GitHub Pages
       ↓
https://username.github.io/my-react-app/
```
