## Professional Self-Assessment

My time in the Computer Science program here at SNHU has been about closing the gap between the theory and production-level engineering work.
The Travlr Getaways capstone projects pushed me to pull together everything I've learned, requiring me to architect connecting a native C++ desktop client to a Node.js and MongoDB backend.
<br>
This ePortfolio tracks that growth.
The artifacts presented here demonstrate my ability to deliver secure, industry-ready software across three primary domains.
<br><br>
<h1>Software Design and Engineering</h1>
<br>
My primary enhancement focused on completely overhauling the application's administrative frontend architecture. 
I replaced the original web-based dashboard with a compiled, native C++ application built on the Qt framework.
This shift meant handling memory management, object-oriented design, and asynchronous network requests so the UI wouldn't freeze up while waiting for the API.
By doing this, I proved my ability to pick up an entirely new framework and deliver a clean, intuitive desktop interface without sacrificing user experience.
<br><br>
<h1>Algorithms and Data Structures</h1>
<br>
To make the application run more efficiently on the client side, I built a custom binary search tree in C++ to handle the trip data filtering.
Instead of relying on a standard linear array search, the BST drops the time complexity for price filtering from a linear O(n) to O(log n).
This enhancement shows my ability to evaluate performance trade-offs and implement the exact data structures to speed up execution at the local level.
<br><br>
<h1>Databases and Security</h1>
<br>
I locked down the Express and MongoDB backend by implementing JSON Web Tokens (JWT) and a local Passport.js strategy. 
I wrote custom Mongoose schemas that use cryptographic hashing and salting to store user credentials safely.
From there, I set up custom middleware to protect the REST API endpoints, ensuring that nobody can execute POST or PUT requests to modify the database without passing a valid bearer token.
I then verified the security flow and token generation using Postman.
<br><br>
<h1>Professional Practices and Version Control</h1>
<br>
Throughout the development lifecycle, I maintained strict version control using Git, relying on branching strategies to safely isolate, build, and merge new modules before pushing them up to my repository. 
Documenting code, tracking changes, and clearly communicating technical concepts have become standard parts of my workflow.
<br>
The artifact and enhancements in this ePortfolio maps out the whole process. 
They represent my progression into a developer who can architect, secure, and optimize a system from the database up to the desktop UI.

---

## Code Review
//Walk the reader through the code review and link it here:

* **Watch the Code Review:** [Link the code review here](#)

---

## Original Artifact
Below is the baseline project I used as an artifact for all my categories:

* **Software Design & Engineering**
* **Algorithms & Data Structures**
* **Databases**

[Download / View original code](#)

---

## Enhanced Artifact
Below are the final, refactored artifacts demonstrating enhancements in architecture, increased efficiency through algorithms, and database security improvements:

| Enhancement Category | Repository | Key Improvements |
| :--- | :--- | :--- |
| **Software Design & Engineering** | [View enhancement code](#) | //explain key improvement here
| **Algorithms & Data Structures** | [View enhancement code](#) | //explain key improvement here
| **Databases** | [View enhancement code](#) | //explain key improvement here

---

## Narratives
These narratives explain the enhancement process, challenges encountered, and course outcomes met for each milestone:

### 1. Software Design & Engineering Narrative
* **Summary:** *//include the narrative text here directly*

### 2. Algorithms & Data Structures Narrative
* **Summary:** *//include the narrative text here directly*

### 3. Database Narrative
* **Summary:** *//include the narrative text here directly*
