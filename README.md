# 🧩 C++ Regex to NFA Engine

A lightweight, from-scratch implementation of a **Regular Expression Engine** built with **C++** and **Standard Template Library (STL)**.
This project demonstrates core computer science concepts by converting infix regex patterns into postfix notation, generating a Non-Deterministic Finite Automaton (NFA), and validating input strings via graph traversal.

## 🚀 Features

-   **⚙️ Shunting Yard Algorithm:** Robust parsing logic to convert infix regex to postfix (Reverse Polish Notation).
-   **🕸️ Thompson's Construction:** Converts postfix patterns into a dynamic NFA graph structure.
-   **🔍 DFS Pattern Matching:** A recursive backtracking engine to traverse the NFA and validate strings.
-   **🔗 Explicit Concatenation:** Uses the special `?` operator to explicitly link characters (e.g., `a?b`).
-   **⚡ Zero Dependencies:** Built entirely using standard C++ libraries (`<stack>`, `<queue>`, `<map>`, etc.).
-   **🛠️ Custom Operators:** Supports Union (`|`), Kleene Star (`*`), and Grouping `()`.

## 🛠️ Tech Stack

-   **Language:** C++ (C++11 or higher)
-   **Core Logic:** Automata Theory, Graph Theory
-   **Data Structures:** STL (Stack, Queue, Map, Set, Vector)

## 📦 Installation & Setup

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/esalama01/mini-regex-engine.git](https://github.com/esalama01/mini-regex-engine.git)
    cd mini-regex-engine
    ```

2.  **Compile the Code**
    Use `g++` or any standard C++ compiler to build the executable:
    ```bash
    g++ main.cpp -o regex_engine
    ```

3.  **Run the Application**
    Execute the binary to start the interactive matcher:
    ```bash
    ./regex_engine
    ```

4.  **Usage Syntax (Important)**
    This engine requires **explicit concatenation** using the `?` symbol.
    * *Standard Regex:* `ab`
    * *This Engine:* `a?b`
    * *Example Input:* `(a|b)*?c` matches `abac`

## 📂 Project Structure

```text
📁 mini-regex-engine/
│
├── 📜 main.cpp            # Monolithic source file containing all logic
│    ├── Shunting Yard     # Infix to Postfix conversion functions
│    ├── NFA Class         # State management & Transition logic
│    └── Matcher Class     # DFS Traversal Engine
│
└── 📜 README.md           # Project Documentation
