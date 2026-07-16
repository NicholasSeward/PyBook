# Git/GitHub Basics

In this class, all assignments will be submitted through GitHub. This is standard practice in the software industry and will give you valuable, real-world skills.

## What is Git?

- Git is a version control system: it tracks changes in your code over time.
- You can think of it as a very powerful "undo/redo" system that also lets you share work with others.
- Git runs locally on your computer.

## What is GitHub?

- GitHub is a website that hosts Git repositories in the cloud.
- It lets you store, share, and collaborate on projects.
- For this class, your GitHub repository is the official record of your work—if it's not pushed to GitHub, it's not submitted.

## Ways to Use GitHub

There are multiple ways to interact with Git and GitHub:

### Command Line (git commands)
- The most flexible and powerful way.
- Requires installing Git on your computer.
- You run commands like:
  ```
  git clone <repo-url>
  git pull
  git add .
  git commit -m "message"
  git push
  ```
- This is the "professional" way, but can be intimidating at first.

### GitHub Desktop
- A beginner-friendly application for Windows and macOS.
- Lets you do most Git tasks (clone, commit, push, pull) with buttons instead of commands.
- Good option if you're working locally and don't want to use the command line.

### GitHub Codespaces
- Runs a full coding environment in the cloud—accessible in your browser.
- You don't need to install anything on your computer.
- Great for keeping things consistent across different machines (no risk of "forgetting to push" on your laptop and being stuck in the lab).
- Codespaces uses VS Code as the editor, so it looks and feels like a modern IDE.

## Setup Notes

### If using the Command Line (git commands):
- You will need a GitHub account.
- You must install Git and configure it with your GitHub username and email.
- First time only:
  ```
  git config --global user.name "Your Name"
  git config --global user.email "your@email.com"
  ```

### If using GitHub Desktop (local app):
- You will need a GitHub account.
- No command line setup is required.
- Download here: https://desktop.github.com
- GitHub Desktop handles cloning, committing, pushing, and pulling through its graphical interface.

### If using GitHub Codespaces (cloud-based):
- Just log into GitHub, open your repository, and click "Code → Open with Codespaces."
- A complete development environment runs directly in your browser.
- No local installation or setup required.

## Beginner Pitfall: Clones Everywhere

It's possible to clone your repository onto multiple computers (your laptop, a lab machine, a codespace).

Beginners often forget which copy is up to date.

**Rule of thumb:**
- Always push before switching to another machine.
- Always pull as the first thing when you open a new session.

To keep it simple, many students find it easiest to stick to just one main environment at first (GitHub Desktop OR Codespaces).

## A Simple Flow to Start

1. Clone your repository (first time only).
2. Pull before you start working.
3. Edit your files.
4. Commit your changes with a clear message.
5. Push your changes to GitHub.
6. Repeat steps 2–5 each work session.
