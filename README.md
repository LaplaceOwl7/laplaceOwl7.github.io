# CS499: Capstone

<!-- This markdown code was AI-Assisted for formatting and flow  -->

## Professional Self-Assessment

My name is Chad Salaets, a computer science graduate from Southern New Hampshire University. The computer science program has been an important journey for me over the past 2.5 years. I originally began as a chemistry major, but transitioned into computer science as my career goals shifted toward areas more aligned with computer science and mathematics.

My time at SNHU changed how I think about software development. Instead of focusing only on writing code that works, I learned to think more like a software engineer, considering architecture, design trade-offs, and maintainability. Early coursework focused mainly on correctness, while later courses emphasized design quality, scalability, and structure. The capstone required pulling together multiple areas of the discipline rather than working within a single subject. It involved secure coding practices, database management, systems architecture, and quality assurance. This portfolio reflects growth through refactoring, enhancement, and justification of design decisions rather than creating new projects from scratch.

Communication between developers and stakeholders is critical in software development. My background in chemistry helped me learn how to explain complex topics in a clear and accessible way, which translated well into computer work. Throughout the program, collaboration was developed through feedback cycles with instructors in revisions. Coursework required interpreting unclear requirements, explaining technical decisions during code reviews, writing documentation for future maintenance, and organizing code so others could modify it safely. Clear naming conventions, comments, and structure helped communicate intent without excessive explanation. Adjusting technical depth depending on the audience was a common requirement. Documentation, logs, benchmarks, and schema descriptions were designed so future developers and stakeholders could understand the system and make informed decisions about performance, security, and design trade-offs.

The software engineering portion of the capstone focused heavily on the separation of concerns. Responsibilities were isolated, and systems were designed around interfaces instead of concrete implementations. Revising existing code to improve maintainability is an important skill, especially when working on systems where not everything can be rewritten. Applying object-oriented principles intentionally, rather than mechanically, showed their value in managing complexity and supporting long-term stability.

The capstone also provided an opportunity to apply algorithmic thinking to improve performance and scalability. Data structures were selected based on access needed and system needs rather than theory alone. Balancing theoretical complexity with real-world performance required careful consideration of the system’s purpose. Benchmarking and analysis were used to justify decisions using measured results instead of assumptions. Performance tables and reports made it easier to compare algorithm behavior as data size increased.

Security was treated as a design concern throughout the project. Input validation, parameterized queries, and defensive programming practices were applied consistently to handle malformed input, misuse, or unexpected behavior. These decisions helped reduce risk at system boundaries and reinforced data integrity rather than relying on the user to provide the correct data.

Overall, the software design, algorithmic work, and database integration function together as a single system. Modular architecture supports interchangeable algorithms, algorithms operate on persistent relational data, and database constraints help enforce correctness and security. This portfolio demonstrates readiness for entry-level software engineering or backend development roles by showing the ability to work with existing codebases, improve structure and security, and reason about performance, data, and system design in a practical setting.

## Reflection: Skills Developed

Each category forced me to learn about computer science as a whole. Each category was a opportunity to develop a strong basis of skills.

### Category One: Software Engineering

- Learned how to use best practice tools:
    - CMake
    - Doxygen
    - Markdown
- Learned how separation of concerns can improve system clarity by isolating concerns like data and presentation.
- Gained an increased understanding of layered architecture and how tight coupling between modules quickly becomes overly complex.
- Learned to decide the responsibilities of modules and assign them per class based on their purpose.
- Designed clear interfaces using headers without exposing internal details.
- Demonstrated the perks of object-oriented code in a system's complexity. 
- Learned to apply encapsulation instead of treating all classes like data structures. 
- Understood the constructor design. 
- Learned separation in headers and source files. 
- Gained experience in circular dependencies.
- Learned to bias small classes with a focused purpose.
- Recognized how monolithic designs can cripple testing and reuse.
- Learned how to anticipate future requirements.
- Learned to write self-documenting code. 
- Learned that minimizing headers introduces Weaknesses.
- Garnered more confidence in refactoring, knowing I won't break the code; and if I do, I'll fix it.

### Category 2: Data Structures & Algorithms

- Learned to properly decide an algorithm's choices driven by data size, input characteristics, and usage patterns instead of just optimized code.
- Gained insights into simpler algorithms that can outperform complex ones thanks to constant factors.
- Learned to evaluate trade-offs between time complexity, space complexity, and code maintainability.
- Developed a strong rationale for determining the best, average, and worst-case behaviors.
- Learned how algorithmic inefficiencies are only visible in larger datasets.
- Learned the specific quirks in choosing containers like vector, map, and unordered_map, which affect the algorithm's performance.
- Learned to design data structures with healthy access patterns, not for data representation (preReq vectors vs preReq objects).
- Gained experience in developing polymorphic code using swap algorithms.
- Learned that theoretical complexity must be proven with data-based evidence.
- Learned to use performance data to justify design choices rather than comfort or theory. 
- Learned to validate algorithms for empty inputs, malformed data, or single-element datasets.
- Learned to build defensive checks in regards to performance.
- Demonstrated how to communicate algorithmic decisions in non-technical terms.


