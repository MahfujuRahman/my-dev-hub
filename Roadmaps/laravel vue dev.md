# Full-Stack Developer + Competitive Programming + DevOps Roadmap

**Duration:** ~6 months  
**Daily Commitment:** 3 hours/day  
**Learning Style:** One subject at a time, then mix  
**Resources:** All free  

---

## Phase 1: Programming Fundamentals & Git (Weeks 1–3)

### Goal:  
Build strong PHP fundamentals, OOP, and Git version control knowledge.

### Week 1: PHP Basics  
**Topics:** Syntax, variables, data types, operators, control flow, functions  
**Daily Tasks:**  
- Day 1: PHP setup, echo/print, variables, data types  
- Day 2: Operators, type juggling, constants  
- Day 3: Control flow - if/else, switch  
- Day 4: Loops - for, while, foreach  
- Day 5: Functions basics, parameters, return values  
- Day 6: Arrays (indexed, associative)  
- Day 7: Mini project: Simple calculator or form handler

**Resources:**  
- [PHP Manual - Basics](https://www.php.net/manual/en/langref.php)  
- [W3Schools PHP Tutorial](https://www.w3schools.com/php/)  
- [PHP Exercises](https://www.w3resource.com/php-exercises/)

---

### Week 2: PHP OOP Fundamentals  
**Topics:** Classes, objects, properties, methods, inheritance, interfaces, traits  
**Daily Tasks:**  
- Day 1: Class and object basics  
- Day 2: Properties & methods  
- Day 3: Constructors and destructors  
- Day 4: Inheritance basics  
- Day 5: Interfaces and traits  
- Day 6: Visibility (public, private, protected)  
- Day 7: Mini project: Simple bank account class system

**Resources:**  
- [PHP OOP Manual](https://www.php.net/manual/en/language.oop5.php)  
- [Laracasts OOP Bootcamp (free)](https://laracasts.com/series/object-oriented-bootcamp-in-php)  

---

### Week 3: Git Version Control  
**Topics:** Installation, basic commands, branches, merging, GitHub workflows  
**Daily Tasks:**  
- Day 1: Git installation, init, status, add, commit  
- Day 2: Viewing history, diff, log  
- Day 3: Branch creation, switching branches  
- Day 4: Merging branches, resolving conflicts  
- Day 5: Remote repos: clone, push, pull  
- Day 6: Pull requests and GitHub flow basics  
- Day 7: Practice: Create repo + feature branch workflow

**Resources:**  
- [Pro Git Book](https://git-scm.com/book/en/v2)  
- [FreeCodeCamp Git Tutorial](https://www.freecodecamp.org/news/git-and-github-for-beginners/)  

---

## Phase 2: Backend Development with Laravel (Weeks 4–8)

### Goal:  
Master Laravel core — routing, controllers, models, migrations, validation, authentication, API, testing.

### Week 4: Laravel Basics Setup & Routing  
- Day 1: Install Laravel, environment setup (Homestead/Valet/XAMPP)  
- Day 2: Basic routes, route parameters  
- Day 3: Controllers & route grouping  
- Day 4: Blade templating engine basics  
- Day 5: Passing data to views, layouts & components  
- Day 6: Middleware basics  
- Day 7: Mini project: Simple blog homepage + post routes

### Week 5: Eloquent ORM & Migrations  
- Day 1: Database configuration  
- Day 2: Migrations and schema building  
- Day 3: Eloquent models basics  
- Day 4: Query builder and relationships (one-to-one, one-to-many)  
- Day 5: Eloquent advanced queries (where, orderBy, eager loading)  
- Day 6: Database seeding & factories  
- Day 7: Mini project: Blog post CRUD with database

### Week 6: Validation & Authentication  
- Day 1: Request validation basics  
- Day 2: Custom validation rules  
- Day 3: Form requests  
- Day 4: Authentication scaffolding with Laravel Breeze  
- Day 5: User registration & login  
- Day 6: Password reset & email verification  
- Day 7: Mini project: User registration and login system

### Week 7: API Development  
- Day 1: API routes vs web routes  
- Day 2: Resource controllers & API resources  
- Day 3: Authentication for APIs (Sanctum)  
- Day 4: API rate limiting  
- Day 5: Testing APIs with Postman  
- Day 6: API error handling  
- Day 7: Mini project: REST API for posts with auth

### Week 8: Testing & Debugging  
- Day 1: Introduction to PHPUnit & Laravel test structure  
- Day 2: Writing unit tests for models  
- Day 3: Writing feature tests for controllers  
- Day 4: Testing validation & authentication  
- Day 5: Debugging with Laravel Telescope & dd()  
- Day 6: Error logging setup  
- Day 7: Practice writing tests for previous mini projects

**Resources:**  
- [Laravel Official Docs](https://laravel.com/docs/10.x)  
- [Laravel From Scratch (YouTube)](https://www.youtube.com/playlist?list=PLpzy7FIRqpGD0kxI48v8QEVVZd744Phi4)  
- [Laracasts Laravel Testing (free series)](https://laracasts.com/series/laravel-testing-decoded)  

---

## Phase 3: Frontend Development with Vue 3 (Weeks 9–12)

### Goal:  
Learn Vue 3 fundamentals, components, reactivity, routing, state management, API integration.

### Week 9: Vue Setup & Basic Components  
- Day 1: Vue 3 installation with Vite  
- Day 2: Template syntax, interpolation, directives  
- Day 3: Components creation & registration  
- Day 4: Props and event handling  
- Day 5: Conditional rendering and loops  
- Day 6: Slots basics  
- Day 7: Mini project: To-do list with basic components

### Week 10: Reactivity System  
- Day 1: reactive() and ref() basics  
- Day 2: Computed properties  
- Day 3: Watchers and lifecycle hooks  
- Day 4: Handling user input and forms  
- Day 5: Handling events & methods  
- Day 6: Dynamic & conditional components  
- Day 7: Mini project: Form with validation

### Week 11: Vue Router & SPA Routing  
- Day 1: Installing and configuring Vue Router  
- Day 2: Defining routes and nested routes  
- Day 3: Navigation guards  
- Day 4: Route params and query  
- Day 5: Lazy loading routes  
- Day 6: Programmatic navigation  
- Day 7: Mini project: Multi-page SPA

### Week 12: State Management with Pinia & API Calls  
- Day 1: Pinia store basics  
- Day 2: State, getters, and actions  
- Day 3: Using store in components  
- Day 4: API calls with Axios basics  
- Day 5: Handling API errors  
- Day 6: Combining Pinia and API calls  
- Day 7: Mini project: Todo app with remote API & Pinia

**Resources:**  
- [Vue 3 Official Docs](https://vuejs.org/guide/introduction.html)  
- [Vue Mastery Intro to Vue 3 (free)](https://www.vuemastery.com/courses/intro-to-vue-3/intro-to-vue3)  
- [Pinia Docs](https://pinia.vuejs.org/)  
- [Axios GitHub](https://github.com/axios/axios)  

---

## Phase 4: Database & Advanced Backend (Weeks 13–14)

### Goal:  
Master advanced SQL and advanced Laravel features like queues, notifications, caching.

### Week 13: Advanced SQL  
- Day 1: Complex SELECT queries, subqueries  
- Day 2: JOIN types and usage  
- Day 3: GROUP BY, HAVING, aggregate functions  
- Day 4: Transactions and ACID principles  
- Day 5: Indexing and optimization basics  
- Day 6: Backup and restore commands  
- Day 7: Practice SQL problems

### Week 14: Advanced Laravel  
- Day 1: Laravel queues and jobs basics  
- Day 2: Creating and dispatching jobs  
- Day 3: Notifications (mail, database, broadcast)  
- Day 4: Cache drivers and usage  
- Day 5: Task scheduling  
- Day 6: Performance tips and config caching  
- Day 7: Mini project: Background email sending

**Resources:**  
- [SQLBolt](https://sqlbolt.com/)  
- [Laravel Docs Advanced](https://laravel.com/docs/10.x/queues)  

---

## Phase 5: Competitive Programming (Ongoing from Week 15)

### Goal:  
Build problem-solving skills with algorithms and data structures.

### Weeks 15+ (Start easy, increase difficulty gradually)  
- Focus on one algorithm/data structure weekly: sorting, recursion, arrays, stacks, trees, graphs, DP  
- Solve at least 5-10 problems daily on coding platforms  
- Study solutions and learn optimizations  

**Platforms:**  
- [LeetCode](https://leetcode.com/)  
- [Codeforces](https://codeforces.com/)  
- [AtCoder](https://atcoder.jp/)  
- [CP Algorithms](https://cp-algorithms.com/)  

---

## Phase 6: DevOps & Deployment (Weeks 20–22)

### Goal:  
Learn Linux, Docker, VPS deployment, CI/CD automation.

### Week 20: Linux & Shell Basics  
- Day 1-3: Linux terminal commands (navigation, file management)  
- Day 4-5: Permissions, users, processes  
- Day 6-7: Basic bash scripting  

### Week 21: Docker  
- Day 1-2: Docker installation and concepts  
- Day 3-4: Dockerfiles and images  
- Day 5-6: Docker Compose  
- Day 7: Containerizing Laravel + Vue apps

### Week 22: CI/CD & VPS Deployment  
- Day 1-2: GitHub Actions introduction  
- Day 3-4: Automate tests and builds  
- Day 5-6: Deployment scripts via SSH to VPS  
- Day 7: Full CI/CD pipeline project

**Resources:**  
- [Linux Journey](https://linuxjourney.com/)  
- [Docker Docs](https://docs.docker.com/get-started/)  
- [GitHub Actions Docs](https://docs.github.com/en/actions)  

---

# After 6 Months: Continuous Learning & Project Building

- Combine backend + frontend skills to build full-stack projects  
- Regularly practice competitive programming  
- Improve DevOps skills: Monitoring, Logging, Security  
- Explore cloud services (AWS, DigitalOcean, etc.)  
- Contribute to open source and build portfolio  

---

# Would you like me to generate this as a downloadable `.md` file for you now?  
Just say “Yes,” and I’ll prepare it!  
