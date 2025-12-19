# SITE1101 — Conversation & Shared Files
Date: 2025-12-19

This file is a downloadable transcript of the recent conversation and the HTML/README files shared during the session. Use this to keep a record or to include in the project folder.

---

## Conversation summary
- User requested a clean, responsive modular static website (SITE 1101).
- Assistant proposed a directory structure and provided a README.md.
- User provided `index.html` and `projects.html`.
- Assistant suggested accessibility and styling improvements (active nav state, responsive project images).
- CONVERSATION.md below updated to reflect the latest project file changes.

---

## index.html
```html
<!-- filepath: /Users/aishagoja/Desktop/site1101/index.html -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Aisha Goja</title>
    <link rel="stylesheet" href="assets/css/style.css" />
  </head>
  <body>
    <!-- Navigation -->
    <nav>
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="projects.html">Projects</a>
    </nav>

    <!-- Home Content -->
    <div class="profile-pic">
      <img src="assets/images/profil.jpg" alt="profile" />
    </div>
    <h1>Hello- I'm Aisha Goja</h1>
    <p class="color-dark">
      Welcome to my personal website! I’m a student passionate about Information
      Systems and Web Development.
    </p>

    <footer class="footer">
      <div class="footer-left">
        <a href="https://github.com/aishagjv" target="_blank">
          <img
            src="assets/images/github.svg"
            alt="GitHub"
            class="footer-icon"
          />
        </a>
        <a href="https://www.codecademy.com/profiles/gojayevaaisha" target="_blank">
          <img src="assets/images/codeacademy.png" alt="Code" class="footer-icon" />
        </a>
      </div>

      <div class="footer-right">© 2025 Aisha Goja. All rights reserved.</div>
    </footer>
  </body>
</html>
```

---

## projects.html (updated)
```html
<!-- filepath: /Users/aishagoja/Desktop/site1101/projects.html -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Aisha Goja — Projects</title>
    <link rel="stylesheet" href="assets/css/style.css" />
  </head>
  <body>
    <!-- Navigation -->
    <nav>
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="projects.html" class="active" aria-current="page">Projects</a>
    </nav>

    <h1 class="project-title">Projects</h1>

    <div class="projects">
      <div class="project-item">
        <img class="project-image" src="assets/images/project1.JPG" alt="Logic Gates project screenshot" />
        <h2>Logic Gates</h2>
        <p class="color-dark">
          To construct basic logic gates (AND, OR, NOT, NAND, XOR) using
          transistors and other electronic components. Role: Developer —
          responsible for layout, styling, and interactivity. Technologies:
          transistor-based circuits and prototyping.
        </p>
      </div>

      <div class="project-item">
        <img class="project-image" src="assets/images/Project2.png" alt="Hour of Code screenshot" />
        <h2>Hour of Code</h2>
        <p class="color-dark">
          Hour of Code — a beginner-friendly interactive lesson built with HTML,
          CSS, and JavaScript that teaches core programming concepts through
          short hands-on exercises and challenges.
        </p>
      </div>
    </div>

    <footer class="footer">
      <div class="footer-left">
        <a href="https://github.com/aishagjv" target="_blank">
          <img src="assets/images/github.svg" alt="GitHub" class="footer-icon" />
        </a>
        <a href="https://www.codecademy.com/profiles/gojayevaaisha" target="_blank">
          <img src="assets/images/codeacademy.png" alt="Codecademy" class="footer-icon" />
        </a>
        <!-- Visible link to repository -->
        <a href="https://github.com/aishagjv/site1101" target="_blank" class="repo-link">Repository</a>
      </div>

      <div class="footer-right">© 2025 Aisha Goja. All rights reserved.</div>
    </footer>
  </body>
</html>
```

---

## CSS snippets added / recommended
```css
// filepath: /Users/aishagoja/Desktop/site1101/assets/css/style.css
/* Active nav link */
nav a.active,
nav a[aria-current="page"] {
  color: #ffffff;
  background: #2b6cb0;
  padding: 0.45rem 0.75rem;
  border-radius: 8px;
  font-weight: 600;
  box-shadow: 0 2px 6px rgba(43,108,176,0.12);
}

/* Project image styling — consistent, responsive card images */
.project-image {
  width: 480px;
  height: 240px;
  object-fit: cover;
  border-radius: 16px;
  border: 4px solid #ffffff;
  display: block;
  margin: 0 auto 1rem;
}

/* Responsive adjustments */
@media (max-width: 640px) {
  .project-image {
    width: 100%;
    height: 180px;
  }
}
```

