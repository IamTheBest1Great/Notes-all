# Comprehensive Frontend Interview Questions (JavaScript & React)
ALL notes and interview questions here - https://github.com/priya42bagde
This document compiles a wide range of frontend interview questions covering JavaScript, React, Redux, system design, performance, HTML/CSS, coding problems, and behavioral topics. The questions are sourced from the provided notes and the GitHub repository [priya42bagde](https://github.com/priya42bagde). They are categorized for easy navigation and study.

---

## 📚 Table of Contents
- [JavaScript Core Concepts](#javascript-core-concepts)
- [JavaScript Advanced & Internals](#javascript-advanced--internals)
- [Asynchronous JavaScript](#asynchronous-javascript)
- [JavaScript Coding & Polyfills](#javascript-coding--polyfills)
- [React Core](#react-core)
- [React Hooks & Performance](#react-hooks--performance)
- [React Advanced & Internals](#react-advanced--internals)
- [Redux & State Management](#redux--state-management)
- [Frontend System Design](#frontend-system-design)
- [Performance Optimization](#performance-optimization)
- [HTML & CSS](#html--css)
- [Browser & DOM APIs](#browser--dom-apis)
- [Coding Problems (DSA & Algorithms)](#coding-problems-dsa--algorithms)
- [Low-Level Design (LLD) / Component Design](#low-level-design-lld--component-design)
- [Real-World Scenarios & Problem Solving](#real-world-scenarios--problem-solving)
- [Behavioral & Hiring Manager Questions](#behavioral--hiring-manager-questions)
- [Frontend Architecture & Team Leadership](#frontend-architecture--team-leadership)
- [Testing, CI/CD & Developer Experience](#testing-cicd--developer-experience)
- [Miscellaneous / General](#miscellaneous--general)

---

## JavaScript Core Concepts

### Variables & Scope
1. Difference between `var`, `let`, and `const`.
2. What is scope? Explain global, function, and block scope.
3. What is hoisting?
4. Why do we get `ReferenceError: Cannot access 'x' before initialization`?
5. What is the Temporal Dead Zone (TDZ)?
6. Difference between `undefined` and `not defined`.
7. Truthy and falsy values in JavaScript.

### Functions & Execution
8. Function declaration vs function expression.
9. Arrow functions vs regular functions – differences in `this` and syntax.
10. What is the call stack?
11. What is an execution context?
12. Explain closures with a real-world example.
13. How does the `this` keyword behave in arrow functions, class methods, and event handlers?
14. Explain `call`, `apply`, and `bind` with use cases. Implement polyfills.

### Data Types & Coercion
15. Primitive vs reference types.
16. Type coercion and equality: `==` vs `===`.
17. Difference between `null` and `undefined`.
18. How to check if a variable is an array?

### Objects & Prototypes
19. How does prototypal inheritance work?
20. Prototype chain vs class inheritance.
21. `Object.create()` and ES6 classes.
22. Shallow copy vs deep copy – how to achieve each? Modern solution: `structuredClone()`.

### Arrays & Iteration
23. Difference between `map`, `filter`, and `forEach`.
24. `map` vs `forEach` – when to use which?
25. `slice` vs `splice`.
26. `find`, `some`, `every` – use cases.
27. Sorting arrays with custom comparators.

### ES6+ Features
28. Destructuring (objects and arrays).
29. Spread and rest operators.
30. Template literals.
31. Modules (`import`/`export`).
32. Optional chaining (`?.`) and nullish coalescing (`??`).
33. WeakMap vs Map – real use cases.
34. Symbols and iterators.

---

## JavaScript Advanced & Internals

1. Explain the JavaScript event loop in detail. Microtasks vs macrotasks.
2. How do JavaScript engines optimize code? (JIT, hidden classes, inline caching)
3. How does garbage collection work in V8?
4. What is the difference between `setTimeout` and `setInterval`?
5. Implement a custom Promise (conceptually).
6. How does the browser rendering pipeline work? (HTML → CSS → Layout → Paint → Composite)
7. What causes memory leaks in frontend applications? How to prevent them?
8. Explain `AbortController` and request cancellation.
9. Cross-tab communication methods: `BroadcastChannel`, `storage` events, `postMessage`.
10. Event delegation at scale – benefits and pitfalls.
11. Why does JavaScript have closures? (data privacy, hooks, callbacks, memoization)
12. `var`, `let`, `const` – interviewers want hoisting + TDZ explanation.

---

## Asynchronous JavaScript

1. Synchronous vs asynchronous programming.
2. Callback functions – what are they? Callback hell.
3. Promises – states (pending, fulfilled, rejected) and how they work.
4. `async` / `await` – how they simplify promises.
5. Event loop: Why does a Promise run before `setTimeout`? (Microtasks vs macrotasks)
6. Implement `Promise.all`, `Promise.race`, `Promise.allSettled` from scratch.
7. Difference between microtask queue and callback (macrotask) queue.
8. How to handle multiple independent API calls efficiently? (`Promise.all`, `allSettled`)
9. What are the advantages of `Promise.allSettled` over `Promise.all`?

---

## JavaScript Coding & Polyfills

1. Implement `Promise.all` from scratch.
2. Implement debounce and throttle functions.
3. Implement a deep clone function (deep copy).
4. Write a polyfill for `call`, `apply`, and `bind`.
5. Implement `map`, `reduce`, `filter` from scratch.
6. Flatten a nested array without using `Array.flat()`.
   - Input: `[1,2,3,[4,5,6,[7,8,[10,11]]],9]`
   - Output: `[1,2,3,4,5,6,7,8,10,11,9]`
7. Find the first repeating character in a string (e.g., `"success"` → `"c"`).
8. Find the first non-repeating character in a string.
9. Currying for infinite sum: `sum(10)(20)(30)() → 60`, `sum(10)(20)(30)(40)(50)(60)() → 210`.
10. Find sum of numbers without using a for loop (using `reduce` or recursion).
11. Given an array of users, find all active user ids:
    - `users = [{ id: 1, active: true }, { id: 2, active: false }]`
    - `users = [{ id: 1, active: true }, null, {}, { id: 2, active: false }]`
12. Solve a problem using only `map()` and `filter()` (no loops). Explain edge cases.
13. Implement a custom hook like `useDebounce` or `useFetch` (React).

---

## React Core

1. What is React JS?
2. Why React.js? What problems does it solve?
3. What is JSX and how is it rendered in the browser?
4. What are components? Functional vs class components.
5. What are state and props? Difference between them.
6. What is a hook? Why were hooks introduced?
7. If we have `var`, `let`, `const`, why do we need state variables?
8. What is re-rendering, and why does it happen?
9. What is reconciliation in React? How does the diffing algorithm work?
10. Why are keys important in lists? What happens if keys are unstable?
11. What is the difference between `Router` and `Link` in React Router?
12. What is routing in React? How does it work?
13. Controlled vs uncontrolled components – explain with examples.
14. What is prop drilling? Problems and solutions.
15. How do you pass parent data to a deeply nested child (e.g., 5th child)?
16. Difference between `useMemo` and `React.memo`.
17. Difference between `useMemo` and `useCallback`.
18. What happens if a component wrapped in `memo()` has its own state changes?
19. What happens if a child uses `memo()` and parent props don't change?
20. What is state batching? What changed in React 18 regarding batching?
21. Explain `useEffect` deeply: cleanup function, dependency array pitfalls.
22. Difference between `useEffect`, `useLayoutEffect`, and `useInsertionEffect`.
23. What problems does `useMemo` actually solve? When should you NOT use it?
24. When would you use `React.memo`?
25. Build a custom hook like `useDebounce` or `useFetch`.

---

## React Advanced & Internals

1. How does React Fiber architecture change rendering?
2. What is concurrent rendering? When does it help vs hurt?
3. Explain React Server Components vs Client Components.
4. What is hydration? How do hydration mismatches occur?
5. How does React Context work? When can it hurt performance?
6. Scenario: Context API causes frequent re-renders – why and how to fix?
7. What is code splitting? How does `React.lazy` work internally?
8. How does tree shaking work in modern bundlers?
9. What is the purpose of `Suspense` beyond lazy loading?
10. Explain the concept of "controlled re-render boundaries".
11. How would you build a custom hook library?
12. What are the hidden reasons a component re-renders even when props don't change? (parent re-render, inline functions/objects, context changes)
13. How does React 18's automatic batching work?
14. How do you handle real-time updates efficiently in React?

---

## Redux & State Management

1. What is Redux and why is it used?
2. What problems does Redux solve in large React applications?
3. Explain the Redux data flow (action → reducer → store → view).
4. What is Redux Toolkit and why is it recommended over plain Redux?
5. Explain the flow of Redux Toolkit.
6. How does Redux Toolkit work internally?
7. What is `createSlice()` and what does it contain? (name, initialState, reducers)
8. Explain reducers and `extraReducers` – when to use each?
9. What is `createAsyncThunk()` and why is it used?
10. How does async flow work in Redux Toolkit?
11. Where and why have you used Redux Toolkit in your projects?
12. Redux vs Context API vs Zustand – how do you decide in a large-scale application?
13. Compare Redux, MobX, and Recoil for enterprise-scale state management (pros and cons).
14. How would you design a state management solution for a complex analytics/dashboard app?

---

## Frontend System Design

### Design Problems
1. Design an autocomplete search with debouncing, caching, and race condition handling.
2. Design an infinite scrolling feed (virtualization, pagination, loading states).
3. Design a real-time dashboard with multiple data sources.
4. Design an e-commerce frontend with filters (price, category, rating) and scalable state updates.
5. Design a notification/toast system with queueing, auto-dismiss, and priority handling.
6. Design a search with typeahead/autocomplete.
7. Design a config-driven form renderer using a JSON schema.
8. Design a file upload component with progress tracking and chunked uploads.
9. Design a data table with sorting, filtering, pagination, and performance trade-offs.
10. Design an image gallery with lazy loading and skeleton placeholders.
11. Design a carousel that can handle 1000+ images efficiently.
12. Design a drag-and-drop interface (e.g., kanban board).
13. Design a multi-step form with validation.
14. Design a theme-able, extensible component library.
15. Design a state management solution for a complex app.
16. How would you implement Server-Side Rendering (SSR) for a React application? When to use SSR, SSG, ISR?

### Architecture & Strategy
17. How would you structure a micro-frontend architecture enabling team autonomy and independent releases?
18. How do you manage shared libraries and dependencies in a large monorepo?
19. How would you design SSR/SSG/hydration strategy for a React app?
20. How do you handle breaking API changes safely on the frontend?
21. What is your approach to multi-tenant frontend applications?
22. How do you implement dark mode across an app?
23. How do you ensure accessibility beyond ARIA labels?

---

## Performance Optimization

1. How would you optimize a React application rendering 100k+ items in a list? (virtualization, windowing, pagination)
2. What strategies would you use to improve page load time for a global audience? (CDN, lazy loading, code splitting, image optimization)
3. How do you debug a performance bottleneck in a React app using DevTools? (Profiler, Performance tab)
4. How would you improve Web Vitals (LCP, CLS, INP)?
5. What causes unnecessary re-renders in React? How to avoid them? (memoization, stable props, colocated state)
6. Explain techniques for dynamic code splitting and lazy loading in multi-route SPAs.
7. How do you optimize images and fonts?
8. What are preload, prefetch, and priority hints?
9. How do you analyze bundle size and fix tree shaking failures?
10. What is the difference between virtualization and windowing? Trade-offs.
11. How do you avoid layout thrashing?
12. CPU vs memory bottlenecks – how to identify and fix?
13. Edge caching vs CDN caching strategies.
14. How would you handle a large dataset without blocking the main thread? (Web Workers, virtualization)
15. How do you detect and prevent memory leaks in long-running SPAs?

---

## HTML & CSS

### HTML
1. What are semantic tags in HTML? Give examples.
2. What is the difference between `div` and `span`?
3. How do you create a form with validation?
4. What is the purpose of the `meta` tags?
5. Explain the difference between `localStorage`, `sessionStorage`, and cookies.

### CSS
6. What is a pseudo-class? Give examples (`:hover`, `:nth-child`, etc.).
7. How to center an element horizontally? Vertically? Both?
8. Difference between `relative` and `absolute` positioning.
9. What is Flexbox? Explain main concepts.
10. How would you create a responsive layout with CSS Grid?
11. What are container queries?
12. How do you implement a CSS animation? How to debug janky animations on mobile?
13. Explain the concept of specificity in CSS.
14. What are CSS custom properties (variables)?
15. How do you handle dark mode theming?

### Inline Layout
16. How to place 5 `div`s in a row without using flex, margin, or padding? (Hint: `display: inline-block`)

---

## Browser & DOM APIs

1. How do you select and manipulate DOM elements?
2. Explain event bubbling and capturing.
3. What is event delegation? When would you use it?
4. How does `addEventListener` work? How to remove listeners?
5. What are the different ways to handle forms in JavaScript?
6. Difference between `LocalStorage` and `SessionStorage`.
7. How do you work with cookies in JavaScript?
8. Explain the `IntersectionObserver` API and its use cases (lazy loading, infinite scroll).
9. What is the `ResizeObserver`?
10. How do you implement drag and drop using native APIs?
11. How does the `history` API work for routing?
12. What is the `AbortController` used for?

---

## Coding Problems (DSA & Algorithms)

1. Maximum sum subarray (Kadane's algorithm).
2. Sliding window maximum.
3. Merge k sorted linked lists.
4. Detect a cycle in a linked list.
5. Longest palindromic substring.
6. Design and implement an LRU Cache.
7. Flatten a nested array (recursive/iterative).
8. Find first repeating character in a string.
9. Find first non-repeating character.
10. Implement debounce and throttle.
11. Implement deep clone.
12. Implement `Promise.all`.
13. Currying for infinite sum.
14. Given an array of users with nested null/objects, filter active user ids.

---

## Low-Level Design (LLD) / Component Design

### Component Design Fundamentals
1. Design a Todo List application with add, edit, delete, and mark-as-complete.
2. Design a Tabs component that supports dynamic content loading and async data.
3. Design an Accordion component – should it allow single or multiple panels open? Why?
4. Design a Star Rating component – how would you support half or partial ratings?
5. Design a Progress Bar / Stepper with configurable steps and validation logic.
6. Design a Modal/Dialog component – focus trapping, accessibility, backdrop behavior.
7. Design a Toggle / Switch component – controlled vs uncontrolled patterns.
8. Design a Dropdown / Select component with keyboard navigation and accessibility.

### State, Data & UI Systems
9. Design a Posts with Comments system – how do you manage deeply nested data?
10. Design an E-commerce Filter system (price, category, rating) with scalable state updates.
11. Design a Config-Driven Form Renderer using a JSON schema.
12. Design a Notification / Toast system with queueing, auto-dismiss, and priority.
13. Design a Search with Autocomplete / Typeahead – debouncing, caching, race conditions.

### Performance & Optimization
14. Design a Carousel that can handle 1000+ images efficiently.
15. Implement Virtual Scrolling for very large lists.
16. Design an Image Gallery with lazy loading and skeleton placeholders.
17. Design a Data Table with sorting, filtering, pagination, and performance trade-offs.
18. Implement Debouncing and Throttling in a search or scroll-heavy component.
19. Design a File Upload component with progress tracking and chunked uploads.
20. How do you detect and prevent memory leaks in long-running SPAs?

### Architecture & Scalability
21. How would you design a theme-able, extensible component library?
22. How do you structure a large-scale React application across multiple teams?
23. Design a state management solution for a complex analytics/dashboard app.
24. How would you implement SSR for a React application?

---

## Real-World Scenarios & Problem Solving

1. **Memory Leak**: You notice a memory leak in a production SPA – how do you identify and fix it?
2. **Library Upgrade**: A component breaks when upgrading a library version – how do you manage dependencies?
3. **UI Glitches**: Users report intermittent UI glitches in different browsers – how do you troubleshoot?
4. **Peak Traffic Failure**: A critical UI feature fails during peak traffic – how do you mitigate?
5. **Debugging Production**: How would you debug production issues methodically? (reproduce, logs, profiling, rollback)
6. **When NOT to use JavaScript**: CPU-heavy tasks, long-running blocking logic – use backend or workers.
7. **Authentication Token Expiry**: How do you handle token expiry mid-session? (interceptors, refresh token, queue requests)
8. **Multiple API Calls**: How to load a dashboard with independent APIs efficiently? (`Promise.all`, `allSettled`)
9. **Large List Rendering**: 10k+ items cause UI lag – optimization strategies.
10. **Context Re-renders**: Context API causes frequent re-renders – why and how to fix?
11. **Component Re-renders Unexpectedly**: Component re-renders even when props don't change – hidden reasons.
12. **Poor SEO & Slow TTI**: React app has poor SEO and slow TTI – frontend-level solutions.
13. **Real-time Updates**: How to handle real-time updates efficiently in React?
14. **A/B Testing**: How to implement A/B testing without affecting current users?
15. **CSS Animation Jank**: A CSS animation is janky on mobile – how to identify and fix?

---

## Behavioral & Hiring Manager Questions

1. Explain a frontend project you built end-to-end.
2. Describe the hardest production bug you fixed.
3. How do you balance performance vs feature delivery?
4. How do you handle disagreements in technical decisions?
5. When did you get stuck while using React, and how did you fix it?
6. Have you led a team? What is your current role?
7. Have you handled task distribution and requirement breakdown?
8. Have you been involved in architectural or technical decision-making?
9. How do you mentor juniors through code walkthroughs, tech spikes, and 1:1s?
10. Do you have any questions for me?

---

## Frontend Architecture & Team Leadership

1. How would you structure a micro-frontend architecture for team autonomy?
2. Describe your process for creating and enforcing a scalable design system across distributed teams.
3. How do you manage shared libraries and dependencies in a monorepo?
4. What is your framework for identifying, prioritizing, and reducing technical debt?
5. How do you implement scalable code review workflows (linters, pre-commit hooks, pair programming)?
6. How do you handle versioning of UI contracts?
7. What tools and practices do you use for frontend observability, error tracking, and performance monitoring?
8. How do you ensure secure handling of sensitive user data on the client side? (XSS, CSP, CSRF, token leakage)
9. How would you design a migration strategy from a legacy jQuery app to modern React/Next.js?
10. How do you integrate feature flags (LaunchDarkly, etc.) in React ecosystems?
11. How do you coordinate deployments with DevOps teams? Handling multiple pods with different versions.

---

## Testing, CI/CD & Developer Experience

1. How would you implement a robust frontend monitoring and logging system?
2. What are flaky test detection strategies?
3. Explain contract testing between frontend and backend.
4. What is visual regression testing? How would you implement it?
5. How would you design a CI/CD pipeline for frontend apps with staging, canary, and blue-green deployments?
6. What is chaos engineering for frontend?
7. How do you ensure code quality with testing? (unit, integration, e2e)
8. Have you worked with Storybook? How do you use it?

---

## Miscellaneous / General

1. What is the difference between CSR, SSR, SSG, and ISR?
2. What are Web Vitals and why do they matter?
3. How do you build PWAs with service workers, manifest files, and offline-first experiences?
4. Compare WebSockets, SSE, and WebRTC for real-time features.
5. How do you handle offline-first apps with IndexedDB, background sync, and conflict resolution?
6. What is your strategy for fluid responsive design using CSS Grid, Flexbox, and container queries?
7. How do you extract spacing, font sizes, and colors from Figma designs?
8. How do you approach developing a reusable component from a design?
9. What is atomic design methodology?
10. How do you check page load behavior using browser developer tools? What metrics do you look at?
11. How would you check cumulative layout shifts (CLS) on a page?
12. What tools do you use for frontend performance analysis? (Lighthouse, WebPageTest, Chrome DevTools)

---

*This document is a living compilation. Use it to prepare for frontend interviews at all levels – from junior to senior/staff.*


## 1. Variables & Scope

### Difference between `var`, `let`, and `const`

| Feature | `var` | `let` | `const` |
|---------|------|------|--------|
| **Scope** | Function-scoped | Block-scoped `{ }` | Block-scoped `{ }` |
| **Hoisting** | Hoisted and initialized with `undefined` | Hoisted but not initialized (TDZ) | Hoisted but not initialized (TDZ) |
| **Re-declaration** | Allowed in same scope | Not allowed | Not allowed |
| **Re-assignment** | Allowed | Allowed | Not allowed (for primitives; for objects, properties can be modified) |
| **Global property** | Becomes property of `window` (in browsers) | Does not create property on `window` | Does not create property on `window` |

```javascript
// var example
console.log(x); // undefined (hoisted)
var x = 5;
var x = 10; // allowed

// let example
// console.log(y); // ReferenceError: Cannot access 'y' before initialization
let y = 20;
// let y = 30; // SyntaxError: Identifier 'y' has already been declared

// const example
const z = 40;
// z = 50; // TypeError: Assignment to constant variable
const obj = { a: 1 };
obj.a = 2; // allowed – object is not frozen
```

### What is scope? Explain global, function, and block scope.

**Scope** defines where variables and functions are accessible during runtime.

- **Global scope**: Variables declared outside any function or block are globally accessible. In browsers, global variables become properties of `window`.
- **Function scope**: Variables declared with `var`, `let`, or `const` inside a function are accessible only within that function.
- **Block scope**: Introduced with ES6; `let` and `const` are block-scoped, meaning they are confined to the nearest `{ }` (e.g., `if`, `for`, `while`). `var` ignores block scope.

```javascript
if (true) {
  var a = 1;   // function-scoped (or global)
  let b = 2;   // block-scoped
  const c = 3; // block-scoped
}
console.log(a); // 1
// console.log(b); // ReferenceError: b is not defined
// console.log(c); // ReferenceError: c is not defined
```

### What is hoisting?

Hoisting is JavaScript's behavior where variable and function declarations are moved to the top of their containing scope during compilation.

- `var` declarations are hoisted and initialized with `undefined`.
- `let` and `const` are hoisted but remain uninitialized (in the Temporal Dead Zone).
- Function declarations are hoisted entirely (both name and body), so they can be called before they appear in code.

```javascript
console.log(foo); // undefined (var)
var foo = 'bar';

sayHello(); // "Hello!" – function declaration hoisted
function sayHello() { console.log("Hello!"); }

// Arrow function (assigned to var) – only variable is hoisted, not the assignment
// sayHi(); // TypeError: sayHi is not a function
var sayHi = () => console.log("Hi");
```

### Why do we get `ReferenceError: Cannot access 'x' before initialization`?

This error occurs when trying to access a `let` or `const` variable before its declaration line is executed, because they are hoisted but not initialized. The time between entering the scope and the actual declaration is the **Temporal Dead Zone (TDZ)**.

### What is the Temporal Dead Zone (TDZ)?

The TDZ is the period from entering a block scope until the variable is declared with `let` or `const`. During this time, accessing the variable results in a `ReferenceError`. It prevents accidental use of variables before they are ready.

```javascript
{
  // TDZ for a starts here
  // console.log(a); // ReferenceError
  let a = 10; // TDZ ends here
}
```

### Difference between `undefined` and `not defined`

- **`undefined`** is a primitive value automatically assigned to variables that have been declared but not yet assigned a value. It is a valid value.
- **`not defined`** is a reference error thrown when trying to access a variable that was never declared in the current scope.

```javascript
let a;
console.log(a); // undefined
console.log(b); // ReferenceError: b is not defined
```

### Truthy and falsy values in JavaScript

In JavaScript, every value is either **truthy** or **falsy** when evaluated in a boolean context (e.g., `if` condition).

**Falsy values** (only 8):
- `false`
- `0`, `-0`, `0n` (BigInt zero)
- `""`, `''`, ` `` ` (empty string)
- `null`
- `undefined`
- `NaN`

Everything else is **truthy**, including:
- `"0"`, `"false"`, `" "` (non-empty strings)
- `[]` (empty array)
- `{}` (empty object)
- `function() {}`
- `Infinity`, `-Infinity`

### Additional Questions for Variables & Scope

**Q: What is the difference between `let` and `const` in terms of object mutation?**  
A: `const` prevents reassignment of the variable, but if the variable holds an object, the object's properties can still be mutated. To freeze an object, use `Object.freeze()`.

**Q: Can you declare a `let` variable in a `switch` block without curly braces?**  
A: Yes, but each `case` shares the same block scope. Using `let` in multiple cases without a block will cause a redeclaration error. It's safer to wrap cases in `{}`.

**Q: What is the difference between implicit and explicit global variables?**  
A: Explicit globals are declared with `var` in global scope. Implicit globals occur when assigning to an undeclared variable (without `var`, `let`, `const`) – this creates a property on the global object (but is not hoisted). In strict mode, this throws an error.

**Q: How does strict mode affect scoping and variable declaration?**  
A: Strict mode (`"use strict"`) prevents accidental globals, disallows duplicate parameter names, and changes the behavior of `this` in functions (defaults to `undefined` instead of `window`).

---

## 2. Functions & Execution

### Function declaration vs function expression

| | Function Declaration | Function Expression |
|---|----------------------|----------------------|
| **Syntax** | `function name() {}` | `const name = function() {};` or arrow function |
| **Hoisting** | Entire declaration hoisted (can call before definition) | Only variable declaration hoisted (not assignment) |
| **Name** | Has a named identifier | Can be anonymous or named |
| **Usage** | Can be used anywhere in its scope | Must be defined before invocation |

```javascript
// Function declaration – hoisted
foo(); // "foo"
function foo() { console.log("foo"); }

// Function expression – not hoisted
// bar(); // TypeError: bar is not a function
const bar = function() { console.log("bar"); };
```

### Arrow functions vs regular functions – differences in `this` and syntax

**Syntax differences:**
- Arrow functions omit the `function` keyword; can have implicit return if single expression.
- If only one parameter, parentheses can be omitted.

**`this` binding:**
- **Regular functions**: `this` is determined by how the function is called (dynamic binding). In global context, `this` refers to the global object (or `undefined` in strict mode). As a method, `this` refers to the object. As a constructor, `this` refers to the new instance.
- **Arrow functions**: Do not have their own `this`; they capture `this` from the surrounding lexical scope at the time they are defined (lexical binding). They are not suitable for methods that need their own `this` (e.g., event handlers, object methods that need the object), but they are great for callbacks that need to preserve the outer `this`.

```javascript
const obj = {
  name: "Alice",
  regular: function() { console.log(this.name); },
  arrow: () => console.log(this.name) // `this` is global (or undefined in strict mode)
};
obj.regular(); // "Alice"
obj.arrow();   // undefined (or error in strict mode)

// Arrow functions cannot be used as constructors (no `prototype` property)
// new (() => {}); // TypeError
```

### What is the call stack?

The **call stack** is a data structure that records function calls. When a function is invoked, a frame is pushed onto the stack. When it returns, it's popped. It helps track the execution order and current point of execution. Stack overflow occurs when too many frames are pushed (e.g., infinite recursion).

### What is an execution context?

An **execution context** is an abstract environment where JavaScript code is evaluated and executed. There are three types:
- **Global execution context**: Default context, creates global object and `this`.
- **Function execution context**: Created when a function is called; includes local variables, arguments, and `this`.
- **Eval execution context** (rare).

Each execution context has two phases:
1. **Creation phase**: Hoisting occurs, scope chain is built, `this` is determined.
2. **Execution phase**: Code is executed line by line.

The call stack holds a stack of execution contexts.

### Explain closures with a real-world example

A **closure** is the combination of a function and the lexical environment within which that function was declared. The inner function retains access to variables from its outer scope even after the outer function has returned.

**Real-world example: Counter factory**

```javascript
function createCounter() {
  let count = 0;
  return function() {
    count++;
    return count;
  };
}

const counter = createCounter();
console.log(counter()); // 1
console.log(counter()); // 2
// `count` is private and persists because the inner function closes over it.
```

**Use cases:** Data privacy, function factories, partial application, maintaining state in callbacks.

### How does the `this` keyword behave in arrow functions, class methods, and event handlers?

- **Arrow functions**: Lexical `this` (inherits from enclosing context). In an event listener, if you use an arrow function, `this` will refer to the enclosing context (e.g., the component, not the DOM element). In a class method, if defined as an arrow property, `this` is bound to the instance.
- **Class methods**: Regular class methods have `this` bound to the instance when called as `obj.method()`. But if passed as a callback, `this` can be lost; solutions: bind, arrow method, or using `.bind` in constructor.
- **Event handlers (DOM)**: In regular function event handlers, `this` refers to the element that received the event. In arrow functions, `this` is lexical (often the window or surrounding context). Use regular function if you need the element.

### Explain `call`, `apply`, and `bind` with use cases. Implement polyfills.

All three are used to control the `this` value in functions.

- **`call(thisArg, arg1, arg2, ...)`**: Invokes the function immediately with a given `this` and arguments passed individually.
- **`apply(thisArg, [argsArray])`**: Same as `call`, but arguments are passed as an array.
- **`bind(thisArg, ...args)`**: Returns a new function with the `this` bound permanently; can be called later.

**Use cases:**
- Borrowing methods: e.g., `Array.prototype.slice.call(arguments)`
- Function currying: `const multiply = (a,b) => a*b; const double = multiply.bind(null, 2);`
- Event handlers: ensure `this` refers to the class instance.

**Polyfills:**

```javascript
// call polyfill
Function.prototype.myCall = function(context, ...args) {
  context = context || globalThis;
  const uniqueId = Symbol(); // avoid property collision
  context[uniqueId] = this;
  const result = context[uniqueId](...args);
  delete context[uniqueId];
  return result;
};

// apply polyfill
Function.prototype.myApply = function(context, argsArray) {
  context = context || globalThis;
  const uniqueId = Symbol();
  context[uniqueId] = this;
  const result = context[uniqueId](...argsArray);
  delete context[uniqueId];
  return result;
};

// bind polyfill (simplified)
Function.prototype.myBind = function(context, ...boundArgs) {
  const fn = this;
  return function(...args) {
    return fn.apply(context, boundArgs.concat(args));
  };
};
```

### Additional Questions for Functions & Execution

**Q: What is the difference between `function` and `=>` in terms of `arguments` object?**  
A: Regular functions have an `arguments` array-like object containing passed arguments. Arrow functions do not have their own `arguments`; they inherit from the parent scope.

**Q: What is a higher-order function?**  
A: A function that takes another function as an argument or returns a function (e.g., `map`, `filter`, `reduce`).

**Q: What is memoization?**  
A: An optimization technique that caches the results of expensive function calls. Implemented using closures to store a cache object.

**Q: What is the event loop? How does it work with the call stack and task queue?**  
A: The event loop continuously checks if the call stack is empty; if so, it takes tasks from the task queue (or microtask queue) and pushes them onto the stack. Asynchronous operations (setTimeout, promises) are handled via the event loop.

---

## 3. Data Types & Coercion

### Primitive vs reference types

- **Primitive types**: `string`, `number`, `bigint`, `boolean`, `undefined`, `symbol`, `null`. Stored directly in the variable (value). Immutable. Copied by value.
- **Reference types**: `object`, `array`, `function`, `date`, etc. Stored as reference (memory address). Mutable. Copied by reference.

```javascript
let a = 10;
let b = a; // copy value
b = 20;
console.log(a); // 10

let obj1 = { x: 1 };
let obj2 = obj1; // copy reference
obj2.x = 2;
console.log(obj1.x); // 2
```

### Type coercion and equality: `==` vs `===`

- **`==` (abstract equality)**: Performs type coercion if the operands are of different types. Tries to convert them to a common type before comparison.
- **`===` (strict equality)**: Compares both value and type; no coercion.

**Coercion rules (for `==`):**
- If one operand is number and other is string, convert string to number.
- If one is boolean, convert boolean to number (true→1, false→0).
- If one is object and other is primitive, call `ToPrimitive` on object.
- `null == undefined` is `true`; `null === undefined` is `false`.
- `NaN` is not equal to anything (including `NaN`). Use `isNaN()` or `Number.isNaN()`.

**Best practice:** Always use `===` except when intentionally checking for `null` or `undefined` with `==`.

### Difference between `null` and `undefined`

- **`undefined`**: A variable that has been declared but not assigned a value; also the default return of functions without `return`. Type `undefined`.
- **`null`**: An assignment value representing "no value" or "empty". Type `object` (historical bug) but it's a primitive.

```javascript
let a; // undefined
let b = null; // null
typeof null; // "object"
typeof undefined; // "undefined"
```

### How to check if a variable is an array?

- `Array.isArray(arr)` – preferred, works across realms.
- `arr instanceof Array` – may fail if array comes from another iframe.
- `Object.prototype.toString.call(arr) === '[object Array]'` – reliable fallback.

### Additional Questions for Data Types & Coercion

**Q: What is `NaN` and how to check for it?**  
A: `NaN` (Not-a-Number) is a numeric value that represents an unrepresentable number. `typeof NaN === 'number'`. Use `isNaN(value)` (coerces) or `Number.isNaN(value)` (strict, recommended) to check.

**Q: What is the difference between `Object.is()` and `===`?**  
A: `Object.is()` is similar to `===` but handles two special cases: `Object.is(NaN, NaN)` is `true` and `Object.is(-0, +0)` is `false`. `===` does the opposite.

**Q: How does JavaScript handle implicit coercion in arithmetic?**  
A: The `+` operator prefers string concatenation if either operand is a string; other arithmetic operators (`-`, `*`, `/`) coerce to numbers. Example: `'5' + 3` → `'53'`, `'5' - 3` → `2`.

**Q: What are symbols used for?**  
A: Symbols are unique and immutable primitives used as object property keys to avoid name collisions. They are not enumerable in `for...in` loops, but can be accessed via `Object.getOwnPropertySymbols()`.

---

## 4. Objects & Prototypes

### How does prototypal inheritance work?

Every JavaScript object has an internal `[[Prototype]]` (accessible via `__proto__` or `Object.getPrototypeOf()`). When accessing a property, JavaScript first looks on the object itself; if not found, it follows the prototype chain until it reaches `null`. This is the basis of inheritance.

```javascript
const parent = { a: 1 };
const child = Object.create(parent);
child.b = 2;
console.log(child.a); // 1 (from parent)
console.log(child.b); // 2
console.log(child.toString); // from Object.prototype
```

### Prototype chain vs class inheritance

- **Prototype chain**: JavaScript's native inheritance mechanism based on linking objects. You can create objects that inherit from other objects directly (using `Object.create`).
- **Class inheritance** (ES6): Syntactic sugar over prototypal inheritance. It provides a familiar class syntax (`class`, `extends`, `super`) but still uses prototypes under the hood.

```javascript
// Prototype chain
function Animal(name) { this.name = name; }
Animal.prototype.speak = function() { console.log(`${this.name} makes noise.`); };

function Dog(name) { Animal.call(this, name); }
Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog;
Dog.prototype.speak = function() { console.log(`${this.name} barks.`); };

// ES6 Classes
class Animal {
  constructor(name) { this.name = name; }
  speak() { console.log(`${this.name} makes noise.`); }
}
class Dog extends Animal {
  speak() { console.log(`${this.name} barks.`); }
}
```

### `Object.create()` and ES6 classes

- **`Object.create(proto, propertiesObject)`**: Creates a new object with the specified prototype object. Useful for simple inheritance without constructors.
- **ES6 classes**: Provide a more declarative way to define constructors and methods. They also support static methods, private fields (with `#`), and mixins.

### Shallow copy vs deep copy – how to achieve each? Modern solution: `structuredClone()`

- **Shallow copy**: Copies only the top-level properties. Nested objects are still referenced.
  - Methods: spread operator `{...obj}`, `Object.assign({}, obj)`, `Array.slice()`, `[...arr]`.
- **Deep copy**: Recursively copies all nested structures, resulting in a fully independent copy.
  - Traditional: `JSON.parse(JSON.stringify(obj))` – limited (fails with functions, undefined, symbols, circular references).
  - Modern: `structuredClone(obj)` – built-in (available in browsers and Node 17+), handles most types (including Dates, Maps, Sets, arrays, objects, but not functions, DOM elements, etc.).
  - Libraries: Lodash `_.cloneDeep()`.

```javascript
const original = { a: 1, b: { c: 2 } };
const shallow = { ...original };
shallow.b.c = 3;
console.log(original.b.c); // 3 (changed)

const deep = structuredClone(original);
deep.b.c = 4;
console.log(original.b.c); // 3 (unchanged)
```

### Additional Questions for Objects & Prototypes

**Q: How do you check if a property exists in an object?**  
A: 
- `'prop' in obj` – checks own and inherited properties.
- `obj.hasOwnProperty('prop')` – checks own properties only.
- `Object.hasOwn(obj, 'prop')` – modern alternative.

**Q: What is the difference between `Object.keys()`, `Object.values()`, `Object.entries()`?**  
A: They return arrays of own enumerable property keys, values, and key-value pairs, respectively.

**Q: What is property descriptor?**  
A: An object that describes attributes of a property: `value`, `writable`, `enumerable`, `configurable`. Can be retrieved with `Object.getOwnPropertyDescriptor(obj, prop)`.

**Q: How to create a truly immutable object?**  
A: 
- `Object.freeze(obj)` – prevents adding/removing properties and makes all existing properties non-writable (shallow).
- For deep freeze, recursively freeze.
- Using `const` only prevents reassignment, not mutation.

---

## 5. Arrays & Iteration

### Difference between `map`, `filter`, and `forEach`

| Method | Return | Purpose |
|--------|--------|---------|
| `map` | New array of same length | Transform each element |
| `filter` | New array of filtered elements | Select elements based on condition |
| `forEach` | `undefined` | Execute side effects (e.g., logging, updating external variables) |

```javascript
const arr = [1, 2, 3];
const doubled = arr.map(x => x * 2); // [2,4,6]
const evens = arr.filter(x => x % 2 === 0); // [2]
arr.forEach(x => console.log(x)); // logs 1,2,3
```

### `map` vs `forEach` – when to use which?

- Use `map` when you need to transform an array into another array of the same length.
- Use `forEach` when you just need to iterate and perform side effects (like updating UI, printing, or accumulating with external variable). `forEach` does not return a value.

### `slice` vs `splice`

| Method | Returns | Mutates original? | Purpose |
|--------|---------|------------------|---------|
| `slice(start, end)` | New array (shallow copy) | No | Extract a portion without modifying |
| `splice(start, deleteCount, ...items)` | Array of removed elements | Yes | Remove/replace/add elements at any position |

```javascript
const arr = [1, 2, 3, 4];
const sliceRes = arr.slice(1, 3); // [2,3]
console.log(arr); // [1,2,3,4]

const spliceRes = arr.splice(1, 2, 'a', 'b'); // [2,3] removed
console.log(arr); // [1,'a','b',4]
```

### `find`, `some`, `every` – use cases

- **`find(callback)`**: Returns the first element that satisfies the condition; else `undefined`. Use when you need the element itself.
- **`some(callback)`**: Returns `true` if at least one element satisfies the condition; else `false`. Use to check existence.
- **`every(callback)`**: Returns `true` if all elements satisfy the condition; else `false`. Use to validate all.

```javascript
const users = [{ id: 1, active: true }, { id: 2, active: false }];
const user = users.find(u => u.id === 2); // { id:2, active:false }
const hasActive = users.some(u => u.active); // true
const allActive = users.every(u => u.active); // false
```

### Sorting arrays with custom comparators

`sort()` without a comparator converts elements to strings and sorts lexicographically. Provide a comparator function that returns negative, zero, or positive.

```javascript
const numbers = [3, 1, 10, 2];
numbers.sort((a, b) => a - b); // ascending [1,2,3,10]
numbers.sort((a, b) => b - a); // descending

const objects = [{ name: 'John', age: 30 }, { name: 'Jane', age: 25 }];
objects.sort((a, b) => a.age - b.age); // sort by age
```

### Additional Questions for Arrays & Iteration

**Q: How do you flatten an array?**  
A: `flat()` (ES2019): `[1,[2,3]].flat()` → `[1,2,3]`. For deeper, pass depth or `Infinity`. Polyfill via `reduce` and recursion.

**Q: What is the difference between `reduce` and `reduceRight`?**  
A: Both accumulate values; `reduce` goes left-to-right, `reduceRight` goes right-to-left.

**Q: How to remove duplicates from an array?**  
A: Using `Set`: `[...new Set(array)]`. For objects, use `Map` with a unique key.

**Q: How to convert an array-like object to an array?**  
A: `Array.from(arrayLike)`, `[...arrayLike]`, or `Array.prototype.slice.call(arrayLike)`.

**Q: What are the performance implications of `map`, `filter`, `reduce` chains?**  
A: Each method creates a new array and loops through the entire array. For large arrays, consider using a single `reduce` to avoid multiple passes.

---

## 6. ES6+ Features

### Destructuring (objects and arrays)

Allows extracting values from arrays or properties from objects into distinct variables.

```javascript
// Array destructuring
const [first, second] = [1, 2];
const [a, , c] = [1, 2, 3]; // a=1, c=3
const [x, ...rest] = [1, 2, 3]; // x=1, rest=[2,3]

// Object destructuring
const { name, age } = { name: 'John', age: 30 };
const { name: personName, city = 'Unknown' } = obj; // alias and default
const { ...other } = obj; // rest properties
```

### Spread and rest operators

- **Spread (`...`)**: Expands elements (array, object) into individual items.
- **Rest (`...`)**: Collects remaining elements into an array or object.

```javascript
// Spread
const arr = [1, 2];
const newArr = [...arr, 3]; // [1,2,3]
const obj = { a: 1, b: 2 };
const newObj = { ...obj, c: 3 }; // { a:1, b:2, c:3 }

// Rest
function sum(...numbers) { return numbers.reduce((acc, n) => acc + n, 0); }
const [head, ...tail] = [1, 2, 3]; // head=1, tail=[2,3]
```

### Template literals

Strings using backticks `` ` `` that support:
- Multi-line strings
- Interpolation `${expression}`

```javascript
const name = 'Alice';
const greeting = `Hello, ${name}!
Welcome to JavaScript.`;
```

### Modules (`import`/`export`)

ES6 modules allow splitting code into separate files. Use `export` to expose functions/variables, and `import` to consume them.

```javascript
// math.js
export const add = (a, b) => a + b;
export default function multiply(a, b) { return a * b; }

// app.js
import multiply, { add } from './math.js';
```

### Optional chaining (`?.`) and nullish coalescing (`??`)

- **Optional chaining**: Safely access nested properties without worrying about `null` or `undefined`. Short-circuits to `undefined` if any part is nullish.
- **Nullish coalescing**: Returns the right-hand side only when the left is `null` or `undefined` (not for falsy values like `0` or `''`).

```javascript
const user = { profile: { name: 'John' } };
console.log(user.profile?.age); // undefined (no error)
console.log(user.address?.city); // undefined

const value = 0;
const result = value ?? 'default'; // 0 (since 0 is not null/undefined)
const result2 = value || 'default'; // 'default' (since 0 is falsy)
```

### `WeakMap` vs `Map` – real use cases

- **`Map`**: Keys can be any type; holds strong references to keys. Keys are iterable and the map can be cleared. Use for general key-value storage.
- **`WeakMap`**: Keys must be objects; holds weak references to keys, so if there's no other reference, the key can be garbage collected. Not iterable, no `size` property. Use cases:
  - Storing private data for objects without memory leaks.
  - Caching where you don't want to prevent garbage collection.
  - Storing metadata for DOM elements.

```javascript
// WeakMap example: private data
const privateData = new WeakMap();
class Person {
  constructor(name) {
    privateData.set(this, { name });
  }
  getName() {
    return privateData.get(this).name;
  }
}
```

### Symbols and iterators

- **Symbols**: Unique identifiers. Often used to define well-known symbols like `Symbol.iterator` to make objects iterable.
- **Iterators**: Objects with a `next()` method returning `{ value, done }`. Iterable objects have a `[Symbol.iterator]` method.

```javascript
// Making an object iterable
const range = {
  start: 1,
  end: 5,
  [Symbol.iterator]() {
    let current = this.start;
    const end = this.end;
    return {
      next() {
        if (current <= end) return { value: current++, done: false };
        else return { done: true };
      }
    };
  }
};
for (let num of range) console.log(num); // 1 2 3 4 5
```

### Additional Questions for ES6+ Features

**Q: What is the difference between `for...in` and `for...of`?**  
A: `for...in` iterates over enumerable property keys (including prototype chain). `for...of` iterates over iterable values (arrays, strings, maps, sets) – it's the recommended way for arrays.

**Q: What are generators?**  
A: Functions that can be paused and resumed, defined with `function*`. They return an iterator that yields values via `yield`. Useful for lazy evaluation, infinite sequences, and async flows.

**Q: What is the difference between `Promise` and `async/await`?**  
A: Promises are objects representing eventual completion; `async/await` is syntactic sugar over promises, making asynchronous code look synchronous. `await` can only be used inside `async` functions.

**Q: What are private fields in classes?**  
A: Using `#` prefix (e.g., `#privateField`). They are truly private, cannot be accessed outside the class, and are not enumerable.

**Q: What is the `Array.prototype.at()` method?**  
A: `at(index)` allows negative indexing to access elements from the end: `arr.at(-1)` returns last element, equivalent to `arr[arr.length-1]`.

---

## JavaScript Advanced & Internals

### Explain the JavaScript event loop in detail. Microtasks vs macrotasks.

The **event loop** is the mechanism that enables JavaScript’s non‑blocking, asynchronous behavior despite being single‑threaded. It continuously checks the **call stack** and **task queues**, moving tasks to the stack when it’s empty.

There are two main queues:
- **Macrotask (Callback) queue**: Contains tasks like `setTimeout`, `setInterval`, `setImmediate`, I/O events, and UI rendering.
- **Microtask queue**: Contains tasks like `Promise` callbacks (`.then`, `.catch`, `.finally`), `queueMicrotask`, and `MutationObserver`. Microtasks have higher priority.

**Process:**
1. Execute all synchronous code (call stack frames).
2. When the stack is empty, the event loop first processes **all** microtasks in the microtask queue (in FIFO order). If new microtasks are added during this phase, they are also processed before moving to macrotasks.
3. After microtasks are exhausted, one macrotask is taken from the macrotask queue and executed.
4. The browser may perform rendering (if needed) between macrotask cycles.
5. Repeat.

```javascript
console.log('1');
setTimeout(() => console.log('2'), 0);
Promise.resolve().then(() => console.log('3'));
console.log('4');
// Output: 1,4,3,2
// Explanation: synchronous 1,4; microtask (promise) 3; macrotask 2.
```

### How do JavaScript engines optimize code? (JIT, hidden classes, inline caching)

Modern engines (V8, SpiderMonkey) use **Just‑In‑Time (JIT)** compilation, combining interpretation and compilation.

- **Interpretation**: Code starts as bytecode, executed by an interpreter (Ignition in V8). This allows fast startup.
- **JIT compilation**: Hot functions (executed many times) are compiled to machine code by optimizing compilers (TurboFan in V8) for faster execution.
- **Hidden classes**: Instead of dynamic dictionary lookups, objects with the same shape (property names and order) share a hidden class, enabling fast property access via fixed offsets.
- **Inline caching**: When a property is accessed repeatedly, the engine caches the property location based on the hidden class, avoiding repeated lookup overhead.

### How does garbage collection work in V8?

V8 uses a **generational, mark‑and‑sweep** garbage collector.

- **Heap**: Divided into **young generation** (newly allocated objects) and **old generation** (objects that survive multiple collections).
- **Minor GC (Scavenger)**: Runs frequently on the young generation, copying surviving objects to a survivor space. Very fast.
- **Major GC (Mark‑Sweep / Mark‑Compact)**: Runs less often on the old generation. It marks reachable objects, sweeps unreachable ones, and compacts to reduce fragmentation.
- **Incremental marking**: Long pauses are avoided by interleaving marking with JavaScript execution.

### What is the difference between `setTimeout` and `setInterval`?

| | `setTimeout` | `setInterval` |
|---|--------------|---------------|
| **Execution** | Runs once after a delay | Runs repeatedly at a fixed interval |
| **Drift** | No cumulative delay | Can drift if execution time exceeds interval |
| **Cancellation** | `clearTimeout(id)` | `clearInterval(id)` |

**Important**: Both schedule macrotasks. If the callback takes longer than the interval, `setInterval` may queue multiple calls back‑to‑back, causing congestion. A common pattern to avoid this is recursive `setTimeout`:

```javascript
function repeat() {
  // do work
  setTimeout(repeat, delay);
}
```

### Implement a custom Promise (conceptually).

A custom Promise implementation involves managing states (`pending`, `fulfilled`, `rejected`), handling `.then` callbacks (both onFulfilled and onRejected), and supporting chaining and async resolution.

```javascript
class MyPromise {
  constructor(executor) {
    this.state = 'pending';
    this.value = undefined;
    this.handlers = []; // stores { onFulfilled, onRejected }

    const resolve = (value) => {
      if (this.state !== 'pending') return;
      this.state = 'fulfilled';
      this.value = value;
      this.handlers.forEach(h => this._runHandler(h));
    };

    const reject = (reason) => {
      if (this.state !== 'pending') return;
      this.state = 'rejected';
      this.value = reason;
      this.handlers.forEach(h => this._runHandler(h));
    };

    try {
      executor(resolve, reject);
    } catch (err) {
      reject(err);
    }
  }

  _runHandler(handler) {
    if (this.state === 'pending') {
      this.handlers.push(handler);
      return;
    }
    const cb = this.state === 'fulfilled' ? handler.onFulfilled : handler.onRejected;
    if (!cb) {
      // propagate
      const next = this.state === 'fulfilled' ? handler.resolve : handler.reject;
      next(this.value);
      return;
    }
    try {
      const result = cb(this.value);
      handler.resolve(result);
    } catch (err) {
      handler.reject(err);
    }
  }

  then(onFulfilled, onRejected) {
    return new MyPromise((resolve, reject) => {
      this._runHandler({ onFulfilled, onRejected, resolve, reject });
    });
  }

  catch(onRejected) {
    return this.then(null, onRejected);
  }

  // static methods (all, race) would be added similarly
}
```

### How does the browser rendering pipeline work? (HTML → CSS → Layout → Paint → Composite)

The browser rendering pipeline typically involves these steps (per frame):

1. **Parsing HTML** → DOM tree, CSS → CSSOM tree.
2. **Style**: Combine DOM and CSSOM into a render tree (visible nodes with computed styles).
3. **Layout (Reflow)**: Calculate geometry (position, size) for each node in the render tree.
4. **Paint**: Fill in pixels – draw text, colors, images, borders, shadows (creates layers).
5. **Composite**: Combine layers (GPU) and draw to screen.

**Optimizations**:
- Changing properties that affect layout (width, height, position) trigger **layout + paint + composite**.
- Changing paint‑only properties (color, background) trigger **paint + composite**.
- Changing transform/opacity (on a separate layer) triggers **composite only** (the fastest).

### What causes memory leaks in frontend applications? How to prevent them?

Common memory leaks:
- **Global variables**: Accidentally creating globals (`function foo() { x = 10; }`) – use `'use strict'`.
- **Forgotten timers**: `setInterval` / `setTimeout` not cleared.
- **Event listeners** not removed when elements are removed.
- **Closures** holding references to large objects.
- **Detached DOM elements**: Removing elements but still referencing them in JavaScript.
- **Out of scope references**: Variables captured in closures but no longer needed.

**Prevention**:
- Use `let`/`const` and strict mode.
- Clean up timers and listeners in lifecycle hooks (e.g., `componentWillUnmount`, `useEffect` cleanup).
- Avoid storing large data in global scope.
- Use weak references (`WeakMap`, `WeakSet`) for caching or metadata.
- Profile with Chrome DevTools (Memory tab) to identify leaks.

### Explain AbortController and request cancellation.

`AbortController` provides a standard way to cancel asynchronous operations (e.g., fetch, timers). It works via an `AbortSignal` attached to the operation.

```javascript
const controller = new AbortController();
const signal = controller.signal;

fetch('/api', { signal })
  .then(response => response.json())
  .catch(err => {
    if (err.name === 'AbortError') console.log('Fetch aborted');
  });

// Cancel after 1 second
setTimeout(() => controller.abort(), 1000);
```

**Use cases**: Cancelling fetch requests when a component unmounts, implementing debounced search, aborting expensive computations.

### Cross‑tab communication methods: BroadcastChannel, storage events, postMessage.

- **BroadcastChannel**: Simple, same‑origin communication. Create a channel and post messages; all tabs listening receive them.
  ```javascript
  const bc = new BroadcastChannel('my_channel');
  bc.postMessage('Hello');
  bc.onmessage = (e) => console.log(e.data);
  ```
- **localStorage / sessionStorage events**: When storage changes in one tab, a `storage` event fires in other tabs (except the one that made the change). Useful for cross‑tab sync.
- **postMessage** (with `window.opener` or `window.parent`): For communication between a parent window and an iframe, or between windows opened via `window.open()`.
- **SharedWorker**: A background script that can communicate with multiple tabs.

### Event delegation at scale – benefits and pitfalls.

**Event delegation** attaches a single event listener to a parent element instead of many children. The event bubbles up, and the target can be checked.

**Benefits**:
- Reduces memory usage (fewer listeners).
- Works for dynamically added elements.
- Simplifies code.

**Pitfalls**:
- Performance if the parent has many descendants; event target checks become O(n) if not optimized.
- May catch events you don’t want if not filtered properly.
- Not all events bubble (e.g., `focus`, `blur`, `load` can bubble with `useCapture`).
- Need to be careful with `stopPropagation()` – it can break delegation.

**Scalable approach**: Use a library or implement a throttled event handler; filter targets with `closest()` for specific selectors.

### Why does JavaScript have closures? (data privacy, hooks, callbacks, memoization)

Closures are a fundamental feature that allows functions to “remember” their lexical scope even when executed outside that scope.

**Use cases**:
- **Data privacy**: Encapsulate variables not exposed globally (e.g., module pattern, factory functions).
- **React Hooks**: `useState` and `useEffect` rely on closures to maintain state across renders.
- **Callbacks**: Preserve context in asynchronous operations.
- **Memoization**: Cache results of expensive functions (e.g., `useMemo`, `_.memoize`).
- **Function factories**: Create functions with pre‑configured arguments.

### `var`, `let`, `const` – interviewers want hoisting + TDZ explanation.

**Hoisting**: JavaScript moves declarations to the top of their scope during compilation.
- `var` → declaration hoisted, initialized with `undefined`.
- `let` / `const` → declaration hoisted, but not initialized. Access before initialization results in `ReferenceError` due to the **Temporal Dead Zone (TDZ)**.

**TDZ**: The period from entering a block scope until the declaration is executed. Within TDZ, the variable exists but cannot be accessed.

**Example**:
```javascript
console.log(a); // undefined (var)
var a = 1;

console.log(b); // ReferenceError (TDZ)
let b = 2;
```

---

## Asynchronous JavaScript

### Synchronous vs asynchronous programming.

- **Synchronous**: Code executes sequentially; each line waits for the previous to finish. Long operations block the thread.
- **Asynchronous**: Operations (I/O, timers) are delegated, and the program continues without waiting. When the operation completes, a callback or promise is executed via the event loop.

### Callback functions – what are they? Callback hell.

A **callback** is a function passed as an argument to another function, to be executed later. Callback hell refers to deeply nested callbacks that become hard to read and maintain:

```javascript
getUser((user) => {
  getOrders(user.id, (orders) => {
    getOrderDetails(orders[0].id, (details) => {
      // ...
    });
  });
});
```

Solutions: Promises, `async/await`.

### Promises – states (pending, fulfilled, rejected) and how they work.

A Promise represents the eventual completion (or failure) of an asynchronous operation.

- **pending**: Initial state, neither fulfilled nor rejected.
- **fulfilled**: Operation completed successfully, value available via `.then`.
- **rejected**: Operation failed, reason available via `.catch`.

Promises are **immutable** once settled. They support chaining: `.then` returns a new promise, enabling sequential composition.

### `async / await` – how they simplify promises.

`async` functions always return a promise. `await` pauses the function execution until the promise settles, then resumes with the resolved value (or throws if rejected). It allows writing asynchronous code that looks synchronous.

```javascript
async function fetchData() {
  try {
    const response = await fetch('/api');
    const data = await response.json();
    console.log(data);
  } catch (err) {
    console.error(err);
  }
}
```

### Event loop: Why does a Promise run before setTimeout? (Microtasks vs macrotasks)

Promises’ callbacks (`.then`, `.catch`) are **microtasks**, while `setTimeout` callbacks are **macrotasks**. After each macrotask (including the initial script execution), the event loop drains the entire microtask queue before taking the next macrotask. Therefore, a settled promise’s callback always runs before any scheduled `setTimeout`.

### Implement `Promise.all`, `Promise.race`, `Promise.allSettled` from scratch.

**Promise.all**:
```javascript
Promise.myAll = function(promises) {
  return new Promise((resolve, reject) => {
    if (!Array.isArray(promises)) reject(new TypeError('Not an array'));
    const results = new Array(promises.length);
    let completed = 0;
    if (promises.length === 0) resolve(results);
    promises.forEach((p, i) => {
      Promise.resolve(p).then(
        val => {
          results[i] = val;
          completed++;
          if (completed === promises.length) resolve(results);
        },
        err => reject(err)
      );
    });
  });
};
```

**Promise.race**:
```javascript
Promise.myRace = function(promises) {
  return new Promise((resolve, reject) => {
    promises.forEach(p => {
      Promise.resolve(p).then(resolve, reject);
    });
  });
};
```

**Promise.allSettled**:
```javascript
Promise.myAllSettled = function(promises) {
  return new Promise(resolve => {
    const results = [];
    let remaining = promises.length;
    if (remaining === 0) resolve(results);
    promises.forEach((p, i) => {
      Promise.resolve(p).then(
        value => results[i] = { status: 'fulfilled', value },
        reason => results[i] = { status: 'rejected', reason }
      ).finally(() => {
        remaining--;
        if (remaining === 0) resolve(results);
      });
    });
  });
};
```

### Difference between microtask queue and callback (macrotask) queue.

- **Microtask queue**: High priority; processed after each macrotask until empty. Used for promise callbacks, `queueMicrotask`, `MutationObserver`.
- **Macrotask queue**: Lower priority; one task processed per event loop iteration after microtasks are done. Used for `setTimeout`, `setInterval`, I/O, UI rendering.

### How to handle multiple independent API calls efficiently? (`Promise.all`, `allSettled`)

- Use `Promise.all` when you need all to succeed or fail fast (reject on first error).
- Use `Promise.allSettled` when you want to know the outcome of each independent call, regardless of failures (e.g., analytics, fallback data).

### What are the advantages of `Promise.allSettled` over `Promise.all`?

`Promise.allSettled` never rejects; it always resolves with an array of objects describing each promise’s outcome. This is useful when you need to wait for multiple operations and handle errors individually, without failing the whole batch.

---

## JavaScript Coding & Polyfills

### Implement `Promise.all` from scratch (already covered above).

### Implement debounce and throttle functions.

**Debounce**: Delays function execution until after a period of inactivity. Useful for search inputs, window resize.
```javascript
function debounce(fn, delay) {
  let timer;
  return function(...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn.apply(this, args), delay);
  };
}
```

**Throttle**: Ensures a function is called at most once per interval. Useful for scroll events, button clicks.
```javascript
function throttle(fn, limit) {
  let inThrottle;
  return function(...args) {
    if (!inThrottle) {
      fn.apply(this, args);
      inThrottle = true;
      setTimeout(() => (inThrottle = false), limit);
    }
  };
}
```

### Implement a deep clone function (deep copy).

**Using `structuredClone` (modern)**:
```javascript
const clone = structuredClone(original);
```

**Manual implementation** (handles objects, arrays, dates, maps, sets, and cyclic references):
```javascript
function deepClone(obj, map = new WeakMap()) {
  if (obj === null || typeof obj !== 'object') return obj;
  if (map.has(obj)) return map.get(obj);
  let clone;
  if (obj instanceof Date) clone = new Date(obj);
  else if (obj instanceof Map) {
    clone = new Map();
    map.set(obj, clone);
    obj.forEach((val, key) => clone.set(deepClone(key, map), deepClone(val, map)));
    return clone;
  } else if (obj instanceof Set) {
    clone = new Set();
    map.set(obj, clone);
    obj.forEach(val => clone.add(deepClone(val, map)));
    return clone;
  } else if (obj instanceof Array) {
    clone = [];
    map.set(obj, clone);
    obj.forEach((item, i) => clone[i] = deepClone(item, map));
  } else {
    clone = {};
    map.set(obj, clone);
    for (let key in obj) {
      if (obj.hasOwnProperty(key)) clone[key] = deepClone(obj[key], map);
    }
  }
  return clone;
}
```

### Write a polyfill for `call`, `apply`, and `bind`.

**`call` polyfill** (already provided earlier, but here is a clean version):
```javascript
Function.prototype.myCall = function(context, ...args) {
  context = context ?? globalThis;
  const fnSymbol = Symbol();
  context[fnSymbol] = this;
  const result = context[fnSymbol](...args);
  delete context[fnSymbol];
  return result;
};
```

**`apply` polyfill**:
```javascript
Function.prototype.myApply = function(context, argsArray) {
  context = context ?? globalThis;
  const fnSymbol = Symbol();
  context[fnSymbol] = this;
  const result = context[fnSymbol](...argsArray);
  delete context[fnSymbol];
  return result;
};
```

**`bind` polyfill**:
```javascript
Function.prototype.myBind = function(context, ...boundArgs) {
  const fn = this;
  return function(...args) {
    return fn.apply(context, boundArgs.concat(args));
  };
};
```

### Implement `map`, `reduce`, `filter` from scratch.

**`map`**:
```javascript
Array.prototype.myMap = function(callback, thisArg) {
  const result = [];
  for (let i = 0; i < this.length; i++) {
    if (i in this) { // skip empty slots (sparse arrays)
      result.push(callback.call(thisArg, this[i], i, this));
    }
  }
  return result;
};
```

**`filter`**:
```javascript
Array.prototype.myFilter = function(callback, thisArg) {
  const result = [];
  for (let i = 0; i < this.length; i++) {
    if (i in this && callback.call(thisArg, this[i], i, this)) {
      result.push(this[i]);
    }
  }
  return result;
};
```

**`reduce`**:
```javascript
Array.prototype.myReduce = function(callback, initialValue) {
  let accumulator = initialValue;
  let startIndex = 0;
  if (arguments.length < 2) {
    if (this.length === 0) throw new TypeError('Reduce of empty array with no initial value');
    accumulator = this[0];
    startIndex = 1;
  }
  for (let i = startIndex; i < this.length; i++) {
    if (i in this) {
      accumulator = callback(accumulator, this[i], i, this);
    }
  }
  return accumulator;
};
```

### Flatten a nested array without using `Array.flat()`.

**Input**: `[1,2,3,[4,5,6,[7,8,[10,11]]],9]`  
**Output**: `[1,2,3,4,5,6,7,8,10,11,9]`

**Solution** (recursive):
```javascript
function flattenArray(arr) {
  let result = [];
  for (let item of arr) {
    if (Array.isArray(item)) {
      result.push(...flattenArray(item));
    } else {
      result.push(item);
    }
  }
  return result;
}
```

**Iterative with stack**:
```javascript
function flattenArrayIterative(arr) {
  const stack = [...arr];
  const result = [];
  while (stack.length) {
    const next = stack.pop();
    if (Array.isArray(next)) {
      stack.push(...next);
    } else {
      result.push(next);
    }
  }
  return result.reverse(); // because we popped from end
}
```

### Find the first repeating character in a string (e.g., "success" → "c").

```javascript
function firstRepeating(str) {
  const seen = new Set();
  for (let char of str) {
    if (seen.has(char)) return char;
    seen.add(char);
  }
  return null;
}
```

### Find the first non-repeating character in a string.

```javascript
function firstNonRepeating(str) {
  const count = new Map();
  for (let char of str) {
    count.set(char, (count.get(char) || 0) + 1);
  }
  for (let char of str) {
    if (count.get(char) === 1) return char;
  }
  return null;
}
```

### Currying for infinite sum: `sum(10)(20)(30)() → 60`, `sum(10)(20)(30)(40)(50)(60)() → 210`.

```javascript
function sum(x) {
  let total = x;
  function inner(y) {
    if (y === undefined) return total;
    total += y;
    return inner;
  }
  return inner;
}
// Usage: sum(10)(20)(30)() → 60
```

### Find sum of numbers without using a for loop (using reduce or recursion).

**Using reduce**:
```javascript
const arr = [1,2,3,4];
const sum = arr.reduce((acc, val) => acc + val, 0);
```

**Using recursion**:
```javascript
function sumRecursive(arr, index = 0) {
  if (index === arr.length) return 0;
  return arr[index] + sumRecursive(arr, index + 1);
}
```

### Given an array of users, find all active user ids.

**Array**: `users = [{ id: 1, active: true }, { id: 2, active: false }]`  
Also with `null`, `{}`, etc.

```javascript
function getActiveIds(users) {
  return users
    .filter(user => user && typeof user === 'object' && user.active === true)
    .map(user => user.id);
}
```

### Solve a problem using only `map()` and `filter()` (no loops). Explain edge cases.

**Example**: Given an array of numbers, get the squares of even numbers.  
```javascript
const numbers = [1,2,3,4,5];
const result = numbers
  .filter(n => n % 2 === 0)
  .map(n => n * n);
// result: [4,16]
```
**Edge cases**: Empty array → returns empty array. Sparse arrays: `filter` and `map` skip empty slots. Non‑numeric values should be handled by the predicate (e.g., `typeof n === 'number'`). Ensure `map` is called after `filter` to avoid unnecessary processing.

### Implement a custom hook like `useDebounce` or `useFetch` (React).

**`useDebounce`**:
```javascript
import { useState, useEffect } from 'react';

function useDebounce(value, delay) {
  const [debouncedValue, setDebouncedValue] = useState(value);
  useEffect(() => {
    const handler = setTimeout(() => setDebouncedValue(value), delay);
    return () => clearTimeout(handler);
  }, [value, delay]);
  return debouncedValue;
}
```

**`useFetch`**:
```javascript
function useFetch(url, options = {}) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);

  useEffect(() => {
    const abortController = new AbortController();
    const signal = abortController.signal;

    fetch(url, { ...options, signal })
      .then(res => {
        if (!res.ok) throw new Error('Network response was not ok');
        return res.json();
      })
      .then(data => {
        setData(data);
        setLoading(false);
      })
      .catch(err => {
        if (err.name !== 'AbortError') {
          setError(err);
          setLoading(false);
        }
      });

    return () => abortController.abort();
  }, [url]);

  return { data, loading, error };
}
```

---

## React Core

### What is React JS?

React is a JavaScript library for building user interfaces, developed by Facebook. It allows developers to create reusable UI components and manage the view layer of applications using a declarative paradigm. React uses a virtual DOM to optimize rendering and improve performance.

### Why React.js? What problems does it solve?

React solves several frontend challenges:
- **Declarative UI**: Instead of imperatively manipulating the DOM, you describe what the UI should look like for a given state. React handles updates efficiently.
- **Component‑based architecture**: Encourages reusability, maintainability, and separation of concerns.
- **Efficient updates**: Virtual DOM diffing minimizes costly DOM manipulations.
- **Unidirectional data flow**: Makes data flow predictable and easier to debug.
- **Ecosystem and community**: Rich tooling, libraries (React Router, Redux), and strong community support.

### What is JSX and how is it rendered in the browser?

JSX is a syntax extension for JavaScript that looks like HTML but gets transformed into regular JavaScript function calls (`React.createElement`). The browser cannot interpret JSX directly; it is transpiled by tools like Babel into `React.createElement` calls, which produce plain JavaScript objects representing the virtual DOM. These objects are then rendered to the actual DOM by React.

Example:
```jsx
const element = <h1>Hello, world!</h1>;
// Transpiles to:
const element = React.createElement('h1', null, 'Hello, world!');
```

### What are components? Functional vs class components.

Components are the building blocks of a React application. They accept inputs (props) and return React elements describing what should appear on screen.

- **Functional components**: Plain JavaScript functions that accept props and return JSX. They are simpler, support hooks, and are the preferred way to write components today.
- **Class components**: ES6 classes that extend `React.Component` and must implement a `render` method. They have lifecycle methods (`componentDidMount`, etc.) and state management via `this.state` and `this.setState`.

### What are state and props? Difference between them.

- **Props** (short for properties): Read‑only data passed from parent to child. They are immutable within the child component.
- **State**: Mutable data managed within a component. When state changes, the component re‑renders.

| | Props | State |
|---|-------|-------|
| Mutability | Immutable (cannot be changed by child) | Mutable (changed via `setState` or hook setters) |
| Ownership | Owned by parent, used by child | Owned by the component itself |
| Purpose | Configure component, pass data down | Handle dynamic data that changes over time |

### What is a hook? Why were hooks introduced?

Hooks are functions that let you “hook into” React state and lifecycle features from functional components. They were introduced in React 16.8 to allow using state, side effects, and other React features without writing classes.

Reasons for hooks:
- Reuse stateful logic across components without complex patterns like HOCs or render props.
- Simplify component logic by grouping related code (e.g., `useEffect` for side effects).
- Avoid the complexity of `this` binding and class lifecycle methods.
- Improve tree‑shaking and reduce bundle size.

### If we have `var`, `let`, `const`, why do we need state variables?

Regular JavaScript variables do not trigger re‑renders when they change. State variables (`useState`) are designed to:
- Preserve values across renders.
- Trigger a re‑render when updated (via the setter function).
- Work within React’s reconciliation cycle. Without them, changes to variables would not be reflected in the UI.

### What is re‑rendering, and why does it happen?

Re‑rendering is the process where React updates the UI to reflect the current state and props. It happens when:
- A component’s state changes.
- Its props change.
- Its parent re‑renders (by default).
- A context value it uses changes.
- A custom hook triggers an update.

React batches updates for performance; re‑rendering does not necessarily mean the DOM is updated – React computes the difference (reconciliation) and only updates the DOM where needed.

### What is reconciliation in React? How does the diffing algorithm work?

Reconciliation is React’s algorithm for determining which parts of the DOM need to be updated when state or props change. It uses a **virtual DOM** (a lightweight representation) and compares it with the previous version.

**Diffing algorithm (simplified)**:
- **Elements of different types**: The whole subtree is torn down and rebuilt.
- **Elements of the same type**: React keeps the same DOM node and only updates changed attributes (e.g., `className`). Then it recursively diffs children.
- **List children with keys**: Keys help identify which items have changed, been added, or removed. Without stable keys, the algorithm may re‑render more than necessary.

### Why are keys important in lists? What happens if keys are unstable?

Keys give each element a stable identity, allowing React to match items between re‑renders. Without keys, React might reuse DOM nodes incorrectly, leading to performance issues or broken UI (e.g., lost focus, incorrect state). If keys are unstable (e.g., using index when the list can reorder), React may re‑create elements unnecessarily or mix up internal state.

### What is the difference between `Router` and `Link` in React Router?

- **`Router`** (e.g., `BrowserRouter`): Provides the routing context and handles history management. It is the parent component that enables navigation and URL sync.
- **`Link`**: A component that renders an anchor (`<a>`) with the `to` prop. It allows navigation without a full page reload, using client‑side routing.

### What is routing in React? How does it work?

Routing in React is the process of mapping URL paths to different components, enabling a single‑page application (SPA) to simulate multiple pages. React Router (or other libraries) listens to URL changes, matches the path against defined routes, and renders the corresponding component without a full browser refresh. It leverages the browser’s History API (`pushState`, `replaceState`) to manage navigation and updates the UI accordingly.

### Controlled vs uncontrolled components – explain with examples.

- **Controlled component**: Form input whose value is controlled by React state. The input’s value is set via `value` prop and updates via `onChange`. React is the single source of truth.
  ```jsx
  const [value, setValue] = useState('');
  <input value={value} onChange={e => setValue(e.target.value)} />
  ```
- **Uncontrolled component**: The DOM itself manages the input state. You access the current value via a ref (`useRef`).
  ```jsx
  const inputRef = useRef();
  <input ref={inputRef} />
  // later: inputRef.current.value
  ```

### What is prop drilling? Problems and solutions.

Prop drilling is passing data through multiple layers of components via props, even when intermediate components don’t need that data. This makes code harder to maintain and refactor.

**Solutions**:
- **Context API**: Create a context and provide values at a higher level, then consume them deep down.
- **State management libraries**: Redux, Zustand, etc.
- **Component composition**: Instead of passing props, pass components as children or use render props to flatten the hierarchy.

### How do you pass parent data to a deeply nested child (e.g., 5th child)?

Using **Context** is the most common approach. Create a context, wrap the parent tree with a `Provider`, and consume the context in the deeply nested child via `useContext` or `Context.Consumer`. Alternatively, use a state management library like Redux that provides global state.

### Difference between `useMemo` and `React.memo`.

- **`useMemo`**: A hook that memoizes the result of a computation. It recalculates only when its dependencies change. Used to optimize expensive calculations inside a component.
- **`React.memo`**: A higher‑order component that memoizes a component. It prevents re‑rendering if the props have not changed (shallow comparison). It wraps the whole component, not a value.

### Difference between `useMemo` and `useCallback`.

- **`useMemo`**: Returns a memoized **value**. It caches the result of a function call.
- **`useCallback`**: Returns a memoized **function** (the function reference is stable). It is essentially `useMemo(() => fn, deps)`.

Use `useCallback` when passing callbacks to child components that rely on reference equality to avoid unnecessary re‑renders.

### What happens if a component wrapped in `memo()` has its own state changes?

The component will still re‑render when its internal state changes, regardless of `memo`. `React.memo` only controls re‑renders triggered by parent prop changes. State updates always cause a re‑render of the component (unless you use other optimizations like `useState` with a functional update that doesn’t change the value).

### What happens if a child uses `memo()` and parent props don't change?

If the child is wrapped with `React.memo` and its props (by shallow comparison) have not changed, the child will **not** re‑render even if the parent re‑renders. This can prevent unnecessary renders.

### What is state batching? What changed in React 18 regarding batching?

State batching is the process of grouping multiple state updates into a single re‑render to improve performance. In React 17 and earlier, batching only happened inside React event handlers (e.g., `onClick`). Updates inside promises, `setTimeout`, or native events were not batched.

**React 18** introduced **automatic batching** for all updates, regardless of where they originate (promises, timeouts, etc.), using `createRoot`. This reduces unnecessary re‑renders.

### Explain `useEffect` deeply: cleanup function, dependency array pitfalls.

`useEffect` lets you perform side effects (data fetching, subscriptions, DOM manipulations) in functional components. It runs after the browser paints.

- **Dependency array**: If omitted, effect runs after every render. If empty (`[]`), runs only once (mount). If values are provided, effect runs when any of those values change.
- **Cleanup function**: Return a function from `useEffect` – it runs before the component unmounts and before the next effect execution (to clean up previous subscriptions). Useful for canceling requests, clearing timers, removing event listeners.

**Pitfalls**:
- Missing dependencies can lead to stale data or infinite loops.
- Including unnecessary dependencies may cause excessive re‑runs.
- Using objects or arrays as dependencies without memoization can cause unwanted re‑runs because reference changes every render.

### Difference between `useEffect`, `useLayoutEffect`, and `useInsertionEffect`.

- **`useEffect`**: Runs asynchronously after the browser paints. Suitable for most side effects.
- **`useLayoutEffect`**: Runs synchronously after all DOM mutations but before the browser paints. Useful for measuring layout or making visual updates that should appear before paint (e.g., scrolling to an element). Use sparingly as it blocks painting.
- **`useInsertionEffect`**: A newer hook (React 18) intended for CSS‑in‑JS libraries to inject styles before layout effects fire. Not meant for general use.

### What problems does `useMemo` actually solve? When should you NOT use it?

`useMemo` solves unnecessary recomputation of expensive calculations on every render. It also helps maintain referential equality for objects/arrays that are dependencies of other hooks (like `useEffect`).

**When NOT to use it**:
- For trivial calculations (e.g., `a + b`); the overhead of memoization may exceed the cost.
- Over‑using `useMemo` can make code less readable and lead to bugs if dependencies are mishandled.
- It does not guarantee that the value won’t be recomputed if React decides to re‑mount the component (e.g., during memory pressure).

### When would you use `React.memo`?

Use `React.memo` for:
- Components that receive the same props often but re‑render due to parent re‑renders.
- Large components that are expensive to re‑render.
- Pure functional components that depend on props only.

Avoid over‑using `memo` because the shallow prop comparison itself costs time. Use it where profiling shows a benefit.

### Build a custom hook like `useDebounce` or `useFetch`.

**`useDebounce`** (example):
```javascript
import { useState, useEffect } from 'react';

function useDebounce(value, delay) {
  const [debouncedValue, setDebouncedValue] = useState(value);
  useEffect(() => {
    const handler = setTimeout(() => setDebouncedValue(value), delay);
    return () => clearTimeout(handler);
  }, [value, delay]);
  return debouncedValue;
}
```

**`useFetch`** (example):
```javascript
function useFetch(url, options = {}) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);

  useEffect(() => {
    const abortController = new AbortController();
    const fetchData = async () => {
      try {
        const res = await fetch(url, { ...options, signal: abortController.signal });
        if (!res.ok) throw new Error('Network error');
        const json = await res.json();
        setData(json);
        setLoading(false);
      } catch (err) {
        if (err.name !== 'AbortError') {
          setError(err);
          setLoading(false);
        }
      }
    };
    fetchData();
    return () => abortController.abort();
  }, [url, ...Object.values(options)]); // caution: options can cause infinite loops
  return { data, loading, error };
}
```

---

## React Advanced & Internals

### How does React Fiber architecture change rendering?

React Fiber (introduced in React 16) is a complete rewrite of the reconciliation engine. It enables **incremental rendering**, splitting work into chunks and prioritizing updates (e.g., user input over data fetching). Fiber makes React capable of:
- Pausing, aborting, or reusing work.
- Assigning priorities to different types of updates.
- Supporting concurrent rendering and Suspense.

### What is concurrent rendering? When does it help vs hurt?

Concurrent rendering allows React to work on multiple tasks simultaneously, interrupting low‑priority work to handle high‑priority updates (like typing). It helps keep the UI responsive.

**When it helps**: During heavy computations, data fetching, or large list updates – the app stays interactive.
**When it may hurt**: Not all apps need it; it adds complexity and can cause subtle bugs if components assume synchronous rendering.

### Explain React Server Components vs Client Components.

- **Server Components**: Run on the server and send a special JSON-like format to the client. They never re‑render on the client and can access server resources (databases, file system) directly. They reduce bundle size and improve performance.
- **Client Components**: Run in the browser and can have interactivity, state, and effects. They are the traditional React components.

In the new React architecture, components are “use client” or “use server” directives. Server Components can import Client Components, but not vice versa.

### What is hydration? How do hydration mismatches occur?

Hydration is the process where React attaches event listeners and reconciles the server‑rendered HTML with the client‑side virtual DOM. It allows interactive components to “take over” the static markup.

**Hydration mismatches** occur when the HTML generated on the server differs from the initial render on the client (e.g., due to different data, random values, or browser‑only APIs). React will then attempt to patch the mismatch, which can cause performance issues and break user experience.

### How does React Context work? When can it hurt performance?

Context provides a way to pass data through the component tree without prop drilling. It works by creating a `Provider` component that holds a value. Any component that consumes the context via `useContext` will re‑render when the context value changes.

**Performance pitfalls**:
- If the context value changes frequently, many consumers may re‑render.
- When a component consumes context, it cannot be memoized based on props alone; it will re‑render whenever the context value changes, even if the component’s own props didn’t change.
- Using context for global state that changes often (e.g., animations) can cause excessive re‑renders.

### Scenario: Context API causes frequent re‑renders – why and how to fix?

**Why**: The context value is an object that gets re‑created on every render of the provider, causing all consumers to re‑render. Even if the actual data hasn’t changed, the reference changed.

**Fixes**:
- Memoize the context value with `useMemo` to keep the same object unless dependencies change.
- Split contexts into smaller, focused contexts so consumers only subscribe to what they need.
- Use state management libraries (like Redux) that allow selective subscriptions.
- Use `useContextSelector` or similar pattern if available.

### What is code splitting? How does `React.lazy` work internally?

Code splitting is the practice of breaking the bundle into smaller chunks that are loaded on demand, improving initial load time. `React.lazy` allows you to dynamically import a component as a separate chunk.

Internally, `React.lazy` takes a function that calls `import()` and returns a Promise. React suspends rendering until the promise resolves, showing a fallback (via `<Suspense>`). The lazy‑loaded component is then rendered.

### How does tree shaking work in modern bundlers?

Tree shaking is a dead‑code elimination technique that removes unused exports from the final bundle. Bundlers like Webpack and Rollup analyze the import/export graph and only include code that is actually used. This relies on ES modules being statically analyzable.

### What is the purpose of Suspense beyond lazy loading?

Suspense is a generic mechanism for orchestrating asynchronous dependencies in React. Besides lazy loading components, it can be used for data fetching (with libraries like Relay, Next.js) or any asynchronous operation that integrates with Suspense. It lets components “wait” for something before rendering, with a fallback UI.

### Explain the concept of "controlled re‑render boundaries".

A controlled re‑render boundary is a technique to isolate parts of the UI that re‑render frequently from those that don’t. This can be achieved by:
- Using `React.memo` on child components.
- Moving state down to the components that need it.
- Lifting state up only as necessary.
- Using `useMemo` and `useCallback` to stabilize props.
- Structuring context to avoid unnecessary consumers.

### How would you build a custom hook library?

A custom hook library is a collection of reusable hooks. Steps:
1. Design hooks with clear APIs, handling edge cases.
2. Write them as pure functions that follow the Rules of Hooks.
3. Document with examples and TypeScript types.
4. Publish to npm or a private registry.
5. Include tests (React Testing Library) and ensure they work across versions.

### What are the hidden reasons a component re‑renders even when props don't change?

- **Parent re‑render**: By default, when a parent re‑renders, all its children re‑render, regardless of prop changes. (Fixed with `React.memo`)
- **Inline functions/objects**: If you pass an inline function or object as prop, the child sees a new reference on every render, causing a re‑render (unless the child is memoized and uses deep comparison or the prop is memoized).
- **Context changes**: If the component consumes a context that changes, it re‑renders.
- **Hooks with changing dependencies**: `useEffect`, `useMemo`, `useCallback` dependencies may cause re‑execution of hooks, but not necessarily the whole component re‑render.
- **State updates that set the same value**: In React 18, if you set state to the same value (using `setState(prev => prev)`), it may still cause a re‑render in some cases (but not in strict mode?).

### How does React 18's automatic batching work?

Automatic batching in React 18 groups multiple state updates from any source (not just event handlers) into a single re‑render. This is enabled by default when using `createRoot`. It reduces unnecessary renders and improves performance. You can opt out using `flushSync`.

### How do you handle real-time updates efficiently in React?

- Use WebSockets or Server‑Sent Events (SSE) for pushing updates.
- Manage connections with custom hooks that handle lifecycle (connect on mount, disconnect on unmount).
- Use `useRef` to store the connection object.
- Throttle or debounce UI updates if they are frequent.
- Use `useReducer` or state management to batch updates.
- Leverage `React.memo` and careful component structure to avoid re‑rendering large parts of the UI.
- Use virtualization for large lists.

---

## Redux & State Management

### What is Redux and why is it used?

Redux is a predictable state container for JavaScript applications. It centralizes application state in a single store, enforces immutability, and provides a unidirectional data flow (action → reducer → new state). It’s used to manage complex state that is shared across many components, especially in large applications.

### What problems does Redux solve in large React applications?

- **State sharing**: Avoids prop drilling for deeply nested components.
- **Predictability**: State changes happen via pure reducers, making it easier to debug with time‑travel.
- **Separation of concerns**: UI logic is decoupled from state management.
- **Middleware**: Enables handling side effects (async actions, logging) in a structured way.
- **DevTools**: Excellent debugging capabilities.

### Explain the Redux data flow (action → reducer → store → view).

1. **Action**: A plain object with a `type` field describing what happened (e.g., `{ type: 'INCREMENT' }`). Dispatched from the UI.
2. **Reducer**: A pure function that takes the current state and an action, and returns a new state (immutable update). Reducers combine to form the root reducer.
3. **Store**: Holds the state tree. Provides `dispatch`, `getState`, and `subscribe`.
4. **View**: React components subscribe to the store and re‑render when the state changes.

### What is Redux Toolkit and why is it recommended over plain Redux?

Redux Toolkit (RTK) is the official, opinionated toolset for Redux. It simplifies common patterns, reduces boilerplate, and includes best practices out of the box:

- **`configureStore`**: Sets up the store with good defaults (middleware, devtools).
- **`createSlice`**: Automatically generates action creators and reducers.
- **`createAsyncThunk`**: Handles asynchronous actions with loading states.
- **Immer integration**: Allows writing mutable‑looking code in reducers (actual immutability is handled).
- **Redux DevTools** automatically enabled.

### Explain the flow of Redux Toolkit.

1. **Define slices** using `createSlice`. Each slice contains `name`, `initialState`, and `reducers` (functions that handle actions). Reducers can be simple or use `prepare` callbacks.
2. **Combine slices** (if needed) and configure the store with `configureStore`.
3. **Dispatch actions** using the generated action creators (e.g., `increment()`).
4. **Use hooks** (`useSelector`, `useDispatch`) in React components to read state and dispatch actions.
5. **Async logic**: Use `createAsyncThunk` to define thunks that handle async requests and dispatch pending/fulfilled/rejected actions.

### How does Redux Toolkit work internally?

- `createSlice` uses `createReducer` and `createAction` under the hood to generate reducers and action creators. It leverages Immer to allow immutable updates with mutable syntax.
- `configureStore` calls Redux’s `createStore`, applies default middleware (including `redux-thunk`), and enables the Redux DevTools Extension.
- `createAsyncThunk` returns a thunk that dispatches the lifecycle actions automatically and allows handling of the async operation.

### What is `createSlice()` and what does it contain? (name, initialState, reducers)

`createSlice` accepts an object with:
- `name`: A string used as prefix for action types.
- `initialState`: The initial state value.
- `reducers`: An object mapping action names to reducer functions (or `prepare` callbacks). Each reducer function receives `state` and `action` and can mutate the state (thanks to Immer).
- `extraReducers` (optional): Allows responding to actions not defined in the slice (e.g., from `createAsyncThunk`).

It returns an object with `actions` (action creators) and `reducer` (slice reducer).

### Explain reducers and extraReducers – when to use each?

- **`reducers`**: Used for actions that are directly handled by this slice. RTK automatically generates action creators with the same names. Good for synchronous, slice‑specific updates.
- **`extraReducers`**: Used to respond to actions defined elsewhere (e.g., thunks, actions from other slices). It’s often used with `builder` callback to handle `pending`, `fulfilled`, `rejected` of async thunks. It allows a slice to react to actions that are not its own.

### What is `createAsyncThunk()` and why is it used?

`createAsyncThunk` is a function that creates a thunk action that handles asynchronous requests. It takes an action type prefix and a payload creator (async function). It automatically dispatches `pending`, `fulfilled`, and `rejected` actions based on the promise. This reduces boilerplate for loading states and error handling.

### How does async flow work in Redux Toolkit?

1. Define a thunk using `createAsyncThunk`.
2. Inside the payload creator, perform async work (e.g., fetch).
3. Dispatch the thunk from a component.
4. The thunk dispatches the `pending` action immediately.
5. When the async work completes, it dispatches `fulfilled` with the result, or `rejected` with an error.
6. In slices, use `extraReducers` to listen to these actions and update state (e.g., set loading false, store data).

### Where and why have you used Redux Toolkit in your projects?

Common scenarios:
- **Large‑scale apps with complex shared state**: Shopping carts, user authentication, multi‑step forms.
- **Real‑time dashboards**: To manage data from WebSockets across many components.
- **Apps with complex async flows**: To maintain loading/error states in a consistent manner.
- **When multiple features need access to the same data**: E.g., user profile, preferences, notifications.

### Redux vs Context API vs Zustand – how do you decide in a large-scale application?

| | Redux | Context API | Zustand |
|---|-------|-------------|---------|
| **Use case** | Large apps, complex state, frequent updates | Simple state, medium nesting, low update frequency | Small‑medium apps, simple API, minimal boilerplate |
| **Performance** | Optimized with selectors, middleware | Can cause re‑renders; requires careful splitting | Very performant, minimal re‑renders |
| **Boilerplate** | Higher (but RTK reduces it) | Low | Very low |
| **Tooling** | Excellent (DevTools) | Basic | Good |
| **Learning curve** | Steeper | Easy | Easy |

**Decision**: For large‑scale apps with many features, complex async logic, and need for time‑travel debugging, Redux (with RTK) is a solid choice. If you need a lighter alternative with good performance and less boilerplate, Zustand is popular. Context is best for static or low‑frequency updates (e.g., theme, localization) and not recommended for high‑frequency state.

### Compare Redux, MobX, and Recoil for enterprise-scale state management (pros and cons).

| | Redux | MobX | Recoil |
|---|-------|------|--------|
| **Paradigm** | Functional, immutable | Observable, mutable | Atomic, graph‑based |
| **Boilerplate** | High (reducers, actions) | Low (decorators, observables) | Moderate (atoms, selectors) |
| **Learning curve** | Steep | Moderate | Moderate |
| **Performance** | Good with selectors | Excellent (fine‑grained) | Good with derived state |
| **Tooling** | Excellent DevTools | Good | Good (early) |
| **Scalability** | Proven in huge apps | Good, but mutable may cause unpredictability | Newer, but promising |

- **Redux** is battle‑tested, great for large teams due to strict patterns, but requires discipline.
- **MobX** allows more flexibility and less code, but mutable updates can be error‑prone in large teams.
- **Recoil** offers a more React‑centric approach with derived state and concurrent rendering support, but is newer.

### How would you design a state management solution for a complex analytics/dashboard app?

For a dashboard app with:
- Real‑time data (WebSockets)
- Multiple widgets that can be individually refreshed
- Filters that affect many widgets
- Large datasets (need virtualization)

Approach:
1. Use Redux Toolkit for global state (filters, user settings, notifications).
2. Use `createEntityAdapter` for normalized data (e.g., metrics, widgets).
3. Use `createAsyncThunk` for API calls with cancellation support (AbortController).
4. For real‑time updates, use a custom middleware to listen to WebSocket messages and dispatch actions.
5. Use `useSelector` with memoized selectors (Reselect) to avoid re‑renders.
6. For widget‑specific state (e.g., expanded/collapsed), keep it locally in the widget component to avoid global re‑renders.
7. Leverage React.memo for widget components that receive stable props.
8. Use Suspense and lazy loading for heavy dashboard sections.

This combines the predictability of Redux with localized state for performance.
