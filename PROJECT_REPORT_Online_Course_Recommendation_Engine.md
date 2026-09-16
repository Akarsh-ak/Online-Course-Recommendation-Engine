# DSA: 25 – Online Course Recommendation Engine

## 1. Project Overview

The **Online Course Recommendation Engine** is an academic project for **Data Structure and Algorithms - II (CCSE0301)**. The project explores how suitable data structures and algorithms can organize online course information, search courses efficiently, rank relevant courses, and present recommendations to students.

The main problem is that online learning platforms contain a large number of courses. A student may know the topic or skill they want to learn but still find it difficult to choose a suitable course. This project proposes a DSA-based approach to make course searching and recommendation easier.

**Student:** Akarsh Singh  
**Branch:** B.Tech CSE-A  
**Course:** Data Structure and Algorithms - II  
**Course Code:** CCSE0301  
**Faculty:** Mr. Shamshad Ali  
**Assignment:** Individual Assignment  
**SDG:** SDG 4 – Quality Education

---

## 2. Problem Statement

Students have access to many online courses covering similar subjects. Comparing these courses manually can take time.

The proposed system organizes course information and helps a student find suitable courses based on interests, skills, level, and course relevance.

The project focuses on applying **Data Structures and Algorithms** rather than depending entirely on machine learning.

---

## 3. Problem Context

For example, a student interested in programming may find courses for C, C++, Python, Java, Data Structures, Algorithms, Web Development, and Machine Learning.

The student may want to compare courses using factors such as:

- Topic or category
- Required skills
- Difficulty level
- Duration
- Rating
- Prerequisites
- Relevance to the student's interest

A recommendation engine can organize this information and produce a ranked list of suitable courses.

---

## 4. Objectives

1. Recommend suitable online courses.
2. Organize course information using appropriate data structures.
3. Provide efficient course searching.
4. Support insertion, deletion, and modification of course records.
5. Rank suitable courses.
6. Sort recommendation results.
7. Represent relationships between related courses.
8. Apply Trees, Heaps, Priority Queues, and Graphs.
9. Demonstrate practical applications of DSA.
10. Develop a simple academic prototype.

---

## 5. Target Users

### Students
The primary users who search for courses and receive recommendations.

### Teachers and Mentors
Can use the system concept to guide students toward relevant learning resources.

### Learning Platforms
The concept can be extended to a learning platform that organizes and recommends courses.

---

## 6. Scope

### Included

- Course record management
- Course searching
- Course insertion
- Course deletion
- Course modification
- Course ranking
- Course sorting
- Course category organization
- Course relationship representation
- DSA-based recommendation logic

### Future extensions

- User profiles
- Course ratings and reviews
- Personalized recommendations
- Machine learning
- Real course APIs
- Web interface
- Database integration
- Recommendation history

---

## 7. System Workflow

```text
Student Input
     |
     v
Interests / Skills / Level
     |
     v
Course Search
     |
     v
Course Matching
     |
     v
Recommendation Score
     |
     v
Priority Queue / Heap
     |
     v
Sorting
     |
     v
Recommended Courses
```

---

## 8. DSA Concepts and Their Applications

| DSA Concept | Proposed Application |
|---|---|
| Binary Tree | Organize course categories |
| Memory Representation of Tree | Store course information |
| In-order Traversal | Visit courses in sorted order |
| Pre-order Traversal | Process course hierarchy |
| Post-order Traversal | Process child records before parent |
| Constructing Binary Tree from Traversal | Build course hierarchy |
| BST Insertion | Add courses |
| BST Deletion | Remove courses |
| BST Searching | Find courses |
| BST Modification | Update course information |
| Binary Heap | Rank recommendations |
| Threaded Binary Tree | Support efficient traversal |
| Threaded Tree Traversal | Visit records |
| AVL Tree | Maintain balanced searching |
| Priority Queue | Prioritize suitable courses |
| Heap Sort | Sort recommendations |
| Graph | Represent course relationships |
| Adjacency Matrix | Store course connections |
| Adjacency List | Store related courses |

