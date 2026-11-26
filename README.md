# TaskFlow — HTMX & Tailwind CSS To-Do Application

A sleek, hypermedia-driven To-Do List web application built with **HTMX** and **Tailwind CSS**. TaskFlow demonstrates modern HATEOAS (Hypermedia as the Engine of Application State) patterns in a single, zero-build HTML file by pairing real HTMX attributes with a lightweight client-side XHR mock server and `localStorage` persistence.

---

## Features

- **Hypermedia-Driven UI (HTMX)**:
  - Full CRUD operations powered by `hx-get`, `hx-post`, `hx-put`, and `hx-delete`.
  - **Out-of-Band (`hx-swap-oob`) Updates**: Automatically refreshes task counters, filter badges, and the completion progress bar whenever tasks are added, toggled, edited, or deleted.
  - **Debounced Live Search**: Real-time filtering via `hx-trigger="keyup changed delay:200ms"`.
  - **Inline Editing**: Swaps individual task rows into an inline edit form on demand without full-page reloads.
- **Rich Task Management**:
  - **Priority Levels**: `High`, `Medium`, and `Low` color-coded badges.
  - **Category Tags**: Organize tasks under `Work`, `Design`, `Personal`, or `Urgent`.
  - **Smart Due Dates**: Automatic labels and highlights for *Today*, *Tomorrow*, and *Overdue* tasks.
  - **Quick Filters**: Switch between `All`, `Active`, `Completed`, and `High Priority` views, plus a one-click *Clear Completed* action.
- **Polished Styling & UX (Tailwind CSS)**:
  - Glassmorphic card layout with responsive design for desktop and mobile.
  - Built-in **Dark & Light Mode** toggle with persisted theme preference.
  - Smooth CSS swap transitions using `.htmx-swapping` and `.htmx-added` hooks.

---

## Tech Stack

| Layer | Technology |
| :--- | :--- |
| **Hypermedia / Interactivity** | [HTMX](https://htmx.org/) (v2.x via CDN) |
| **Styling & Theming** | [Tailwind CSS](https://tailwindcss.com/) (Play CDN) |
| **Backend Simulation** | Custom client-side `XMLHttpRequest` interceptor returning HTML fragments |
| **Persistence** | Browser `localStorage` |

---

## Getting Started

No build tools, bundlers, or backend servers are required.

1. **Download or Save** the generated `index.html` file to your computer.
2. **Open in a Browser**: Double-click `index.html` or serve it locally with any static file server:
   ```bash
   # Using Python
   python3 -m http.server 8080

   # Or using Node.js (npx)
   npx serve .
