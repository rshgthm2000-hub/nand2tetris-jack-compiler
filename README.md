# Nand2Tetris Jack Compiler

## 📌 Overview

This project is a **complete two-pass compiler** for the **Nand2Tetris** course, implemented entirely in **Python**. It translates high-level, object-oriented **Jack source code (`.jack`)** into **Virtual Machine (VM) bytecode (`.vm`)`)**, acting as the vital link between high-level programming and the underlying stack machine architecture.

The compiler features a robust modular design, incorporating a custom **lexical analyzer**, **recursive descent parser**, **scoped symbol table**, and a specialized **VM instruction writer**. It processes either a single `.jack` source file or an entire directory of files to generate the corresponding runnable VM targets.

---

## 🚀 Features

* **Full Syntax Analysis:** Efficiently tokenizes and parses the complex, context-free grammar of the Jack language.
* **Modular Software Pipeline:** Clean separation of concerns between structural parsing, semantic analysis, and backend translation.
* **Dual-Scope Symbol Table:** Separates class-level fields/statics from subroutine-level arguments/local variables to track memory indexing cleanly.
* **Object-Oriented Compilation:** Smoothly compiles complex class constructors, object instantiations, dynamic method tracking (`this`), and functional subroutines.
* **Program Flow Control:** Handles standard control loops (`while`, `if-else`) and seamlessly manages execution transitions.
* **Built-in Error Reporting:** Gracefully catches syntax irregularities and formatting bugs mid-parse.

---

## 🛠️ Technologies Used

* **Language:** Python 3
* **Concepts:** Compiler Construction, Lexical Analysis, Recursive Descent Parsing, Code Generation, Object-Oriented Memory Layout

---

## 📂 Project Structure

```
nand2tetris-jack-compiler/
├── Jack_Compiler.py        // Main driver script that coordinates compilation
├── token_reader.py         // Tokenizer that strips comments and isolates lexical atoms
├── compilation_engine.py   // Parser that enforces grammar and drives code generation
├── symbol_table.py         // Tracks scope, types, and running indexes for variables
├── vm_writer.py            // Low-level abstraction interface for writing output bytecode
├── error_reporter.py       // System for identifying and displaying parsing errors
└── README.md
```

---

## ▶️ How to Run

### Setup
No external libraries or heavy dependencies are required. All you need is a standard Python 3 interpreter environment.

### Execute

Compile a single Jack source file:
```bash
python Jack_Compiler.py Main.jack
```

Compile a directory containing multiple Jack files:
```bash
python Jack_Compiler.py SquareGame/
```

---

## 📘 Learning Outcomes

* Mastery over building a clean two-pass compilation pipeline from scratch.
* In-depth practical exposure to recursive descent parsing techniques.
* Thorough understanding of how object allocation, pointer management, and data encapsulation operate beneath high-level programming syntax.
* Deepened structural design and file organization skills using Python.

---

## 📖 References

* Nand2Tetris Course Official Site
* The Elements of Computing Systems by Noam Nisan and Shimon Schocken

---

## 🧑‍💻 Author

**RISHI GOUTHAM** Python | Software Architecture | Computer Science Student

---

## 📄 License

This project is created for educational purposes as part of the Nand2Tetris computer system engineering course.
```