---

## README.md (previously provided)
```markdown
// filepath: /Users/aishagoja/Desktop/site1101/README.md
# SITE 1101 — personal portfolio (Aisha Goja)

Brief static portfolio site built with HTML, CSS and JavaScript for the SITE 1101 university project.

## Features
- Home (index.html) — profile photo + short intro
- About (about.html) — background, qualifications, activities
- Projects (projects.html) — project cards with screenshot, title, description
- Global responsive navigation bar and footer with links to GitHub & Codecademy
- Modular structure: assets/css, assets/js, assets/images
- Fully responsive for mobile, tablet, desktop

## Repository structure
assets/
  css/
    style.css
  images/
index.html
about.html
projects.html
README.md

## How to view locally
1. Open the project folder in your file manager and double-click `index.html` — or run a local server:
   - In Terminal (macOS) from project root:
     ```
     python3 -m http.server 8000
     ```
   - Then open: http://localhost:8000

## Common development tasks
- Edit HTML files in the project root.
- Edit styles in `assets/css/style.css`.
- Edit JS in `assets/js/script.js`.
- Add images to `assets/images/` and reference them from HTML.

## Git: quick commit & push (Terminal, macOS)
1. Initialize repo (if not already):
   ```
   cd /Users/aishagoja/Desktop/site1101
   git init
   git add .
   git commit -m "Initial site1101 portfolio files"
   ```
2. Create a remote repository on GitHub (web) or with GitHub CLI:
   ```
   gh repo create Aisha-site1101 --public --source=. --remote=origin --push
   ```
   (If not using `gh`, create repo on GitHub and then:)
   ```
   git remote add origin https://github.com/<your-username>/<repo>.git
   git branch -M main
   git push -u origin main
   ```

## Deploy to GitHub Pages
Option A — GitHub Pages from `main` branch:
1. Push changes to `main` (see Git steps above).
2. On GitHub repo page → Settings → Pages → Branch: `main` / Folder: `/ (root)` → Save.
3. After a minute, your site will be available at `https://<your-username>.github.io/<repo>/`.
```

---

Place this updated CONVERSATION.md at: /Users/aishagoja/Desktop/site1101/CONVERSATION.md
```// filepath: /Users/aishagoja/Desktop/site1101/CONVERSATION.md
# SITE1101 — Conversation & Shared Files
Date: 2025-12-19

This file is a downloadable transcript of the recent conversation and the HTML/README files shared during the session. Use this to keep a record or to include in the project folder.

---

## Conversation summary
- User requested a clean, responsive modular static website (SITE 1101).
- Assistant proposed a directory structure and provided a README.md.
- User provided `index.html` and `projects.html`.
- Assistant suggested accessibility and styling improvements (active nav state, responsive project images).
- CONVERSATION.md below updated to reflect the latest project file changes.

---

## index.html
```html
<!-- filepath: /Users/aishagoja/Desktop/site1101/index.html -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Aisha Goja</title>
    <link rel="stylesheet" href="assets/css/style.css" />
  </head>
  <body>
    <!-- Navigation -->
    <nav>
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="projects.html">Projects</a>
    </nav>

    <!-- Home Content -->
    <div class="profile-pic">
      <img src="assets/images/profil.jpg" alt="profile" />
    </div>
    <h1>Hello- I'm Aisha Goja</h1>
    <p class="color-dark">
      Welcome to my personal website! I’m a student passionate about Information
      Systems and Web Development.
    </p>

    <footer class="footer">
      <div class="footer-left">
        <a href="https://github.com/aishagjv" target="_blank">
          <img
            src="assets/images/github.svg"
            alt="GitHub"
            class="footer-icon"
          />
        </a>
        <a href="https://www.codecademy.com/profiles/gojayevaaisha" target="_blank">
          <img src="assets/images/codeacademy.png" alt="Code" class="footer-icon" />
        </a>
      </div>

      <div class="footer-right">© 2025 Aisha Goja. All rights reserved.</div>
    </footer>
  </body>
</html>
```

---

