 # 🧠 Data Structures Labs (TND004)

A collection of labs from the course **TND004 – Data Structures**, exploring the implementation and analysis of common data structures such as linked lists, trees, heaps, priority queues, and graphs. Each lab focuses on applying algorithmic thinking to real-world simulation or problem-solving tasks.

## 📁 Repository Structure

```
.
├── Lab1/              # Linked lists and iterators
├── Lab2/              # Trees and recursive algorithms
├── Lab3/              # Priority queues and pattern detection
├── Lab4/              # Graph traversal and pathfinding (if applicable)
└── README.md          # This file
```

---

## ⚙️ Dependencies & Build Setup

### 🔧 General

* **CMake ≥ 3.20** – Used to configure and build the labs
* **C++20** support – Required for modern language features

### 🛠 macOS Setup

If you're on macOS, Apple Clang may not fully support `std::format`, so:

1. **Install the `fmt` library**:

   ```bash
   brew install fmt
   ```

2. **Build with linking to `fmt`**:

   ```bash
   clang++ -std=c++20 -lfmt -I/opt/homebrew/include -L/opt/homebrew/lib ...
   ```

> ✅ Note: The labs use `fmt::format` on macOS instead of `std::format`.
> 🔁 Additionally, you may need to manually update linker settings or replace occurrences of std::format with fmt::format in your code files.

---

### 🪠 Windows Setup

If you're using **Visual Studio 2022+**, no extra libraries are needed:

* `std::format` is supported natively
* Just use the default CMake preset or open the generated project directly

---

### 📦 Vcpkg (Optional Labs)

Some labs (like collision simulations) use external libraries managed by [vcpkg](https://github.com/microsoft/vcpkg):

```bash
git clone https://github.com/microsoft/vcpkg.git
cd vcpkg
./bootstrap-vcpkg.sh    # Linux/macOS
.\bootstrap-vcpkg.bat   # Windows
```

To install libraries (e.g., `glfw3`, `glm`, `fmt`, `glad`, etc.):

```bash
./vcpkg install fmt glfw3 glm glad
```

---

## 🔨 How to Build

From inside a lab directory (e.g., `Lab3/`):

```bash
mkdir build
cd build
cmake ..
make
```

Or, for Windows with Visual Studio:

```bash
cmake .. -G "Visual Studio 17 2022"
```

---

## ✅ Lab Status Overview

| Lab | Topic                              | Status        |
| --- | ---------------------------------- | ------------- |
| 1   | Linked Lists                       | ✅ Complete    |
| 2   | Trees / Recursion                  | ✅ Complete    |
| 3   | Priority Queue / Pattern Detection | ✅ Complete    |
| 4   | Graph Structures                   | ⏳ In Progress |

---

## 📚 Key Concepts Covered

* Custom data structures (linked list, set, binary heap)
* STL vs. manual memory management
* Priority queue implementations: sorted vector vs. binary heap
* Sorting-based geometric algorithms (e.g. collinearity detection)
* Time and space complexity analysis
* Cross-platform builds and dependency management

---

## 💬 Suggested Repository Description (for GitHub)

> Implementations of data structures and algorithms from the TND004 Data Structures course (LiU). Includes linked lists, trees, heaps, and pattern detection using priority queues. Built using C++20 and CMake with cross-platform support (macOS/Windows).

---

## 📌 Optional Additions

* 📈 **Performance Results** for comparisons (e.g., heap vs. vector queue)
* 🧪 **Unit Tests**
* 📚 **References** to textbooks or lecture notes
* 🧠 **Complexity Analysis** (for each lab)