### Category 3: Database Management

- Learned to translate real-world requirements into normalized schemas.
- Gained experience in defining constraints to force correct data formats.
- Learned how schema design has long-term implications for future revisions.
- Learned how to use primary keys, uniqueness constraints, and Not Null enforcement. 
- Demonstrated how databases can prevent bugs that are not caught in application checks.
- Demonstrated why files are a poor choice in concurrency, scale, and complexity concerns. 
- Learned to write parameterized queries to avoid injection vulnerabilities. 
- Learned how to separate data access logic from business logic. 
- Gained experience in designing layers to isolate the SQLite database from the application code. 
- Learned how to use the SQLite library in C++.
- Demonstrated how database connection failures and query errors are handled gracefully.
- Demonstrated how to log database interactions for debugging, traceability, and security. 
- Demonstrated how user authentication can be enforced.
- Understood how database constraints can complement and enforce secure coding.
- Learned how database systems can and should reflect the system's entire architecture.
- Learned the process of reasoning how data will flow across the system's layers.

## Link to GitHub Repository:

### Prior to Enhancements

[CS300: Data Structures And Algorithms](https://github.com/LaplaceOwl7/Data-Structures-And-Algorithms)

### Code Review

[Code Review of the Original Code](https://youtu.be/naC4lX37uyY)
### After Enhancements

[CS:499 Project](https://github.com/LaplaceOwl7/CS499-CapStone-AlgorithmicAnswers)


## Introduction to Enhancements


### Overview

The original design of this project was a class taken at Southern New Hampshire University's Computer Science program. The class was CS300: Data Structures and Algorithms. The final project was designed to evaluate the students' knowledge of algorithms, C++ coding skills, and knowledge of file management within C++. The original file was a single CPP file that replicated a software to store course objects that represented actual courses found at a university. The single CPP file was complete with a function to extract information from a CSV file, create a vector with all course objects, and alphabetically sort the vector by CourseIDs.

### Motivation for enhancing the artifact

Southern New Hampshire University students take capstone courses, where all the skills and knowledge learned from the program are tested. The goal was to revise the code base to demonstrate the knowledge and skills learned in the program.

The project had three enhancement categories planned:
  - Software Engineering & Design
  - Algorithms & Data Structures
  - Database / Data Management
  
#### Overview

All 3 artifacts are from the same source. This artifact was from the CS300: Data Structures and Algorithms class. The purpose was to install a sorting algorithm so that a mock school's database would contain courses, each with a course title, course ID, and prerequisites. The project included a single C++ file equipped with a CSV file to pull the information from. The original code was my first introduction to C++, and did not follow best practice security guidelines.

The inclusion of this artifact demonstrates my technical growth in the C++ language as a whole, and demonstrates my awareness of common C++ pitfalls like lack of input validation, safe file handling, etc. The industry-relevant skills here are the ability to stick to a coding guideline, use best practice tools like CMake, Doxygen, and SQLite. It aligns with my interest in software engineering programs close to the metal, like virtualization engines. 

The original version was riddled with issues, like a lack of input sanitization from CIN and the CSVs. The architecture was poorly designed with a master vector holding all the courses, and the only way to modify any courses was via the CSV file. The technical debts here were incurred in favor of implementing an algorithm. The purpose of this class was to learn about data structures like binary search trees and heaps, and the algorithms commonly found, not full secure coding. 

---

### Category 1: Software Engineering & Design Enhancements

#### Design Rationale

##### Object-Oriented Refactoring

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
- Aligns with standard software engineering outcomes: clear separation of concerns, robust error handling, data integrity, and modular architecture, all of which matter in professional-quality software systems.


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

- All input data, whether from CSV import or user prompts, is validated before processing: format checks, field presence, sanity checks.
- Edge cases are handled: malformed CSV rows, missing fields, invalid types, duplicate IDs, or invalid user input are detected early and handled gracefully rather than causing undefined behavior.
- Sanitization and validation act as a defensive layer to protect internal data structures and database integrity, reducing risks of corruption or unexpected failure.

### Error Logging Mechanism

- The file `Err.cpp` implements error logging: whenever an exception, invalid input, or database error occurs, relevant details are written to a log.
- Logged data includes context (what operation failed, what data was involved), so future debugging or forensic analysis can trace root causes.
- Proper error logging helps identify recurring issues, unexpected input patterns, and supports maintainability over time, rather than silent failures or crashes that are harder to reproduce.

### Separation of Error Logs vs. User Action Logs

- Error logs (from `Err.cpp`) are separate from user-action logs (from `Recorder.cpp`): this separation enables clarity between normal operations and exceptional/error conditions.
- Such a distinction allows for easier monitoring, debugging, auditability, and analysis.
- This approach aligns with logging best practices: structured, purpose-specific logs improve observability without overwhelming developers with mixed, noisy logs.

---


