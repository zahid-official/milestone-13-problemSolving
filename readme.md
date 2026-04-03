<div align="center">

# TypeScript Problem Solving

A hands-on TypeScript project demonstrating core language features through practical problem-solving - covering generics, type guards, union & intersection types, enums, OOP inheritance, async patterns and more.

[![GitHub Repo](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/zahid-official/milestone-13)
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
<img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
<img src="https://img.shields.io/badge/ts--node--dev-3178C6?style=for-the-badge&logo=ts-node&logoColor=white" alt="ts-node-dev" />

</div>

<br/>

## 🔍 Overview

This project is a focused TypeScript exercise project that tackles real-world coding problems using TypeScript's powerful type system. Each function demonstrates a specific language concept - from generics and type narrowing to class inheritance and async/await - making it an ideal reference for building type-safe, maintainable code.

> _Mastering TypeScript, one problem at a time._

<br/>

## ✨ Problem Solving

<table align="center">
<thead>
<tr><th align="center">No.</th><th align="left">Problem</th><th align="left">Function / Class</th><th align="left">Concept</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td align="center">1</td><td><b>Format String</b></td><td><code>formatString()</code></td><td>Optional Parameters</td><td>Converts a string to uppercase by default, or lowercase when the optional <code>toUpper</code> flag is explicitly set to <code>false</code></td></tr>
<tr><td align="center">2</td><td><b>Filter by Rating</b></td><td><code>filterByRating()</code></td><td>Typed Object Arrays</td><td>Accepts an array of objects with <code>title</code> and <code>rating</code> properties, returns only items with a rating greater than 4</td></tr>
<tr><td align="center">3</td><td><b>Concatenate Arrays</b></td><td><code>concatenateArrays&lt;T&gt;()</code></td><td>Generics</td><td>Merges multiple arrays of any type into a single array using a generic type parameter <code>&lt;T&gt;</code> and rest parameters</td></tr>
<tr><td align="center">4</td><td><b>Vehicle & Car</b></td><td><code>Vehicle</code> → <code>Car</code></td><td>OOP & Inheritance</td><td>Base <code>Vehicle</code> class with private members; <code>Car</code> extends it with an additional <code>model</code> property and <code>getModel()</code> method</td></tr>
<tr><td align="center">5</td><td><b>Process Value</b></td><td><code>processValue()</code></td><td>Union Types & Type Guards</td><td>Accepts <code>string | number</code>, returns the string length for strings or doubles the value for numbers using <code>typeof</code> narrowing</td></tr>
<tr><td align="center">6</td><td><b>Most Expensive Product</b></td><td><code>getMostExpensiveProduct()</code></td><td>Interfaces & Reduce</td><td>Defines a <code>Product</code> interface and finds the highest-priced product using <code>.reduce()</code>, returns <code>null</code> for empty arrays</td></tr>
<tr><td align="center">7</td><td><b>Day Type Checker</b></td><td><code>getDayType()</code></td><td>Enums</td><td>Uses a <code>Day</code> enum with all weekdays; returns <code>"Weekend"</code> for Saturday/Sunday and <code>"Weekday"</code> for the rest</td></tr>
<tr><td align="center">8</td><td><b>Async Square</b></td><td><code>squareAsync()</code></td><td>Async/Await & Promises</td><td>Returns a <code>Promise&lt;number&gt;</code> that resolves with the squared value after 1 second, or rejects for negative inputs</td></tr>
</tbody>
</table>

<br/>

## 🛠️ Tech Stack

<table align="center">
<thead>
<tr><th align="left">Technology</th><th align="center">Version</th><th align="left">Purpose</th></tr>
</thead>
<tbody>
<tr><td><b>TypeScript</b></td><td align="center"><code>ES2024</code></td><td>Statically typed language for JavaScript</td></tr>
<tr><td><b>Node.js</b></td><td align="center"><code>v18+</code></td><td>JavaScript runtime environment</td></tr>
<tr><td><b>ts-node-dev</b></td><td align="center">-</td><td>TypeScript execution with auto-restart on changes</td></tr>
</tbody>
</table>

<br/>

## 🏗️ Architecture

<div align="center">
<pre>
┌──────────────────────────────────────────────────────────┐
│                    TypeScript Compiler                   │
│                   (tsconfig.json - ES2024)               │
├──────────────────────────────────────────────────────────┤
│                                                          │
│  src/index.ts                                            │
│  ┌────────────────────────────────────────────────────┐  │
│  │            Utility Functions                       │  │
│  │                                                    │  │
│  │  ┌──────────────┐  ┌───────────────────────────┐   │  │
│  │  │  formatString │  │  filterByRating          │   │  │
│  │  │  (Overloads)  │  │  (Array + Object Types)  │   │  │
│  │  └──────────────┘  └───────────────────────────┘   │  │
│  │                                                    │  │
│  │  ┌──────────────┐  ┌───────────────────────────┐   │  │
│  │  │ concatenate  │  │  processValue             │   │  │
│  │  │ Arrays&lt;T&gt;    │  │  (Union + Type Guards)    │   │  │
│  │  └──────────────┘  └───────────────────────────┘   │  │
│  │                                                    │  │
│  │  ┌──────────────────────────────────────────────┐  │  │
│  │  │  getMostExpensiveProduct (Interface + Reduce)│  │  │
│  │  └──────────────────────────────────────────────┘  │  │
│  ├────────────────────────────────────────────────────┤  │
│  │            OOP Hierarchy                           │  │
│  │  ┌──────────────┐                                  │  │
│  │  │   Vehicle    │◄── Base class (make, year)       │  │
│  │  │   └── Car    │◄── Derived class (+ model)       │  │
│  │  └──────────────┘                                  │  │
│  ├────────────────────────────────────────────────────┤  │
│  │            Enums &amp; Async                           │  │
│  │  ┌──────────────┐  ┌───────────────────────────┐   │  │
│  │  │   Day Enum   │  │  squareAsync              │   │  │
│  │  │  (getDayType)│  │  (Promise + setTimeout)   │   │  │
│  │  └──────────────┘  └───────────────────────────┘   │  │
│  └────────────────────────────────────────────────────┘  │
│                            │                             │
│                            ▼                             │
│                   dist/ (Compiled JS)                    │
└──────────────────────────────────────────────────────────┘
</pre>
</div>

## 📂 Project Structure

```
milestone-13/
│
├── package.json                   # Dependencies and scripts
├── tsconfig.json                  # TypeScript compiler configuration
│
├── src/
│   └── index.ts                   # All TypeScript problem solutions
│
└── dist/                          # Compiled JavaScript output
```

<br/>

## 🚀 Getting Started

### Prerequisites

<table align="center">
<thead>
<tr><th align="left">Requirement</th><th align="left">Details</th></tr>
</thead>
<tbody>
<tr><td><b>Node.js</b></td><td>v18 or higher recommended</td></tr>
<tr><td><b>npm</b></td><td>Comes bundled with Node.js</td></tr>
<tr><td><b>TypeScript</b></td><td>Installed as a dev dependency</td></tr>
</tbody>
</table>

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/zahid-official/milestone-13.git

# 2. Navigate to the project directory
cd milestone-13

# 3. Install dependencies
npm install

# 4. Start the development server
npm run dev
```

The application will compile and run via `ts-node-dev` with auto-restart enabled.

<br/>

## 📜 Available Scripts

<table align="center">
<thead>
<tr><th align="left">Command</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><code>npm run dev</code></td><td>Run TypeScript with <code>ts-node-dev</code> - auto-restarts on file changes</td></tr>
<tr><td><code>npm test</code></td><td>Run the test suite (placeholder)</td></tr>
</tbody>
</table>

<br/>

## ⚙️ How It Works

<div>
<pre>
                      Source File (index.ts) ──► ts-node-dev watches for changes
                                                          │
                                          ┌───────────────┘
                                          ▼
                                TypeScript Compiler
                                (strict mode, ES2024)
                                          │
                              ┌──────────┴──────────┐
                              ▼                     ▼
                        Type Checking          Transpilation
                        (Catches errors        (Generates JS
                          at compile time)       in /dist)
                              │                     │
                              ▼                     ▼
                        Error Feedback ◄──    Node.js Runtime
                        (Developer fix)       (Executes output)
</pre>
</div>

1. **Write** - TypeScript functions are authored in `src/index.ts` with full type annotations.
2. **Compile** - `ts-node-dev` transpiles TypeScript on-the-fly with `--transpile-only` for speed.
3. **Execute** - The compiled JavaScript runs in the Node.js runtime environment.
4. **Watch** - File changes trigger automatic re-compilation and re-execution via `--respawn`.
5. **Validate** - TypeScript's strict mode catches type errors before runtime, ensuring code correctness.

<br/>

## 🌟 Author

<div align="center">
  <a href="https://github.com/zahid-official">
    <img src="https://github.com/zahid-official.png" width="100" height="100" style="border-radius: 50%;" alt="Zahid Official" />
  </a>

  <h3>Zahid Official</h3>
  <p><b>Web Developer | Tech Enthusiast</b></p>

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/zahid-official)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/zahid-web)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:zahid.official8@gmail.com)

  <p>Building type-safe solutions through clean code and continuous learning</p>
</div>

<br/>

## 🤝 Contributing

Contributions are welcome and appreciated! Here's how you can help improve this project:

```bash
# 1. Fork the repository

# 2. Create a feature branch
git checkout -b feature/your-feature-name

# 3. Make your changes and commit
git commit -m "feat: add your feature description"

# 4. Push to your fork
git push origin feature/your-feature-name

# 5. Open a Pull Request against the main branch
```

<p align="center"><i>Mastering TypeScript, one problem at a time.</i></p>
