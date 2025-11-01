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

Awaiting Confirmation to begin project...
