# Practice C Programs in Depth 🚀

[![C Language](https://img.shields.io/badge/Language-C-00599C?logo=c&logoColor=white)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Standard](https://img.shields.io/badge/Standard-C99%20%2F%20C11-blue.svg)](https://en.cppreference.com/w/c)
[![Category](https://img.shields.io/badge/Focus-Systems%20%26%20DSA-green.svg)](#key-topics-covered)
[![Status](https://img.shields.io/badge/Status-Active%20Practice-orange.svg)](#)

A comprehensive, hands-on repository dedicated to mastering the **C programming language from ground up to advanced system-level concepts**. This collection spans deep pointer mechanics, memory layout & dynamic allocation, custom data structures, bit-level manipulations, file I/O, callbacks, and algorithmic problem-solving with detailed inline explanations.

---

## 📖 Table of Contents

- [About This Repository](#-about-this-repository)
- [Key Topics Covered](#-key-topics-covered)
  - [1. Pointers & Memory Management](#1-pointers--memory-management)
  - [2. Data Structures & Algorithms](#2-data-structures--algorithms)
  - [3. Function Pointers & Callbacks](#3-function-pointers--callbacks)
  - [4. Structures, Unions & Bitfields](#4-structures-unions--bitfields)
  - [5. Storage Classes & Multi-File Linking](#5-storage-classes--multi-file-linking)
  - [6. File Handling & Error Management](#6-file-handling--error-management)
  - [7. Strings & Character Operations](#7-strings--character-operations)
  - [8. Command Line Arguments](#8-command-line-arguments)
  - [9. Algorithmic Practice & Problem Solving](#9-algorithmic-practice--problem-solving)
- [Repository Directory Structure](#-repository-directory-structure)
- [Compilation & Execution Guide](#-compilation--execution-guide)
  - [Prerequisites](#prerequisites)
  - [Single-File Compilation](#single-file-compilation)
  - [Multi-File Compilation (Storage Classes)](#multi-file-compilation-storage-classes)
  - [Programs with Command-Line Arguments](#programs-with-command-line-arguments)
- [Recommended GitHub Repository Settings](#-recommended-github-repository-settings)
- [Author & Acknowledgments](#-author--acknowledgments)

---

## 📌 About This Repository

Understanding C requires peeling back layers of abstraction: visualizing memory addresses, managing heap lifecycles manually, structuring bits, and building data structures from scratch. 

This repository serves as:
- **A Reference Manual:** Quick reference for C syntax, pointer arithmetic, macros, and standard library behaviors.
- **Deep-Dive Explorations:** Code experiments analyzing memory padding, `offsetof`, dynamic resizing with `realloc`, and function pointer callbacks.
- **Problem-Solving Bank:** Implementations of classic mathematical, matrix, string manipulation, and sorting challenges.

---

## 🧠 Key Topics Covered

### 1. Pointers & Memory Management
- **Dynamic Memory Allocation (`malloc`, `calloc`, `realloc`, `free`):**
  - Understanding heap vs. stack allocation.
  - Zero-initialization with `calloc` vs uninitialized buffers in `malloc`.
  - In-place vs relocated memory expansion with `realloc`.
  - Proper memory deallocation and avoiding dangling pointers.
- **Pointer Arithmetic & Arrays:**
  - 1D and 2D pointer arrays, arrays of pointers, and pointer-to-pointer dereferencing.
  - Constant qualification: pointers to constants (`const int *`) vs constant pointers (`int * const`).
  - Swapping values in-place and via pointers.

### 2. Data Structures & Algorithms
- **Singly Linked List:**
  - Dynamic node creation with `malloc`.
  - Head insertion, tail insertion, traversal, and node deletion.
- **Stack:**
  - LIFO stack operations (`push`, `pop`) implemented on top of linked lists.
- **Search & Sort Algorithms:**
  - Linear Search & Binary Search implementations.
  - Selection sort variations (ascending order, descending order, even-index sorting).

### 3. Function Pointers & Callbacks
- Function pointer declaration and invocation syntax.
- Higher-order functions: passing function pointers as arguments to create callback mechanisms.
- Executing functional transformations across arrays using callbacks.

### 4. Structures, Unions & Bitfields
- **Structures:**
  - Nested structures, arrays within structures, and array of structure objects.
  - Passing structures by value vs. by reference (pointer to structure).
  - Structure padding, boundary alignment, and `sizeof` determinations.
- **Unions & Offset:**
  - Memory sharing among union members.
  - Calculating field byte offsets using the `offsetof()` macro from `<stddef.h>`.
- **Bitfields:**
  - Fine-grained bit-level allocation (`unsigned int flag : 1;`).
  - Memory footprint reduction and bit packing.

### 5. Storage Classes & Multi-File Linking
- Scope, visibility, and lifetime using `extern`, `register`, and `static`.
- Splitting code across translation units: accessing global variables and functions defined across multiple `.c` files.

### 6. File Handling & Error Management
- **File I/O Streams:**
  - Opening, reading, writing, and closing files (`fopen`, `fgets`, `fputs`, `fclose`).
  - Random access in files using `fseek` and position queries with `ftell`.
  - Writing and reading arrays and structured data from text files.
- **Error Handling:**
  - Standard error numbers (`errno`), decoding I/O errors and handling permission issues.

### 7. Strings & Character Operations
- Custom string manipulation built from scratch without standard `<string.h>` functions (`strlen`, `strcmp`).
- String comparison via pointer traversal.
- Tokenization using `strtok` and string normalization.

### 8. Command Line Arguments
- Interacting with `int argc` and `char *argv[]`.
- Converting string inputs to integers using `atoi()` for configurable CLI utilities.

### 9. Algorithmic Practice & Problem Solving
- Numerical problems: Armstrong numbers, Palindrome detection, Prime checking, Fibonacci sequences, digit frequency counter, sum of digits.
- 2D Matrices: $3\times3$ and $m\times n$ matrix multiplication, matrix transpose, and row/column traversals.
- Patterns: Number pyramids and triangle pattern generations.
- Real-world mini simulations: Basic ATM transaction state machine.

---

## 📂 Repository Directory Structure

```plaintext
Practice-C-programs-in-depth/
├── BITFIELD CONCEPT/
│   ├── bitfield_ex.c                 # Basic 1-bit & multi-bit structure fields
│   └── bitfield_ex2.c                # Bitfield memory layout demonstration
├── Callback quetions with conepts/
│   ├── callback_with_pointerfn.c     # Function pointer callbacks
│   ├── callback_with_pointerfn_arguments.c
│   └── performing_fn_on_array_using_callback.c
├── command_line_arguments/
│   ├── cmd_line_arg.c                # argc & argv demonstration
│   └── main_fn_parameters_atoi.c     # Parsing numeric arguments
├── dynamic memory concepts and quetions/
│   ├── dynamic_memory_allocation.c   # Allocation fundamentals
│   ├── malloc_calloc_example.c       # malloc vs calloc comparison
│   ├── malloc_example.c              # Basic malloc usage
│   ├── malloc_realloc_calloc_free.c  # Complete dynamic lifecycle
│   ├── malloc_realloc_example.c      # Resizing buffers with realloc
│   └── malloc_with_realloc.c         # Realloc expansion patterns
├── Enumerated Data type/
│   ├── enum_basics.c                 # Basic enum definitions
│   ├── enum_ex1.c                    # Custom enum values
│   ├── enum_ex2.c                    # Switch-case dispatch with enums
│   └── enum_ex3.c                    # Enum usage examples
├── Extern storage classes example/
│   ├── extern_access_support.c       # Main translation unit using extern
│   └── support.c                     # Secondary unit exporting symbols
├── File Handling/
│   ├── FILE HANDLING (ERROR HANDLING)/
│   │   └── error_handling_basics.c   # errno error codes and interpretation
│   └── FILE HANDLING BASICS/
│       ├── file_handling_basic.c     # File open/close/write
│       ├── file_handling_reading.c   # fgets, fputs, fseek, ftell
│       ├── file_handling_array.c     # Saving and reading array data
│       ├── file_handling_ex2.c       # File appending and reading
│       ├── fie_handling_ex3.c        # File stream processing
│       └── find_sum.c                # Reading numbers from file and summing
├── Function concepts and quetions/
│   ├── 1d_pointer_array.c            # Passing pointer arrays to functions
│   ├── 2d_matrix_using_func.c        # 2D matrix manipulation in functions
│   ├── doubling_array_by_passing_pointer_array_to_func.c
│   ├── factorial.c                   # Recursive factorial
│   ├── marks_of_students.c           # Student marks record computation
│   ├── passing_pointers_into_func.c  # Pass-by-reference mechanics
│   ├── reversal_number.c             # Integer reversal
│   ├── sum_function_program.c        # Function modularity
│   └── sum_using_pointers.c          # Pointer-based addition
├── Matrix_array_quetions_with conepts and using pointers/
│   ├── 2d_array_of_pointer.c         # Dynamic 2D arrays via pointer array
│   ├── 2d_array_of_pointers_example1.c
│   ├── array_pointer.c               # Array indexing vs pointer arithmetic
│   ├── largest_element.c             # Finding max element in array
│   ├── product_matrix_3X3.c          # 3x3 matrix multiplication
│   ├── product_matrix_of_mXn.c       # Arbitrary dimension matrix product
│   └── transpose_of_2x3.c            # Matrix transpose
├── Some pointer quetions/
│   ├── 2d_pointer_array_of_strings.c # Array of string pointers
│   ├── acessing_1d_pointer_array.c   # Traversal via pointers
│   ├── const_program.c               # Const correctness with pointers
│   ├── string_cmp_using_pointer.c    # Custom strcmp via pointers
│   ├── swap_elements.c               # Swapping array elements
│   ├── swap_no_using_ptr.c           # Classic pointer swap
│   └── test.c                        # Scratch test file
├── Some extra programs/
│   ├── atm_simulation_very_basic.c   # Basic ATM console flow
│   ├── digit_counter.c               # Counting digits in integer
│   ├── digit_counter_another_one.c
│   ├── fibonnaci.c                   # Fibonacci series
│   ├── pyramid.c                     # Star/number pyramid pattern
│   ├── repeating_digits_checker.c    # Detecting duplicate digits
│   └── traversing_an_array_to_find_element.c
├── binary and linear search/
│   └── binary_search.c               # Binary search on sorted array
├── linked_list/
│   ├── link_list_ex.c                # Linked list node operations
│   └── singly_linked_list.c          # Singly linked list (insert, delete, display)
├── stack/
│   ├── push_op_using_linked_list.c   # Stack push using linked list
│   └── pop_using_linked_list.c        # Stack pop using linked list
├── string conepts and quetions/
│   ├── str_op.c                      # Common string operations
│   ├── strcmp_without_builtinfn.c    # Custom string comparison
│   ├── string_compare_using_ptr.c    # Pointer-based string compare
│   └── string_len_without_builtinfn.c# Custom string length calculation
├── Structures Conepts/
│   ├── Nested Structures/
│   │   └── nested_struct_ex.c        # Embedded structures
│   ├── Structures concepts and quetions/
│   │   ├── arrays_within_structures.c# Array members in struct
│   │   ├── size_of_structure.c       # Padding and alignment analysis
│   │   ├── struct.c                  # Struct basics
│   │   ├── struct_with_array_obj.c   # Array of struct instances
│   │   └── subject_marks_of_multiple_students_using_struct.c
│   ├── offset function in union and structure/
│   │   └── offset_fn_ex.c            # offsetof() macro demonstration
│   ├── structures_passing_into_fn/
│   │   ├── pass_by_value_and_ref_using_struct.c
│   │   └── struct_in_function.c      # Functions returning/accepting structs
│   └── structures_using_pointers/
│       └── struct_using_pointers.c   # Pointer access to struct members (->)
├── typedef and union/
│   ├── typedef_keyword_example.c     # Type aliasing with typedef
│   └── union_example.c               # Memory sharing in unions
└── some practice quetions/           # 22+ practice exercises
    ├── armsrong_no.c                 # Armstrong number check
    ├── bin_array_using_ptr.c         # Binary array handling
    ├── circular_array.c              # Circular buffer/array traversal
    ├── copy_string.c                 # Custom string copy
    ├── date_breakdown.c              # Parsing DD/MM/YYYY
    ├── digit_freq.c                  # Frequency counter for digits
    ├── display_2d_array.c            # Formatted 2D matrix print
    ├── emp.c                         # Employee record management
    ├── fibbonacci.c                  # Fibonacci series variations
    ├── normalize_strings.c           # String normalization & cleaning
    ├── palindrome.c                  # Palindrome verification
    ├── prime_number_checker.c        # Primality test
    ├── realloc_example.c             # Memory reallocation exercise
    ├── reversal_string.c             # In-place string reversal
    ├── reverse_array_using_ptr.c     # Array reversal using pointers
    ├── reverse_num.c                 # Numerical reversal
    ├── selection_sort_even_sort.c    # Sorting even elements with selection sort
    ├── selection_sort_in_descending.c# Descending selection sort
    ├── str_tokenize.c                # String tokenization practice
    ├── sum_of_individual_digits_in_int.c # Sum of digits
    └── traingle_pattern.c            # Asterisk pattern printing
```

---

## 🛠 Compilation & Execution Guide

### Prerequisites
Make sure you have a standard C compiler installed (e.g., `gcc` or `clang`):
```bash
# Debian / Ubuntu
sudo apt install build-essential

# Arch Linux
sudo pacman -S base-devel

# macOS
xcode-select --install
```

### Single-File Compilation
Compile any single `.c` file using `gcc` with standard warning flags:
```bash
gcc -Wall -Wextra -O2 "linked_list/singly_linked_list.c" -o singly_linked_list
./singly_linked_list
```

### Multi-File Compilation (Storage Classes)
For programs relying on external symbols across multiple translation units (e.g., the `extern` examples):
```bash
cd "Extern storage classes example"
gcc -Wall extern_access_support.c -o extern_demo
./extern_demo
```

### Programs with Command-Line Arguments
For programs under `command_line_arguments/`:
```bash
gcc -Wall command_line_arguments/cmd_line_arg.c -o cmd_arg
./cmd_arg arg1 arg2 123
```

---

## 🏷 Recommended GitHub Repository Settings

To maximize discoverability and presentation on GitHub:

### **About / Description**
> *A comprehensive, hands-on repository of C programming from fundamentals to advanced concepts: pointers, dynamic memory allocation, data structures (linked lists, stacks), bitfields, callbacks, file I/O, and problem-solving.*

### **Topics / Tags**
`c` • `c-programming` • `pointers` • `data-structures` • `dynamic-memory-allocation` • `memory-management` • `linked-list` • `stack` • `bitfields` • `file-handling` • `algorithms` • `computer-science`

---

## 👨‍💻 Author & Acknowledgments

- **Chethan S** ([@chethan779](https://github.com/chethan779))
- Developed for deep learning, conceptual clarity, and rigorous practical mastery of low-level C programming.