---

## 9. Course Data Structure

A course record can contain:

```text
Course ID
Course Name
Category
Level
Duration
Rating
Skills
Prerequisites
Recommendation Score
```

Example:

```text
Course ID: C101
Course Name: Data Structures and Algorithms
Category: Computer Science
Level: Intermediate
Duration: 40 hours
Rating: 4.7
Skills: C++, DSA, Problem Solving
Prerequisites: Basic C++
```

The exact fields can be modified during implementation.

---

## 10. Binary Tree Application

A Binary Tree can organize course categories hierarchically.

Example:

```text
             Computer Science
              /                    Programming          Data
          /                         C++                   DSA
      /   \                 /      Basic  Advanced       Basic  Advanced
```

Tree traversals can then be used to visit and process the stored categories or records.

---

## 11. Binary Search Tree

A BST can be used for course searching and management.

Example:

```text
             50
            /            30    70
         / \    /        20  40  60  80
```

Searching follows:

- Smaller key → move left
- Larger key → move right
- Matching key → course found

Possible operations:

- **Insertion:** Add a course.
- **Searching:** Find a course.
- **Deletion:** Remove a course.
- **Modification:** Find and update a course.

A balanced BST can provide approximately **O(log n)** search, while an unbalanced BST can become **O(n)** in the worst case.

---

## 12. AVL Tree

An AVL Tree is a self-balancing Binary Search Tree.

It can be used when the number of course records becomes large. After insertion or deletion, rotations maintain balance.

Expected complexity:

```text
Search     : O(log n)
Insertion  : O(log n)
Deletion   : O(log n)
```

This helps maintain efficient course searching.

---

## 13. Binary Heap

A Binary Heap can manage recommendation priority.

A course can receive a score based on factors such as:

- Interest match
- Skill match
- Level match
- Rating
- Related-course match

A Max Heap can keep higher-scoring courses at higher priority.

Example:

```text
             Course A
            /                Course B    Course C
        /        Course D Course E
```

---

## 14. Priority Queue

A Priority Queue can return courses according to recommendation priority.

Example:

```text
Course A → 95
Course C → 90
Course B → 84
Course D → 76
```

The most suitable courses can therefore be processed first.

---

## 15. Heap Sort

Heap Sort can arrange recommendations according to their scores.

Example:

```text
Before: 72, 91, 84, 96, 78
After : 96, 91, 84, 78, 72
```

Heap Sort has **O(n log n)** time complexity.

---

## 16. Graph Application

A Graph can represent relationships between courses.

Example:

```text
C Programming
      |
      v
C++ Basics
      |
      v
Data Structures
      |
      v
Algorithms
      |
      v
Competitive Programming
```

Here, courses are vertices and relationships are edges.

This can help identify related courses and possible learning paths.

---

## 17. Adjacency List

An adjacency list stores connected courses.

Example:

```text
C Programming:
    C++ Basics
    Programming Fundamentals

C++ Basics:
    C Programming
    Data Structures

Data Structures:
    C++ Basics
    Algorithms
```

It is useful when the graph is relatively sparse.

---

## 18. Adjacency Matrix

An adjacency matrix can represent direct course connections.

```text
              C++   DSA   Algo
C++            0     1      0
DSA            1     0      1
Algo           0     1      0
```

A `1` represents a connection and `0` represents no direct connection in this example.

---

## 19. Recommendation Logic

A simple recommendation score can combine different matching factors.

Example:

```text
Interest Match     = 40 points
Skill Match        = 30 points
Level Match        = 15 points
Rating Factor      = 10 points
Related Course     =  5 points
--------------------------------
Maximum             100 points
```

The exact scoring formula is a design choice and can be changed during implementation.

Workflow:

```text
Course Records
      |
      v
Calculate Score
      |
      v
Priority Queue / Heap
      |
      v
Sort Results
      |
      v
Top Recommendations
```

