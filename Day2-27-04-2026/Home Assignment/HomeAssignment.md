# Homework — React

**Date:** 27-04-2026

---

## 1. What is the difference between Class Components and Function Components?

**Answer:**

React components can be implemented as either **Class Components** or **Function Components**. Both create UI elements, but they use different syntax and patterns.

---

### Function Components:

- Built as plain JavaScript functions
- Return JSX directly from the function body
- Use **Hooks** like `useState` and `useEffect` for state and side effects
- Do not need the `this` keyword
- Typically shorter and easier to follow

---

### Class Components:

- Defined using ES6 class syntax
- Extend `React.Component`
- Manage state with `this.state`
- Use lifecycle methods such as `componentDidMount`, `componentDidUpdate`
- Often require binding `this` for callbacks

---

## Comparison Table

| Feature        | Function Component      | Class Component              |
| -------------- | ----------------------- | ---------------------------- |
| Definition     | JavaScript function     | ES6 class                    |
| State          | `useState` Hook         | `this.state`                 |
| Lifecycle      | `useEffect` Hook        | Lifecycle methods            |
| this Keyword   | Not required            | Required                     |
| Syntax         | Concise                 | More verbose                 |
| Code Length    | Shorter                 | Longer                       |
| Reusability    | Easier with custom Hooks| More complex (HOCs, render props)|
| Learning Curve | Lower                   | Higher                       |
| Modern Usage   | Common choice           | Mostly legacy                |
| Performance    | Efficient with hooks    | Similar in most cases        |

---

## Key Points

- Function components are **easier to read and write**
- Hooks allow function components to handle **state and lifecycle behavior**
- Class components are **older style code** and are less common in new projects
- Today, most React codebases **favor function components**

---

## Conclusion

Function components are the preferred approach for new React work because they are simpler to maintain and adapt. Class components are still valid, but they are usually reserved for existing legacy code.

---
