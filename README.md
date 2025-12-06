# CS499: Capstone

<!-- This markdown code was AI-Assisted  -->

## Link to GitHub Repository:

[Source Code](https://github.com/LaplaceOwl7/CS499-CapStone-AlgorithmicAnswers)

## 0. Introduction


To be added


## 1. Introduction & Purpose of Enhancements


### Overview

The original design of this project was a class taken at Southern New Hampshire University's Computer Science program. The class was CS300: Data Structures and Algorithms. The final project was designed to evaluate the student's knowledge on algorithms, C++ coding skills, and knowledge in file management within C++. The original file was a single CPP file that replicated a software to store course objects that represented actual courses found at a university. The single CPP file was complete with a function to extract information from a CSV file, create a vector with all course objects, and alphabetically sort the vector by CourseIDs.

### Motivation for enhancing the artifact

Southern New Hampshire University students take capstone courses, where all the skills and knowledge learned from the program are tested. The goal was to revise the code base to demonstrate the knowledge and skills learned in the program.

The project had three enhancement categories planned:
  - Software Engineering & Design
  - Algorithms & Data Structures
  - Database / Data Management

---

### Category 1: Software Engineering & Design Enhancements

#### Object-Oriented Refactoring

##### Classes

Classes like `Course`, `CourseManager`, `Validator`, `DataManager`, `Benchmarker`, `Err`, and Recorder` were created in this enhancement.

#### Architecture & Maintainability Improvements

- The project is modularized into multiple `.cpp` and `.hpp` files. The compartmentalization enhances readability and manages complexity as the code base evolves.
- Waiving UI separation was a conscious design choice: since UI layering in C++ (console-based) wasn’t critical to the core functionality, avoiding over-engineering keeps development focused and maintainable without unnecessary abstraction overhead.
- With code organized logically and documented, future developers (or me in several months) can understand the structure, dependencies, and responsibilities, significantly simplifying the debugging, extension, and refactoring.
- Adopting consistent naming conventions and C++ code organization makes code predictable and uniform.

#### Security & Stability Enhancements

- Validating CSV input and handling malformed or invalid data reduces the risk of unexpected crashes or corrupted data, and is are critically important defensive programming practice.
- Error logging via `Err.cpp` and user action logging via `Recorder.cpp` provide traceability and diagnosis of runtime issues, user mistakes, or invalid operations without crashing the system.
- Defensive programming (validations, careful input checking, error handling) reduces attack surface or unexpected behavior if unexpected input/data arises. Even in small projects, these practices increase stability under edge cases.

#### Professional Engineering Practices

- Use of documentation tools like Doxygen, build-system tools like CMake, and Markdown reports reflects real-world software engineering workflows, promoting readability and collaboration.
- The code structure, modular design, and defensive practices support maintainability and scalability, preparing the project for extension or reuse.
- Aligns with standard software engineering outcomes: clear separation of concerns, robust error handling, data integrity, modular architecture, all of which matter in professional-quality software systems.


---

## Category 2: Algorithms & Data Structures Enhancements

Category two was concerned with the algorithms and data structures of the code. The most important work was to implement MergeSort, QuickSort, and StandardSort, in addition to making all functions reachable from `Sorter.cpp`.

### Implemented Sorting Algorithms

- Bubble Sort
- Merge Sort
- Quick Sort
- Standard Library Sort (`std::sort`)

- Source file locations:
  - `BubbleSort.cpp.cpp`, simple, educational, baseline sorting implementation
  - `MergeSort.cpp`  divide-and-conquer stable sort, good for large or unpredictable data
  - `QuickSort.cpp`, in-place, average-efficient sort, good for general-purpose use
  - `std::sort` (standard library), production-quality, optimized sort used as a baseline for performance comparison

### Theoretical Algorithm Analysis

For each sorting algorithm:

- **Time Complexity (Big-O)**
  - Bubble Sort: average/worst **O(n²)**; best case (nearly sorted) **O(n)**
  - Merge Sort: always **O(n log n)**
  - Quick Sort: average **O(n log n)**; worst **O(n²)** 
  - `std::sort`: treated as a well-optimized baseline (often using introspective sort or similar; complexity effectively behaves as **O(n log n)** in most realistic cases)

- **Space Complexity**
  - Bubble Sort: in-place, **O(1)** auxiliary memory
  - Merge Sort: **O(n)** extra memory for merging (unless optimized in-place variant used)
  - Quick Sort: **O(log n)** stack space (recursive calls) or more, depending on implementation/partitioning.

- **Strengths / Weaknesses & Use Cases**
  - Bubble Sort: very simple and stable; good for small or nearly-sorted datasets or educational demonstration. But inefficient for large or random data.
  - Merge Sort: reliable performance (n log n) regardless of input order, stable; good for large datasets or when stability matters; but uses additional memory.
  - Quick Sort: Very efficient on average with low overhead; good general-purpose sort. But worst-case performance if pivot selection is poor; instability may be an issue in contexts needing a stable sort.
  - `std::sort`: optimized, likely includes hybrid strategies; good for production use where performance and robustness are priorities.

### Benchmarking Methodology

- Used input dataset `seedInput.csv` for consistent baseline data.
- Conducted 100 runs per sorting algorithm to average out variance and obtain stable measurement results.
- Measured **execution time in milliseconds as a performance metric.
- Ensured environment consistency across runs (same hardware, input dataset, no extraneous load) to make comparisons reliable.
- Compared implemented sorts against `std::sort` to provide a baseline and highlight practical performance differences.

### Benchmarking Results & Interpretation

- Results (in a tabular format) show how algorithms scale with increasing data size, allowing direct comparison between theoretical expectations and empirical performance.
- Observations:
  - For small datasets, simpler algorithms (Bubble Sort) may perform competitively due to low overhead despite poor asymptotic behavior.
  - As dataset size grows, algorithms with O(n log n) complexity (Merge Sort, Quick Sort, `std::sort`) outperform quadratic sorts significantly.
  - `std::sort` generally performs best due to optimized implementation and lower constant factors.
  - Performance differences align with Big-O theory: algorithms with better complexity scale more gracefully as `n` increases.

### Algorithmic Trade-Off Discussion

- **Stability vs. Performance**: Merge Sort offers stability and consistent performance; Quick Sort offers speed but is unstable and can degrade in the worst case; Bubble Sort is stable but inefficient except for very small or nearly-sorted data.
- **Predictability vs. Overhead**: Merge Sort’s extra memory overhead may be costly for memory-constrained environments; Quick Sort and in-place sorts avoid that at the expense of worst-case risk.
- **Practical Use in Production**: `std::sort` remains industry-preferred because it balances speed, reliability, and implementation robustness. For real-world applications, using a well-tested standard library sort often outweighs custom implementations.
- **When to Use What**:
  - For small or nearly sorted data, simple sorts may suffice.
  - For large data sets with unknown properties, prefer Merge or Quick Sort (or `std::sort`) for performance.
  - If element stability matters, choose Merge Sort (or stable sort variant).
  - For production code aiming at maintainability and performance, rely on standard library sorts unless custom behavior is needed.

---

## Database Enhancements & Data Management

Category 3 focused on database management, including CRUD methods for database modifications.

### Motivation for Migrating from CSV to SQLite

- CSV is simple and is  human-readable, but is limited when data integrity, constraints, or complex queries are needmanagement, relational database like SQLite supports constraints, schema enforcement, and efficient querying, avoiding custom parsing and query-code maintenance required for CSV-based querying.
- SQLite is serverless and embedded: no extra database server required, making it lightweight while providing “database-level” guarantees (integrity, transactions, indexing) that CSV lacks.

### Database Schema Design

- Defined schema includes `courseID` as `PRIMARY KEY` and `courseName` as `NOT NULL`, enforcing uniqueness and preventing null names.
- Prerequisites or other relational data have been handled appropriately to preserve relational integrity and avoid duplication of inconsistent data.
- These constraints ensure data consistency, avoid duplicate or malformed records, and maintain referential/data integrity over time, which CSV-based storage cannot guarantee robustly.

### CRUD Functionality Implementation

- Provided functions: `addCourse`, `removeCourse`, `updateCourse`, `fetchAllCourses`, `searchCourseById`, `searchCourseByName`.
- Each operation uses parameterized SQL queries, which prevents injection vulnerabilities and ensures safe handling of user input before interacting with the database.
- Error handling is in place: database connection open/close, invalid inputs, and failed queries are managed gracefully (not left to undefined behavior).
- This provides a full data-access API, replacing brittle CSV parsing and risky file operations with robust, testable, and maintainable database interactions.

### Data Access Layer Architecture

- Separation of concerns: `DataManager` encapsulates all direct SQL/DB operations; `CourseManager` implements business logic and higher-level course management.
- This decoupling improves maintainability (you can change DB backend or schema without affecting business logic), testability (unit test business logic independently of database), and security (all SQL confined to one layer).
- It aligns with design-pattern best practices: data-access layer abstraction improves modularity and future extensibility.

### User Action Logging

- The file `Recorder.cpp` logs all user actions, providing an audit trail of operations performed.
- This supports accountability, debugging, and understanding historical data modifications, important for reliability, traceability, and potential rollback or audits.
- In professional systems, action logging is critical for diagnosing issues, reproducing bugs, and maintaining data provenance. Even for small projects, it is a sign of mature engineering practice.

---

## Validation, Error Handling, and Logging

### Input Validation Strategy

- All input data , whether from CSV import or user prompts , is validated before processing: format checks, field presence, sanity checks.
- Edge-cases are handled: malformed CSV rows, missing fields, invalid types, duplicate IDs, or invalid user input are detected early and handled gracefully rather than causing undefined behavior.
- Sanitization and validation act as a defensive layer to protect internal data structures and database integrity, reducing risks of corruption or unexpected failure.

### Error Logging Mechanism

- The file `Err.cpp` implements error logging: whenever an exception, invalid input, or database error occurs, relevant details are written to a log.
- Logged data includes context (what operation failed, what data was involved), so future debugging or forensic analysis can trace root causes.
- Proper error logging helps identify recurring issues, unexpected input patterns, and supports maintainability over time , rather than silent failures or crashes that are harder to reproduce.

### Separation of Error Logs vs. User Action Logs

- Error logs (from `Err.cpp`) are separate from user-action logs (from `Recorder.cpp`): this separation enables clarity between normal operations and exceptional/error conditions.
- Such distinction allows for easier monitoring, debugging, auditability, and analysis.
- This approach aligns with logging best practices: structured, purpose-specific logs improve observability without overwhelming developers with mixed, noisy logs.

---