---

## 20. Example Recommendation

Student input:

```text
Interest: Programming
Skill: C++
Level: Intermediate
```

Possible result:

| Course | Interest | Skill | Level | Score |
|---|---|---|---|---:|
| DSA with C++ | High | High | Intermediate | 95 |
| Advanced C++ | High | High | Advanced | 88 |
| Python Basics | Medium | Low | Beginner | 65 |
| Web Development | Medium | Low | Intermediate | 60 |

The courses can then be displayed in priority order.

---

## 21. Proposed Algorithm

### Step 1: Input
Take the student's interests, skills, preferred level, and optional preferences.

### Step 2: Search
Search the course collection using a BST or AVL Tree.

### Step 3: Match
Compare the student's requirements with course information.

### Step 4: Score
Calculate a recommendation score.

### Step 5: Prioritize
Insert suitable courses into a Priority Queue or Heap.

### Step 6: Sort
Use Heap Sort or another selected sorting method.

### Step 7: Relationship Check
Use the Graph structure to identify related courses.

### Step 8: Output
Display the highest-ranked courses.

---

## 22. Pseudocode

```text
START

Input student_interest
Input student_skills
Input student_level

Search courses using BST/AVL Tree

For each matching course:
    calculate recommendation_score

    if course is suitable:
        insert course into priority queue

Use heap/priority queue to prioritize courses

Sort required recommendations

Check related courses using graph

Display recommended courses

END
```

---

## 23. Course Search Pseudocode

```text
searchCourse(root, key):

    if root == NULL:
        return NOT_FOUND

    if key == root.key:
        return root

    if key < root.key:
        return searchCourse(root.left, key)

    return searchCourse(root.right, key)
```

This represents the basic search operation of a Binary Search Tree.

---

## 24. Proposed Project Architecture

```text
Online Course Recommendation Engine
|
|-- Course Management
|   |-- Add Course
|   |-- Delete Course
|   |-- Update Course
|   `-- Display Courses
|
|-- Search Module
|   |-- BST Search
|   `-- AVL Search
|
|-- Recommendation Module
|   |-- Interest Matching
|   |-- Skill Matching
|   `-- Score Calculation
|
|-- Ranking Module
|   |-- Heap
|   `-- Priority Queue
|
|-- Sorting Module
|   `-- Heap Sort
|
`-- Relationship Module
    |-- Graph
    |-- Adjacency List
    `-- Adjacency Matrix
```

---

## 25. Complexity Analysis

| Operation | Technique | Expected Complexity |
|---|---|---:|
| BST Search | Binary Search Tree | O(log n) average |
| BST Search | Worst-case unbalanced BST | O(n) |
| AVL Search | AVL Tree | O(log n) |
| AVL Insertion | AVL Tree | O(log n) |
| AVL Deletion | AVL Tree | O(log n) |
| Heap Insertion | Binary Heap | O(log n) |
| Highest priority | Heap | O(1) |
| Heap Sort | Binary Heap | O(n log n) |
| Graph traversal | Adjacency List | O(V + E) |
| Edge lookup | Adjacency Matrix | O(1) |

`n` = number of courses, `V` = graph vertices, and `E` = graph edges.

---

## 26. Why Multiple Data Structures?

Different operations need different structures.

- **Binary Tree:** hierarchical organization.
- **BST:** ordered course searching.
- **AVL Tree:** balanced searching.
- **Heap:** recommendation priority.
- **Priority Queue:** retrieving high-priority courses.
- **Heap Sort:** ordering results.
- **Graph:** course relationships.
- **Adjacency List:** sparse relationships.
- **Adjacency Matrix:** direct connection lookup.

This separation allows the project to demonstrate multiple DSA concepts in one practical application.

---

## 27. Research and Literature Review

### 1. A literature review of implemented recommendation techniques used in Massive Open Online Courses

A systematic review of recommendation systems used in MOOCs. It discusses recommendation techniques, recommendation types, datasets, evaluation methods, and research gaps.

DOI: https://doi.org/10.1016/j.eswa.2021.115926

### 2. Social Collaborative Filtering Approach for Recommending Courses in an E-learning Platform

This work proposes course recommendation using social filtering and collaborative filtering based on learner profiles and social information.

DOI: https://doi.org/10.1016/j.procs.2019.04.166

### 3. MoodleREC: A recommendation system for creating courses using the Moodle e-learning platform

This paper presents a Moodle-based recommendation system that retrieves, ranks, and recommends learning objects.

DOI: https://doi.org/10.1016/j.chb.2019.106168

### 4. ALP-CRS: Enhancing course recommendation in online education through data mining and graph analysis

This work combines association rule mining and graph analysis/link prediction for course recommendation, making it relevant to the project's graph-based approach.

DOI: https://doi.org/10.1016/j.eij.2026.100955

---

## 28. Research-to-Project Connection

The literature provides background on how educational recommendation systems can be designed.

This project uses that problem area but focuses on DSA implementation:

```text
Recommendation Research
        |
        v
