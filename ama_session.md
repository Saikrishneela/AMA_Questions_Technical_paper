
Q1. What is the difference between select_related() and prefetch_related() in Django ORM?

🔹 Answer hint:
select_related() uses SQL joins — efficient for ForeignKey / OneToOne relations (single-valued).
prefetch_related() does separate queries and joins in Python — efficient for ManyToMany / reverse FK relations (multi-valued).

Q2. How do middleware work in Django, and what are some common use cases?

🔹 Answer hint:
Middleware is a lightweight plugin layer that processes requests and responses globally before views or after responses.
Example use cases: authentication, session management, request logging, CORS, and security (CSRF, XSS protection).


Q3. What is the difference between Serializer and ModelSerializer in Django REST Framework?

🔹 Answer hint:
Serializer gives full control — you define fields manually.
ModelSerializer auto-generates fields from a Django model and simplifies CRUD.

Q4. Explain the difference between PUT and PATCH methods in REST.

🔹 Answer hint:
PUT replaces the entire resource; PATCH updates only specific fields.
Example:

PUT: send all fields (even unchanged ones)

PATCH: send only what you want to modify.


Q5. What’s the difference between var, let, and const?

🔹 Answer hint:

var: function-scoped, hoisted

let: block-scoped, reassignable

const: block-scoped, cannot be reassigned

Q6. What is event bubbling and how can you prevent it?

🔹 Answer hint:
Event bubbling = when an event on a child element propagates up to parent elements.
Prevent it using event.stopPropagation() or event.stopImmediatePropagation().

⚡ Asynchronous Programming

Q7. What are Promises, and how do they differ from callbacks?

🔹 Answer hint:
Promises handle async operations and avoid “callback hell.”
They have states: pending → fulfilled → rejected.


Q8. Explain the async/await syntax in JavaScript. How does it simplify asynchronous code?

🔹 Answer hint:
async/await allows writing async code that looks synchronous.
await pauses until a Promise resolves or rejects.
Example:

async function loadData() {
  try {
    const res = await fetch('/api/data');
    const data = await res.json();
    console.log(data);
  } catch (err) {
    console.error(err);
  }
}



