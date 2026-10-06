# Unit 4 – Student Hands-On Lab Script

## Repository Practice: Homepage + Git Workflow Reinforcement

---

## Purpose of this lab

In this lab, you will:

- Reinforce the Git workflow through repetition
- Build confidence working with repositories and commits
- Reduce reliance on step-by-step instructions
- Practise fixing common Git mistakes
- Treat documentation as part of normal development work

By the end of this session, using Git should feel repeatable rather than fragile.

---

## Prerequisites Check

### Goal

Start from a clean and predictable setup.

### Steps

1. Open your terminal.
2. Confirm Git is installed:

   ```bash
   git --version
   ```

3. Check your current location:

   ```bash
   pwd
   ```

4. Move to a general working directory (for example, your home folder).
5. Confirm you are **not** already inside a Git repository:

   ```bash
   git status
   ```

If Git reports that you are already inside a repository, move to a different directory before continuing.

### Checkpoint

- Git is installed and responding
- You understand where you are in the file system
- You are starting outside any existing Git repository

---

## Part 1 — Project 1: Homepage Repository (Guided)

### Goal

Repeat the full Git workflow with guidance and reinforce good habits.

---

### Part 1.1 — Create Project Directory

1. Create a new directory:

   ```bash
   mkdir unit4-homepage
   ```

2. Move into it:

   ```bash
   cd unit4-homepage
   ```

3. Confirm location:

   ```bash
   pwd
   ```

4. Open the folder in VS Code:

   ```bash
   code .
   ```

### Checkpoint

VS Code is open in the `unit4-homepage` folder.

---

### Part 1.2 — Create Initial Files

1. Create the project files:

   ```bash
   touch index.html
   touch style.css
   ```

2. Open `index.html` and add the following:

   ```html
   <!DOCTYPE html>
   <html lang="en">
     <head>
       <meta charset="UTF-8" />
       <title>My Homepage</title>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <header>
         <h1>Welcome</h1>
       </header>

       <main>
         <p>This is my homepage.</p>
       </main>
     </body>
   </html>
   ```

3. Save the file.

---

### Part 1.3 — Initialise Git and First Commit

1. Initialise Git:

   ```bash
   git init
   ```

2. Check repository status:

   ```bash
   git status
   ```

3. Stage all files:

   ```bash
   git add .
   ```

4. Commit:

   ```bash
   git commit -m "Initial homepage structure"
   ```

### Checkpoint

- Git is initialised
- One commit exists
- `git status` shows a clean working tree

---

### Part 1.4 — Create GitHub Repository

1. Open GitHub in your browser.
2. Create a new repository.
3. Repository name:

   ```
   unit4-homepage
   ```

4. Do **not** add:
   - README
   - Licence
   - `.gitignore`

5. Create the repository.
6. Copy the HTTPS repository URL.

---

### Part 1.5 — Connect and Push

1. Add the remote repository:

   ```bash
   git remote add origin <PASTE_REPOSITORY_URL>
   ```

2. Push to GitHub:

   ```bash
   git branch -M main
   git push -u origin main
   ```

3. Refresh the GitHub page.

### Checkpoint

Your files are visible on GitHub.

---

### Part 1.6 — Incremental Change: Navigation

1. Open `index.html`.
2. Add the following navigation section inside `<body>`:

   ```html
   <nav>
     <a href="#">Home</a>
     <a href="#">About</a>
   </nav>
   ```

3. Save the file.
4. Commit and push:

   ```bash
   git add .
   git commit -m "Add basic navigation"
   git push
   ```

---

### Part 1.7 — Incremental Change: Styling

1. Open `style.css`.
2. Add:

   ```css
   body {
     font-family: Arial, sans-serif;
   }

   header {
     background-color: #f4f4f4;
     padding: 1rem;
   }
   ```

3. Save the file.
4. Commit and push:

   ```bash
   git add .
   git commit -m "Add basic page styling"
   git push
   ```

---

### Part 1.8 — Review History

1. View commit history locally:

   ```bash
   git log --oneline
   ```

2. Review commits on GitHub.

### Checkpoint

Your commit history clearly shows how the project evolved.

---

## Part 2 — Project 2: Second Repository (Reduced Guidance)

### Goal

Repeat the workflow with less instruction.

---

### Task

Create a **new project** with the following requirements:

- Folder name:

  ```
  unit4-profile
  ```

- Files:
  - `index.html`
  - `style.css`

- Content:
  - A heading with a name
  - A short paragraph

- Git:
  - Initialise Git
  - Make at least **two commits**
  - Push to GitHub

---

### Constraints

- Do **not** copy-paste from the first project
- Use the terminal and VS Code
- Use this command when stuck:

  ```bash
  git status
  ```

### Checkpoint

The second repository exists on GitHub with multiple commits.

---

## Part 3 — Break It and Fix It Lab

### Goal

Practise reading and recovering from common Git errors.

---

### Exercise 1 — Commit Without Staging

1. Modify a file.
2. Try to commit without staging:

   ```bash
   git commit -m "Test commit"
   ```

3. Read the error message.
4. Fix it:

   ```bash
   git add .
   git commit -m "Properly staged commit"
   ```

---

### Exercise 2 — Push Without a Remote

1. Create a new directory:

   ```bash
   mkdir broken-repo
   cd broken-repo
   ```

2. Initialise Git and commit a file.
3. Attempt to push:

   ```bash
   git push
   ```

4. Read the error and identify what is missing.

---

### Exercise 3 — Wrong Directory

1. Move to the parent directory.
2. Run:

   ```bash
   git status
   ```

3. Observe the message.
4. Navigate back to the correct repository.

---

## Part 4 — Documentation Commit (README)

### Goal

Treat documentation as part of normal development.

---

### Steps

1. In one existing repository, create:

   ```bash
   touch README.md
   ```

2. Add:

   ```md
   # Project Title

   A simple homepage project for practising Git.
   ```

3. Commit and push:

   ```bash
   git add .
   git commit -m "Add project README"
   git push
   ```

---

## Part 5 — Final Review and Verification

### Checklist

Confirm all of the following:

- At least **two repositories** exist on GitHub
- Each repository has:
  - Multiple commits
  - Clear, readable commit messages

- Commit history tells a logical story
- Git workflow feels repeatable:
  - edit → status → add → commit → push

If something does not match, stop and fix it before moving on.

---

## End of Unit 4 Lab

At this point:

- Git usage should feel familiar
- Errors should feel recoverable
- You should be able to use Git without a step-by-step script