Course Recommendation Problem
        |
        v
DSA-Based Design
   /       |       Trees    Heaps    Graphs
  |        |        |
Search   Ranking  Relations
   \       |       /
    \      |      /
     Course Recommendations
```

The research is used for background and understanding; the main academic implementation focuses on DSA concepts.

---

## 29. Input and Output

### Input

```text
Student Interest
Student Skills
Preferred Level
Optional Category
Optional Duration
```

### Output

```text
Course Name
Category
Level
Rating
Recommendation Score
Related Courses
```

Example:

```text
Recommended Course: Data Structures and Algorithms
Category: Computer Science
Level: Intermediate
Rating: 4.7
Score: 95/100

Related:
- C++ Basics
- Algorithms
- Competitive Programming
```

---

## 30. Testing Plan

### Test Case 1 – Course Search
Input: `C101`  
Expected: Course found.

### Test Case 2 – Course Not Found
Input: `C999`  
Expected: Course not found.

### Test Case 3 – Add Course
Add a new course and search for it.  
Expected: Course successfully inserted and searchable.

### Test Case 4 – Delete Course
Delete an existing course and search again.  
Expected: Course is no longer found.

### Test Case 5 – Recommendation
Input: Programming + C++ + Intermediate.  
Expected: Relevant courses are displayed in priority order.

### Test Case 6 – Related Courses
Select a course and check its graph connections.  
Expected: Related courses are displayed.

---

## 31. Current Project Status

The initial stage has focused on:

- Finalizing the project topic.
- Understanding the course recommendation problem.
- Defining objectives.
- Identifying users.
- Studying relevant Trees and Graphs concepts.
- Mapping DSA concepts to project functions.
- Reviewing research related to online course recommendation.
- Preparing the proposed system design.

The Month 1 progress report records approximately **20% progress**, covering problem understanding, DSA study, and planning.

Implementation and testing are planned for later development stages.

---

## 32. Planned Development

### Phase 1 – Requirements
- Finalize course fields.
- Finalize student input.
- Decide recommendation scoring.

### Phase 2 – DSA Implementation
- Course nodes.
- BST.
- AVL Tree.
- Heap.
- Priority Queue.
- Graph.

### Phase 3 – Recommendation
- Interest matching.
- Skill matching.
- Score calculation.
- Recommendation generation.

### Phase 4 – Ranking and Sorting
- Priority Queue.
- Heap.
- Heap Sort.
- Top recommendations.

### Phase 5 – Testing
- Insertion.
- Deletion.
- Searching.
- Modification.
- Ranking.
- Graph relationships.

### Phase 6 – Documentation
- Screenshots.
- Code explanation.
- Test results.
- Complexity analysis.
- Final demonstration.

---

## 33. Future Scope

The project can later be extended with:

1. User accounts and profiles.
2. Real online-course data.
3. Machine-learning recommendations.
4. Collaborative filtering.
5. Rating prediction.
6. Personalized learning paths.
7. Web interface.
8. Database integration.
9. Recommendation history.
10. Course completion tracking.

---

## 34. Limitations

- The initial recommendation logic is DSA-based.
- The prototype may use manually prepared course records.
- Recommendation quality depends on the available course data and scoring rules.
- Advanced machine-learning personalization is outside the main DSA scope.
- Real-time course information is not part of the initial design.

---

## 35. Expected Outcome

The expected outcome is an academic prototype that demonstrates how different DSA concepts can work together in a real-world recommendation problem.

The intended flow is:

```text
Store Courses
     ↓
