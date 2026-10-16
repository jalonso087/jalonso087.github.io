## Professional Self-Assessment

My time in the Computer Science program here at SNHU has been about closing the gap between the theory and production-level engineering work.
The Travlr Getaways capstone projects pushed me to pull together everything I've learned, requiring me to architect connecting a native C++ desktop client to a Node.js and MongoDB backend.
<br>
This ePortfolio tracks that growth.
The artifacts presented here demonstrate my ability to deliver secure, industry-ready software across three primary domains.
<br><br>
<h3>Software Design and Engineering</h3>
<br>
My primary enhancement focused on completely overhauling the application's administrative frontend architecture. 
I replaced the original web-based dashboard with a compiled, native C++ application built on the Qt framework.
This shift meant handling memory management, object-oriented design, and asynchronous network requests so the UI wouldn't freeze up while waiting for the API.
By doing this, I proved my ability to pick up an entirely new framework and deliver a clean, intuitive desktop interface without sacrificing user experience.
<br><br>
<h3>Algorithms and Data Structures</h3>
<br>
To make the application run more efficiently on the client side, I built a custom binary search tree in C++ to handle the trip data filtering.
Instead of relying on a standard linear array search, the BST drops the time complexity for price filtering from a linear O(n) to O(log n).
This enhancement shows my ability to evaluate performance trade-offs and implement the exact data structures to speed up execution at the local level.
<br><br>
<h3>Databases and Security</h3>
<br>
I locked down the Express and MongoDB backend by implementing JSON Web Tokens (JWT) and a local Passport.js strategy. 
I wrote custom Mongoose schemas that use cryptographic hashing and salting to store user credentials safely.
From there, I set up custom middleware to protect the REST API endpoints, ensuring that nobody can execute POST or PUT requests to modify the database without passing a valid bearer token.
I then verified the security flow and token generation using Postman.
<br><br>
<h3>Professional Practices and Version Control</h3>
<br>
Throughout the development lifecycle, I maintained strict version control using Git, relying on branching strategies to safely isolate, build, and merge new modules before pushing them up to my repository. 
Documenting code, tracking changes, and clearly communicating technical concepts have become standard parts of my workflow.
<br>
The artifact and enhancements in this ePortfolio maps out the whole process. 
They represent my progression into a developer who can architect, secure, and optimize a system from the database up to the desktop UI.

---

## Code Review
The video below is my informal code review of the original Travlr Getaways application, recorded before I started any of my enhancements.
The baseline app was built using a standard MVC structure and a MongoDB database to store the trip data.
While it successfully used REST API endpoints, my analysis highlighted a few major areas that needed improvement.
The web-based UI wasn't as efficient as a compiled desktop app, the basic linear data search would struggle with larger datasets, and the backend lacked proper security.
In this walkthrough, I review the existing JavaScript codebase and explain my plan to fix these issues by migration the frontend to a native C++ Qt environment, building a binary search tree for faster data filtering, and locking down the backend with JSON Web Tokens.

