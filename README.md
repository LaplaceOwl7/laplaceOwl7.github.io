# CS499 Computer Science Capstone Project
### Enhancing and Integrating Software Systems Through Design, Algorithms, and Databases

---

## Developer Information
**Name:** Chad Salaets 

**Program:** Bachelor of Science in Computer Science

**Concentration:** Software Engineering  

**Institution:** Southern New Hampshire University (SNHU)  

**Course:** CS-499: Computer Science Capstone  


---

## **Project Title**

### **Revising CS260 Course Sorting Application**

---

## **Project Overview**
This capstone project demonstrates my evolution of foundational C++ programming skills. The artifact was originally developed in CS260: Data Structures and Algorithms into a modular, scalable system.

The capstone enhancement process showcases professional-level competencies in topics such as:
- **Software Design and Engineering** Refactoring procedural code into object-oriented architecture using a modular approach.
 
- **Algorithms and Data Structures** — Implementing and benchmarking multiple sorting algorithms (Bubble, Merge, and Quick Sort, and potentially more, with runtime analysis and performance evaluation, including reports on the algorithms.

- **Databases** — Integrating a SQLite relational database to replace the static CSV storage to provide persistent data management and secure CRUD operations.

Combined, these enhancements illustrate my growth in the core domains of computer science while emphasizing structured thinking, algorithmic problem-solving, and practical database integration.  

---

## **Project Deliverables**

The project is divided into three objectives:

- **Software Design and Engineering**
	- Create classes to uphold object-oriented principles and modularize the application.
		- Add course class
		- Add CourseManager class.
	- Implement a menu or controller to dictate the program’s core flow.
	- Improve the code’s readability and maintainability
	- Use consistent naming conventions
	- Divide implementation logic into header and source files
	- Uphold secure coding practices:
		- Integrate error handling to catch malformed CSVs or input validation.
		- Integrate Input sanitization
	- System Improvement
		- Architecture will be split into multiple files
		- Sorting class and validator to avoid malformed data.
		- An error logging class that writes to a file.


- **Algorithms and Data Structures**
	- Implement multiple sorting algorithms
		+ Merge Sort
		+ Quick Sort
		+ Bubble Sort (revise)
		+ Insertion Sort (Optional)
		+ Bucket Sort (Optional)
		+ Radix Sort (Optional)
	- Implement algorithmic benchmarking
		+ Records execution time and compares them
		+ Generates a formatted summary table with the number of elements, the algorithm chosen, and the total runtime in milliseconds.
	- Move course data into a vector for dynamic resizing.
	- (Optional) Markdown files with a report on each algorithm, including strengths, weaknesses, O-complexity best case and worst case, tangible examples, and best-practice use-cases


- **Databases**
	- Create a SQL table with courseID as the primary key.
		+ unique courseIds
		+ Parameterize all queries to mitigate injections
		+ log all user actions in a separate log
	- Implement basic CRUD operations
		+ addCourse
		+ removeCourse
		+ updateCourse
		+ fetchAllCourses
		+ searchCourseById
		+ searchCourseByName
	- Integrate the database layer into the CourseManager class
	- Add user menu

---

### Status

### Category One: Software Engineering & Design

##### Object-Oriented Refactoring

| Promised Deliverable | Status | Rationale |
|------|--------|-----------|
| Create a `Course` class for course objects | Fulfilled | Course.cpp and Course.hpp now exist |
| Create a `CourseManager` class to handle CSV/database operations | Fulfilled | CourseManager.cpp and CourseManager.hpp exist; Validator.cpp handles CSV |
| Add a main controller or menu system to manage program flow | Fulfilled | main.cpp manages program flow |
| Separate UI/menu logic from data and backend logic | Waived | UI design in C++ is not trivial like in Java|

##### Architecture & Maintainability

| Promised Deliverable  | Status | Rationale |
|------|--------|-----------|
| Modularize project into logical components | Fulfilled | Project2.cpp was split into 7+ cpp files with individual headers; Each completes 1-3 tasks.|
| Implement encapsulation and abstraction (hide internal data, expose clear interfaces) | Fulfilled | HPPs abstract internal data|
| Use design patterns where appropriate (factory, strategy, etc.) | Waived | Not often implemented correctly; Singleton not needed for project; avoid unnecessary complexity |
| Add UML diagrams for design validation and communication | Fulfilled | Diagrams, class information, and flow created via Doxygen; See `/html/index/html` 

##### Security & Stability

| Promised Deliverable  | Status | Rationale |
|------|--------|-----------|
| Add input sanitization for course input data | Fulfilled  | Basic CSV validation found in Validator.cpp |
| Catch malformed CSV input and handle gracefully | Fulfilled |Basic CSV validation found in Validator.cpp |
| Implement file validation and format checking | Fulfilled | Basic CSV validation found in Validator.cpp |
| Add error logging class to write to file | Fulfilled | Err.cpp generates logs that are stored in /log/details.log |

##### Professional Practices

| Promised Deliverable  | Status | Rationale |
|------|--------|-----------|
| Document design rationale and class responsibilities | Pending | |
| Justify architectural trade-offs and pattern choices | Pending | |
| Ensure maintainability and scalability are demonstrated | Fulfilled | Demonstrated within code|

##### Extra (Not Promised)

| Extended Deliverable  | Status | Rationale |
|------|--------|-----------|
|Used common professional tools  | Fulfilled | Doxygen; CMake; and MDs used |
| Adopt a unified coding standard| Partially Fulfilled | CPP Best practices adopted; mostly complete adoption. |
| Ensure maintainability and scalability are demonstrated | Fulfilled | Demonstrated within code|

#### Category Two: Data Structures & Algorithms:

##### Algorithm Implementation
- [ ] Implement multiple sorting algorithms:
  - [ ] Bubble Sort (refactored)
  - [ ] Merge Sort
  - [ ] Quick Sort
  - [ ] Insertion Sort *(optional)*
  - [ ] Bucket Sort *(optional)*
  - [ ] Radix Sort *(optional)*
- [ ] Add abstraction layer: base `Sorter` class with polymorphism  

##### Performance & Benchmarking
- [ ] Add benchmarking module:
  - [ ] Record execution time in milliseconds  
  - [ ] Compare runtime across algorithms  
  - [ ] Generate formatted summary report  
- [ ] Analyze time and space complexity for each algorithm  
- [ ] Document O-complexity (best, average, worst case)  

##### Data Management
- [ ] Move all course data into a vector for dynamic resizing  
- [ ] Maintain consistent data handling between algorithms  

##### Documentation
- [ ] Include Markdown reports on algorithm performance and use cases  
- [ ] Clearly explain algorithm choice and trade-offs 

#### Category Three: Databases
##### Transition to Database
- [ ] Replace CSV with a SQLite relational database  
- [ ] Define relational schema with constraints:
  - [ ] `courseID` as `PRIMARY KEY`
  - [ ] `courseName` as `NOT NULL`
- [ ] Parameterize all SQL queries (prevent injection attacks)  

##### CRUD Implementation
- [ ] Implement full CRUD operations:
  - [ ] `addCourse()`
  - [ ] `removeCourse()`
  - [ ] `updateCourse()`
  - [ ] `fetchAllCourses()`
  - [ ] `searchCourseById()`
  - [ ] `searchCourseByName()`
- [ ] Integrate CRUD into the `CourseManager` class  

##### Database Management
- [ ] Add database connection and disconnection handling  
- [ ] Log all user actions into separate log files  
- [ ] Include schema creation on first connection  

##### User Interface / Interaction
- [ ] Add user menu options:
  - [ ] “Load Courses”
  - [ ] “Add Course”
  - [ ] “Delete Course”
  - [ ] “Display Course”
  - [ ] “Export Sorted Courses”  

##### Security & Design
- [ ] Enforce unique course IDs  
- [ ] Use parameterized queries for injection prevention  
- [ ] Separate SQL logic from main application logic (data access layer abstraction)  