Search Courses
     ↓
Match Requirements
     ↓
Calculate Relevance
     ↓
Prioritize
     ↓
Sort
     ↓
Recommend
```

The major learning outcome is understanding how theoretical DSA concepts can be applied to a practical software problem.

---

## 36. Conclusion

The **Online Course Recommendation Engine** demonstrates a practical application of Data Structures and Algorithms in education.

Trees can organize and search course data, AVL Trees can maintain balanced searching, Heaps and Priority Queues can manage recommendation priority, Heap Sort can order results, and Graphs can represent relationships between courses.

The project combines these concepts into a single proposed recommendation workflow and provides a foundation for later implementation and testing.

---

## 37. Suggested GitHub Repository Structure

```text
Online-Course-Recommendation-Engine/
|
|-- README.md
|-- PROJECT_REPORT.md
|
|-- src/
|   |-- course.cpp
|   |-- bst.cpp
|   |-- avl.cpp
|   |-- heap.cpp
|   |-- priority_queue.cpp
|   |-- graph.cpp
|   `-- main.cpp
|
|-- data/
|   `-- courses.txt
|
|-- docs/
|   |-- architecture.md
|   |-- algorithms.md
|   `-- research.md
|
`-- screenshots/
```

The filenames above are a suggested structure and should be changed to match the actual implementation files.

---

## 38. Academic Information

| Field | Details |
|---|---|
| Student | Akarsh Singh |
| Branch | B.Tech CSE-A |
| Course | Data Structure and Algorithms - II |
| Course Code | CCSE0301 |
| Faculty | Mr. Shamshad Ali |
| Assignment | Individual Assignment |
| Project | DSA: 25 – Online Course Recommendation Engine |
| SDG | SDG 4 – Quality Education |
| Reporting Stage | Month 1 |

---

## 39. References

1. Khalid, A., Lundqvist, K., & Yates, A. *A literature review of implemented recommendation techniques used in Massive Open Online Courses*. Expert Systems with Applications, 187, 115926.  
   https://doi.org/10.1016/j.eswa.2021.115926

2. Madani, Y., Erritali, M., Bengourram, J., & Sailhan, F. *Social Collaborative Filtering Approach for Recommending Courses in an E-learning Platform*. Procedia Computer Science, 151, 1164–1169.  
   https://doi.org/10.1016/j.procs.2019.04.166

3. De Medio, C., Limongelli, C., Sciarrone, F., & Temperini, M. *MoodleREC: A recommendation system for creating courses using the Moodle e-learning platform*. Computers in Human Behavior, 104, 106168.  
   https://doi.org/10.1016/j.chb.2019.106168

4. Gao, Y., Liu, X., Gao, X., & Zhang, J. *ALP-CRS: Enhancing course recommendation in online education through data mining and graph analysis*. Egyptian Informatics Journal, 34, 100955.  
   https://doi.org/10.1016/j.eij.2026.100955

---

## 40. Author

**Akarsh Singh**  
B.Tech CSE-A  
Noida Institute of Engineering and Technology (NIET)

**Project:** DSA: 25 – Online Course Recommendation Engine

---

> **Documentation note:** This report describes the project's problem, objectives, DSA mapping, proposed architecture, algorithms, research background, testing plan, and development roadmap. Implementation sections are marked as proposed/planned where source code and test evidence have not yet been added.
