Here’s a **very detailed 8-week plan** where each week has **3 separate lessons**.
It’s paced for **kids (10–15)** and follows **Node + Express + lowdb → SQLite**.
Each lesson is short, practical and ends with a mini hands-on activity.

---

# 🗓️ Backend Basics — 8 Weeks × 3 Lessons

---

## **Week 1 — Backend & Node.js Foundations**

**Lesson 1 — Internet & Backend Basics**

* How a website works: browser → request → server → response.
* Frontend vs backend explained with pictures.
* JSON: what it looks like and why it’s used.
* Demo: open Network tab, inspect a request.

**Lesson 2 — Setting Up Node**

* Install Node + VS Code.
* Running first JS file in terminal (`node index.js`).
* Using `console.log()` to print.
* Activity: print your name, favorite color, and return it as an object.

**Lesson 3 — npm & First Package**

* What is `npm init` and `package.json`.
* Installing a package (e.g., `colors` or `chalk`) to color console output.
* Activity: create `hello.js` that prints colorful greeting.

---

## **Week 2 — Express Intro**

**Lesson 1 — First Express Server**

* Install express: `npm install express`.
* `const express = require('express')` and `app.listen()`.
* Return simple text for GET `/`.
* Activity: run server on `localhost:3000`.

**Lesson 2 — Routes & JSON Response**

* Return JSON with `res.json()`.
* Add `/about` and `/hello` routes.
* Activity: create your own info API (name, hobby, school).

**Lesson 3 — Nodemon & Thunder Client**

* Install nodemon for auto restart.
* Thunder Client to test endpoints easily.
* Activity: create `/greet` route and test in Thunder Client with different names using query `?name=Ali`.

---

## **Week 3 — Requests & Data**

**Lesson 1 — Query & Params**

* `req.query` vs `req.params`.
* Activity: `/hello/:name` route that returns `Hello, name!`.

**Lesson 2 — POST & Body**

* `app.use(express.json())`.
* Activity: create POST `/feedback` to accept JSON `{ message: "..." }`.

**Lesson 3 — Simple Todos API (Memory)**

* Make in-memory array: `let todos = []`.
* GET `/todos`, POST `/todos`.
* Activity: add a todo, view list.

---

## **Week 4 — Persist with lowdb**

**Lesson 1 — What is Database vs Memory**

* Why memory resets on restart.
* Introduce JSON file saving.

**Lesson 2 — Setup lowdb**

* Install `lowdb`, initialize db, default data.
* Activity: convert todos to save/load from `db.json`.

**Lesson 3 — CRUD Complete**

* Add DELETE `/todos/:id`.
* Add PUT/PATCH to mark complete.
* Activity: test all endpoints with Thunder Client.

---

## **Week 5 — SQLite**

**Lesson 1 — Database Concept**

* What is a table, row, column.
* Why SQL is used.
* Install SQLite extension for VS Code.

**Lesson 2 — SQLite in Node**

* Install `better-sqlite3`.
* Create `todos` table.
* Insert & select from code.

**Lesson 3 — Switch API to SQLite**

* Replace lowdb with SQLite in `GET/POST`.
* Activity: show todos survive restart & manual DB inspection.

---

## **Week 6 — Errors & Status Codes**

**Lesson 1 — Status Codes**

* 200 OK, 201 Created, 400 Bad Request, 404 Not Found.
* Activity: change response codes in your API.

**Lesson 2 — Input Validation**

* Check if title exists before insert.
* Activity: return 400 if empty todo text.

**Lesson 3 — Error Handling Middleware**

* `app.use((err, req, res, next) => { … })`.
* Activity: create one global error handler and test.

---

## **Week 7 — Connecting to Frontend**

**Lesson 1 — Fetch API**

* How browser uses `fetch` to talk to server.
* Activity: simple HTML + `<script>` to call `/todos` and show list.

**Lesson 2 — POST from Browser**

* Form submission with `fetch`.
* Activity: add new todo via HTML form → appears in list.

**Lesson 3 — Styling & UX**

* Add CSS to style list and buttons.
* Activity: delete todo by clicking a button.

---

## **Week 8 — Final Project**

**Lesson 1 — Plan Your API**

* Decide project: Book Library, Shop, Notes.
* Define fields and routes (CRUD).

**Lesson 2 — Build API & Connect Frontend**

* Create DB table, endpoints, and simple HTML page.

**Lesson 3 — Presentation & Demo**

* Kids present project (show requests + webpage).
* Celebrate achievements 🎉

---

### 💡 Teaching tips

* Keep lessons 30–40 min explanation + 20–30 min practice.
* Draw diagrams for request/response often.
* Let them pair code.
* Give simple JSON data ideas (books, pets, tasks).
* Keep “wow” moments (reload page, see data saved).

---

Would you like me to generate **homework & quiz suggestions** for each lesson (so you can assign quick checks after every class)?
