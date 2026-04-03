<div align="center">

<img src="https://img.shields.io/badge/TS-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript Logo" height="50" />

#  TypeScript Problem Solving

A hands-on TypeScript project demonstrating core language features through practical problem-solving — covering generics, type guards, union & intersection types, enums, OOP inheritance, async patterns, and more.

[![GitHub Repo](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/zahid-official/milestone-13)
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
<img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
<img src="https://img.shields.io/badge/ts--node--dev-3178C6?style=for-the-badge&logo=ts-node&logoColor=white" alt="ts-node-dev" />

</div>

<br/>

## 🔍 Overview

**Milestone 13** is a focused TypeScript exercise project that tackles real-world coding problems using TypeScript's powerful type system. Each function demonstrates a specific language concept — from generics and type narrowing to class inheritance and async/await — making it an ideal reference for building type-safe, maintainable code.

> _Mastering TypeScript, one problem at a time._

<br/>

## ✨ Key Features

### 🔤 Type System Mastery

<table align="center">
<thead>
<tr><th align="left">Feature</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><b>Union Types</b></td><td>Process values of multiple types using <code>string | number</code> unions with type narrowing</td></tr>
<tr><td><b>Intersection Types</b></td><td>Combine multiple type definitions into composite types using the <code>&</code> operator</td></tr>
<tr><td><b>Generics</b></td><td>Build reusable, type-safe functions like <code>concatenateArrays&lt;T&gt;</code> that work across any type</td></tr>
<tr><td><b>Enums</b></td><td>Define named constant sets with <code>Day</code> enum for structured, readable conditional logic</td></tr>
</tbody>
</table>

### 🏗️ Object-Oriented Patterns

<table align="center">
<thead>
<tr><th align="left">Feature</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><b>Class Inheritance</b></td><td><code>Car</code> extends <code>Vehicle</code> with private members, constructors, and method overriding</td></tr>
<tr><td><b>Interfaces</b></td><td>Define contracts like <code>Product</code> to enforce consistent object shapes across functions</td></tr>
<tr><td><b>Access Modifiers</b></td><td>Use <code>private</code> constructor parameters for clean encapsulation and data hiding</td></tr>
</tbody>
</table>

### ⚡ Async & Functional Patterns

<table align="center">
<thead>
<tr><th align="left">Feature</th><th align="left">Description</th></tr>
</thead>
<tbody>
<tr><td><b>Async/Await</b></td><td>Asynchronous square computation with <code>Promise&lt;number&gt;</code> return type and error rejection</td></tr>
<tr><td><b>Array Filtering</b></td><td>Higher-order function <code>filterByRating</code> using typed object arrays and <code>.filter()</code></td></tr>
<tr><td><b>Reduce Operations</b></td><td>Find the most expensive product from a typed array using <code>.reduce()</code> with null safety</td></tr>
<tr><td><b>Type Guards</b></td><td>Runtime type checking with <code>typeof</code> for safe value processing in union types</td></tr>
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
<tr><td><b>ts-node-dev</b></td><td align="center">—</td><td>TypeScript execution with auto-restart on changes</td></tr>
</tbody>
</table>

<br/>

## 🏗️ Architecture

<div align="center">
<pre>
┌──────────────────────────────────────────────────────────┐
│                    TypeScript Compiler                    │
│                   (tsconfig.json — ES2024)                │
├──────────────────────────────────────────────────────────┤
│                                                          │
│  src/index.ts                                            │
│  ┌────────────────────────────────────────────────────┐  │
│  │            Utility Functions                       │  │
│  │                                                    │  │
│  │  ┌──────────────┐  ┌───────────────────────────┐   │  │
│  │  │  formatString │  │  filterByRating           │   │  │
│  │  │  (Overloads)  │  │  (Array + Object Types)   │   │  │
│  │  └──────────────┘  └───────────────────────────┘   │  │
│  │                                                    │  │
│  │  ┌──────────────┐  ┌───────────────────────────┐   │  │
│  │  │ concatenate  │  │  processValue             │   │  │
│  │  │ Arrays&lt;T&gt;    │  │  (Union + Type Guards)    │   │  │
│  │  └──────────────┘  └───────────────────────────┘   │  │
│  │                                                    │  │
│  │  ┌──────────────────────────────────────────────┐  │  │
│  │  │  getMostExpensiveProduct (Interface + Reduce) │  │  │
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
│                          │                               │
│                          ▼                               │
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
<tr><td><code>npm run dev</code></td><td>Run TypeScript with <code>ts-node-dev</code> — auto-restarts on file changes</td></tr>
<tr><td><code>npm test</code></td><td>Run the test suite (placeholder)</td></tr>
</tbody>
</table>

<br/>

## ⚙️ How It Works

<div align="center">
<pre>
Source File (index.ts) ──► ts-node-dev watches for changes
                                    │
                    ┌────────────────┘
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

1. **Write** — TypeScript functions are authored in `src/index.ts` with full type annotations.
2. **Compile** — `ts-node-dev` transpiles TypeScript on-the-fly with `--transpile-only` for speed.
3. **Execute** — The compiled JavaScript runs in the Node.js runtime environment.
4. **Watch** — File changes trigger automatic re-compilation and re-execution via `--respawn`.
5. **Validate** — TypeScript's strict mode catches type errors before runtime, ensuring code correctness.

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

  <p>Creating impactful digital experiences with passion and purposeful design</p>
</div>

<br/>

## 🤝 Contributing

Contributions are welcome and appreciated! Here's how you can help improve **Milestone 13**:

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

<p align="center"><b>Milestone 13</b> — <i>Mastering TypeScript, one problem at a time.</i></p>