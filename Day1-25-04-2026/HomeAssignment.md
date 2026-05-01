# Homework — React

**Date:** 25-04-2026

---

## 1. What is the difference between a library and a framework?

**Answer:**  
The main distinction is who controls the program flow, which is often called **Inversion of Control**.

- **Library:** Your code drives the application and invokes the library as needed.
- **Framework:** The framework defines the overall structure and calls your code at designated points.

**Examples:**

- React → Library (focused on building UI)
- Angular → Framework (includes routing, state management, and more)

---

## 2. What is the current version of React?

**Answer:**  
React is currently at **version 19 (19.2.5)**.

**Important improvements:**

- Actions → Easier form handling and mutation updates
- `use` hook → Better support for asynchronous workflows
- Improved Server Components → Faster rendering and better scalability
- Reduced boilerplate → Cleaner code with less repetition

---

## 3. What are the folder structures in a React project and their use cases?

**Answer:**  
A common layout inside the `src/` directory looks like this:

- `assets/` → Stores images, fonts, icons, and SVG files
- `components/` → Houses reusable UI components
- `configs/` → Contains configuration settings and environment data
- `hooks/` → Custom hooks that can be reused across components
- `context/` → Provides shared state using React Context
- `services/` → Handles API requests and external integrations
- `utils/` → Utility functions and helpers
- `styles/` → CSS or other styling resources
- `App.jsx` → Main application component
- `main.jsx` → Entry point that renders `App` into the DOM

**Why this layout?**  
It helps keep the project organized, easier to understand, and scalable as the app grows.

---

## 4. What is the difference between Create React App and Vite?

**Answer:**

CRA and Vite both scaffold React projects, but they use different build strategies.

**Create React App (CRA):**

- Built on Webpack
- Bundles the whole app before launching the dev server
- Can feel slower for startup and rebuilds in bigger apps

**Vite:**

- Uses native ES Modules in the browser
- Loads code on demand during development
- Uses esbuild for very fast hot reloads

| Feature       | Create React App (CRA) | Vite               |
| ------------- | ---------------------- | ------------------ |
| Tooling       | Webpack-based          | ES Modules-based   |
| Dev Startup   | Slower                 | Fast               |
| Hot Reload    | Moderate               | Very fast          |
| Build Process | Full bundle first      | On-demand bundling |
| Modernity     | Traditional            | Modern tooling     |

**Conclusion:**  
Vite is generally faster and better optimized for modern React development.

---

## 5. What is the difference between SPA and MPA?

**Answer:**

**SPA (Single Page Application):**

- Uses one HTML page for the app
- Updates content dynamically with JavaScript
- Avoids full page refreshes

**MPA (Multi Page Application):**

- Loads a new HTML page for each navigation action
- Relies on the server to serve each page

| Feature         | SPA                   | MPA                          |
| --------------- | --------------------- | ---------------------------- |
| Page Reload     | No                    | Yes                          |
| Routing         | Client-side           | Server-side                  |
| Initial Load    | Usually slower        | Usually faster               |
| Navigation      | Generally faster      | Can be slower                |
| SEO             | Needs extra setup     | More straightforward         |
| User Experience | App-like              | Traditional website behavior |

**Examples:**

- SPA → React, Angular
- MPA → Classic multi-page websites and many online stores

**Use Cases:**

- SPA → Web apps, dashboards, interactive tools
- MPA → Content sites, blogs, SEO-focused platforms

---

## 6. What is Reconciliation, Virtual DOM, and Diffing Algorithm?

**Answer:**

These terms describe how React updates the UI with minimum work.

**Virtual DOM (VDOM):**  
A lightweight copy of the real DOM kept in memory. React compares it instead of manipulating the browser DOM directly.

**Diffing Algorithm:**  
When state or props change, React builds a new Virtual DOM and compares it to the previous version to find what changed.

**Reconciliation:**  
The process of syncing the real DOM with the Virtual DOM by applying only the necessary updates.

**Update flow:**

1. State or props change
2. React creates a new Virtual DOM tree
3. The diffing algorithm compares old and new trees
4. React determines the minimal set of differences
5. The real DOM is updated accordingly

**Why it matters:**  
This approach minimizes unnecessary DOM changes and improves app performance.

---