## projects.html (updated)
```html
<!-- filepath: /Users/aishagoja/Desktop/site1101/projects.html -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Aisha Goja — Projects</title>
    <link rel="stylesheet" href="assets/css/style.css" />
  </head>
  <body>
    <!-- Navigation -->
    <nav>
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="projects.html" class="active" aria-current="page">Projects</a>
    </nav>

    <h1 class="project-title">Projects</h1>

    <div class="projects">
      <div class="project-item">
        <img class="project-image" src="assets/images/project1.JPG" alt="Logic Gates project screenshot" />
        <h2>Logic Gates</h2>
        <p class="color-dark">
          To construct basic logic gates (AND, OR, NOT, NAND, XOR) using
          transistors and other electronic components. Role: Developer —
          responsible for layout, styling, and interactivity. Technologies:
          transistor-based circuits and prototyping.
        </p>
      </div>

      <div class="project-item">
        <img class="project-image" src="assets/images/Project2.png" alt="Hour of Code screenshot" />
        <h2>Hour of Code</h2>
        <p class="color-dark">
          Hour of Code — a beginner-friendly interactive lesson built with HTML,
          CSS, and JavaScript that teaches core programming concepts through
          short hands-on exercises and challenges.
        </p>
      </div>
    </div>

    <footer class="footer">
      <div class="footer-left">
        <a href="https://github.com/aishagjv" target="_blank">
          <img src="assets/images/github.svg" alt="GitHub" class="footer-icon" />
        </a>
        <a href="https://www.codecademy.com/profiles/gojayevaaisha" target="_blank">
          <img src="assets/images/codeacademy.png" alt="Codecademy" class="footer-icon" />
        </a>
        <!-- Visible link to repository -->
        <a href="https://github.com/aishagjv/site1101" target="_blank" class="repo-link">Repository</a>
      </div>

      <div class="footer-right">© 2025 Aisha Goja. All rights reserved.</div>
    </footer>
  </body>
</html>
```

---

## CSS snippets added / recommended
```css
// filepath: /Users/aishagoja/Desktop/site1101/assets/css/style.css
/* Active nav link */
nav a.active,
nav a[aria-current="page"] {
  color: #ffffff;
  background: #2b6cb0;
  padding: 0.45rem 0.75rem;
  border-radius: 8px;
  font-weight: 600;
  box-shadow: 0 2px 6px rgba(43,108,176,0.12);
}

/* Project image styling — consistent, responsive card images */
.project-image {
  width: 480px;
  height: 240px;
  object-fit: cover;
  border-radius: 16px;
  border: 4px solid #ffffff;
  display: block;
  margin: 0 auto 1rem;
}

/* Responsive adjustments */
@media (max-width: 640px) {
  .project-image {
    width: 100%;
    height: 180px;
  }
}
```

---

## README.md (previously provided)
```markdown
// filepath: /Users/aishagoja/Desktop/site1101/README.md
# SITE 1101 — personal portfolio (Aisha Goja)

Brief static portfolio site built with HTML, CSS and JavaScript for the SITE 1101 university project.

## Features
- Home (index.html) — profile photo + short intro
- About (about.html) — background, qualifications, activities
- Projects (projects.html) — project cards with screenshot, title, description
- Global responsive navigation bar and footer with links to GitHub & Codecademy
- Modular structure: assets/css, assets/js, assets/images
- Fully responsive for mobile, tablet, desktop

## Repository structure
assets/
  css/
    style.css
  images/
index.html
about.html
projects.html
README.md

## How to view locally
1. Open the project folder in your file manager and double-click `index.html` — or run a local server:
   - In Terminal (macOS) from project root:
     ```
     python3 -m http.server 8000
     ```
   - Then open: http://localhost:8000

## Common development tasks
- Edit HTML files in the project root.
- Edit styles in `assets/css/style.css`.
- Edit JS in `assets/js/script.js`.
- Add images to `assets/images/` and reference them from HTML.

## Git: quick commit & push (Terminal, macOS)
1. Initialize repo (if not already):
   ```
   cd /Users/aishagoja/Desktop/site1101
   git init
   git add .
   git commit -m "Initial site1101 portfolio files"
   ```
2. Create a remote repository on GitHub (web) or with GitHub CLI:
   ```
   gh repo create Aisha-site1101 --public --source=. --remote=origin --push
   ```
   (If not using `gh`, create repo on GitHub and then:)
   ```
   git remote add origin https://github.com/<your-username>/<repo>.git
   git branch -M main
   git push -u origin main
   ```

## Deploy to GitHub Pages
Option A — GitHub Pages from `main` branch:
1. Push changes to `main` (see Git steps above).
2. On GitHub repo page → Settings → Pages → Branch: `main` / Folder: `/ (root)` → Save.
3. After a minute, your site will be available at `https://<your-username>.github.io/<repo>/`.
```

---

Place this updated CONVERSATION.md at: /Users/aishagoja/Desktop/site1101/CONVERSATION.md