* **Watch the Code Review:** [CS499 Capstone Code Review](https://youtu.be/mx2D3JxvAOY)

---

## Original Artifact
Below is the baseline project I used as an artifact for all my categories:

* **Software Design & Engineering**
* **Algorithms & Data Structures**
* **Databases**

[Download / View original code](https://github.com/jalonso087/cs465-fullstack/tree/module7)

---

## Enhanced Artifact
Below are the final, refactored artifacts demonstrating enhancements in architecture, increased efficiency through algorithms, and database security improvements:

| Enhancement Category | Repository | Key Improvements |
| :--- | :--- | :--- |
| **Software Design & Engineering** | [View enhancement code](https://github.com/jalonso087/cs499-capstone/tree/admin-desktop-app) | Modernized the frontend architecture by migrating from a standard web-based dashboard to a compiled, native C++ Qt desktop application, resulting in a more efficient and responsive user interface
| **Algorithms & Data Structures** | [View enhancement code](https://github.com/jalonso087/cs499-capstone/tree/price-filtering-bst) | The custom binary search tree I developed within the C++ client to handle trip data optimizes the time complexity of price-filtering operations from a standard linear search O(n) down to O(log n)
| **Databases** | [View enhancement code](https://github.com/jalonso087/cs499-capstone/tree/impl-jwt-enh3) | The MongoDB backend was secured by implementing a custom Mongoose user schema with cryptographic hashing, paired with JSON Web Token middleware that intercepts requests and rejects unauthorized attempts to modify database records

---

## Narratives
These narratives explain the enhancement process, challenges encountered, and course outcomes met for each milestone:

### 1. Software Design & Engineering Narrative
* **Summary:** The enhancement completed as my “Enhancement 1” was to develop a C++ native desktop application that handles the administrative functionality of the Angular page developed on the MEAN stack.
<br><br>
The artifact chosen was the Travlr Getaways project developed on the MEAN stack. This web page utilizes MongoDB as a database to contain trip data for potential traveling trips, Express used as the backend for routing, Angular was used in developing the user-facing admin portion of the website, while Node.js for server-side Javascript execution. This project was created as part of CS465, which I took in my last semester.
<br><br>
I chose this item as my artifact specifically because of its complexity. In essentially pruning a piece of the MEAN stack, and replacing that with a native C++ desktop application, I am able to showcase my understanding of the project to such a degree that I can replace the entirety of the work being done through Angular for my own C++ interpretation – utilizing Qt as my UI framework. This improves the artifact in that the admin functionality is partially running locally which increases the speed at which it loads and functions – which will come in handy as the trip database expands.
<br><br>
I met the course outcome I planned to accomplish through this enhancement by using a best in class GUI framework (Qt) chosen after thorough research into ImGui and command line interface and which one of the three can meet the requirements for this assignment. I was able to replace a portion of the MEAN stack functionality by instead utilizing a C++ native desktop application to handle administrative functionality for the project. In using QtWidgets to build out my UI, I believe I showcase my ability to “…use well-founded and innovative techniques, skills, and tools in computing practices for the purpose of implementing computer solutions that deliver value and accomplish industry-specific goals.”
<br><br>
One of the major challenges I face in enhancing this artifact was the “edit trip” functionality. Originally, I had built all submissions for the trips around a POST method – and I only realized it after editing a couple of trips during unit testing and noticing the edited trip was being added as a new trip, which would be absolutely unacceptable in a PROD environment. So I had to instead use a simple if/else statement to determine whether to send a POST (for new trips) or a PUT method (for editing trips). Once I did that, my unit testing came back as a full pass.

### 2. Algorithms & Data Structures Narrative
* **Summary:** Ultimately, the enhancement I chose as my enhancement two was to build upon the C++ native desktop application I built on enhancement one. Specifically, I built upon this application by adding price filtering functionality and a binary search tree for traversal through the price.
<br><br>
Identical to the first artifact, the artifact chosen here was the Travlr Getaways project developed on the MEAN stack. Beyond that, I suppose it is not out of line to say the artifact I worked was not only the MEAN stack developed portion of this project, but it was mostly the C++ native desktop application I developed as part of enhancement one.
<br><br>
I chose this item as my artifact because it was intuitive. Adding price filtering functionality to a native C++ desktop application that I developed to handle the administrative functionalities of this Travlr Getaways project felt right. By iterating on the previous enhancement made, it helps provide and showcase the level of experience I am looking to present here, while also providing a natural uptick in valuable functionality to the application. One problem for price filtering is that iterating through an array of trips for filtering would be a complexity of O(n), which does not scale well as the amount of trips increases. My solution here was to implement a binary search tree for O(log n) traversal.
<br><br>
The course outcome I chose for this enhancement was as follows:
  <strong>Design and evaluate computing solutions that solve a given problem using algorithmic principles and computer science practices and standards appropriate to its solution while managing the trade-offs involved in the design choices</strong>
<br><br>
I met the course outcome I had hoped to meet because I utilized a binary search tree to solve price filtering at an O(log n) complexity. By using a binary search tree, I am solving the problem of traversal that would result in a completely unscalable and barely functional solution had I not implemented an algorithmic solution to this.
<br><br>
One of the major challenges I faced in enhancing the artifact for enhancement two was thinking I had eliminated unnecessary code by removing the “Test API Connection” button, but not removing the connect function in my constructor, leading to (either) a segmentation fault or CMake build error – I can’t remember which of the two was caused by this. This taught me to double and triple check for any instances of an object I am removing by searching through the rest of the code. That will ensure that any unnoticed sections of code that utilize the same object will be pointed out and can be dealt with appropriately.


### 3. Database Narrative
* **Summary:** The enhancement chosen for my enhancement 3 was to build upon the entire stack by implementing JSON Web Tokens to improve the security into the database. I also defined a stricter Mongoose schema to ensure the data getting into the database is safe.
<br><br>
Like the two enhancements before this, the artifact I chose to work on here was the Travlr Getaways project developed on the MEAN stack. This artifact was chosen simply because it was an ideal candidate. The stack already utilized MongoDB and multiple endpoints, which made this an obvious choice for my enhancement on implementing an improvement centered around databases. The specific components of the artifact that showcase my skills and abilities in software development, is the ability to implement JWT authentication and define a stricter Mongoose schema validation, particularly upon an already existing partial implementation and defining that was handled prior to this course. The artifact was improved by handling a hashed authentication, at the lower, endpoint, level, and defining a stricter Mongoose schema has made the program more resilient to any potential threat actors.
<br><br>
The course outcome I chose was:
<strong>Develop a security mindset that anticipates adversarial exploits in software architecture and designs to expose potential vulnerabilities , mitigate design flaws, and ensure privacy and enhanced security of data and resources.</strong>
<br><br>
I met this course outcome by going into the development for this enhancement with that security mindset mentioned in the outcome. Specifically, by assuming malicious intent when building out the Mongoose schema and ensuring all POST and PUT HTTP requests passthrough the JWT authentication method.
<br><br>
One of the challenges I faced while working on the enhancement for this artifact was that JWT had partially been added but was not complete. So, I had to ensure that my implementation did not clash with the pieces of what was already in the program, but instead repurposed what was there into something better.



