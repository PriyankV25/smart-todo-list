# Smart To-Do List

A lightweight, responsive to-do list built with plain HTML, CSS, and JavaScript. It runs directly in your browser: no installation, dependencies, server, or build step required.

[Open the app source](./index.html) · [Features](#features) · [Run it](#run-the-app) · [How it works](#how-it-works) · [Copilot's role](#github-copilots-role)

![HTML5](https://img.shields.io/badge/HTML5-single--file-orange?logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-responsive-blue?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-yellow?logo=javascript&logoColor=black)
![Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)

## Contents

- [Features](#features)
- [Run the app](#run-the-app)
- [Publish with GitHub Pages](#publish-with-github-pages)
- [How it works](#how-it-works)
- [Try it out](#try-it-out)
- [GitHub Copilot's role](#github-copilots-role)
- [Project structure](#project-structure)

## Features

- Add tasks with the **Add Task** button or the **Enter** key.
- Complete and un-complete tasks with checkboxes.
- Delete individual tasks or clear all completed tasks.
- Filter the list by **All**, **Active**, or **Completed**.
- See total, active, and completed task counts.
- Keep tasks between visits using browser `localStorage`.
- Get a friendly empty state, whitespace validation, and accessible status messages.
- Use a responsive dark interface with keyboard-visible focus indicators.

<details>
<summary>What is included?</summary>

Everything is self-contained in [`index.html`](./index.html): the page markup, styles, and application logic. There are no external libraries, APIs, frameworks, fonts, or backend services.

</details>

## Run the app

1. Download or clone this repository.
2. Open `index.html` in a modern web browser.
3. Add a task and try the task controls.

There is no compile or build command. `index.html` is the finished application, not a generated build artifact. Browser storage is local to the browser and origin where the page is opened.

## Publish with GitHub Pages

You can host the app as a public website from this repository:

1. Push the project files, including `index.html`, to a GitHub repository.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose the branch containing the files and the repository root (`/`) as the folder, then save.
5. Follow the Pages link shown in repository settings once deployment completes.

GitHub Pages serves the static files directly; no build workflow is needed.

## How it works

The app uses standard browser features:

1. On startup, JavaScript reads the saved task array from `localStorage`.
2. Submitting the form trims the input and rejects it if it is empty.
3. Tasks are represented as objects with an `id`, `text`, and `completed` flag.
4. The interface is rendered from the task array. Filter selection changes which tasks are shown without changing the saved list.
5. Adding, completing, deleting, or clearing tasks updates the array and saves it back to `localStorage`.

Saved tasks use the storage key `smart-todo-list.tasks`. If browser storage is unavailable or saved data is invalid, the app reports the issue and remains usable for the current page session.

## Try it out

- [ ] Add a task with the button.
- [ ] Add another task by pressing Enter.
- [ ] Try submitting spaces only; no task should be added.
- [ ] Complete a task, then check the **Completed** and **Active** filters.
- [ ] Delete a task and use **Clear completed**.
- [ ] Refresh the page and confirm remaining tasks are still there.
- [ ] Resize the browser window to check the responsive layout.

The checkboxes above are a manual test checklist; tick them in your own copy as you test.

## GitHub Copilot's role

GitHub Copilot, an AI coding assistant, helped create this application from the requested feature and design requirements. It assisted with writing the single-file HTML structure, responsive dark theme, task interactions, local storage handling, and accessibility details. The resulting app was then exercised in a browser for task creation, validation, filtering, completion, deletion, clearing, and persistence after refresh.

Copilot is a development aid, not a runtime dependency: the published application does not call Copilot or any AI service. As with any AI-assisted code, review and test changes before relying on them.

## Project structure

| File | Purpose |
| --- | --- |
| [`index.html`](./index.html) | Complete application: HTML, CSS, and vanilla JavaScript |
| `README.md` | Project overview, run instructions, and documentation |

---

Built with HTML, CSS, JavaScript, and a little help from GitHub Copilot.
