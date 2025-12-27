# Design Notes



---

## 1. Why use ArrayList instead of Array?

- Array has fixed size and becomes inconvenient for add/remove operations.
- ArrayList grows dynamically and is easier for CRUD-based applications.
- Built-in methods (`add`, `remove`, `get`) simplify student/course management.

Therefore, ArrayList is used in repositories for storing Students, Courses and Enrollments.

---

## 2. Where static members are used and why?

- `IdGenerator` class uses **static counters** to generate unique IDs.
- Static ensures ID increments globally and is not tied to individual objects.
- This helps maintain unique student/course/enrollment IDs throughout the system.

---

## 3. Use of Inheritance

Class `Person` is the base class with common fields:
`id, firstName, lastName, email`.

`Student` extends `Person` and adds:
`batch, active`.

Benefits:
- Code reuse – no repeated fields.
- Polymorphism opportunity – `toString()` is overridden.
- Readable structure as per assignment requirement.

---

## 4. Encapsulation & Access Modifiers

- All fields across entities are **private**.
- Public **getters/setters** control access.
- Prevents direct field modification and improves safety.

---

## 5. Service Layer Responsibility

- `StudentService`, `CourseService`, `EnrollmentService`
- Responsible for business logic only.
- UI does not access repositories directly.

This maintains separation of concerns and cleaner architecture.

---

## 6. Exception Handling

- `EntityNotFoundException` handles missing IDs gracefully.
- Shows meaningful error messages instead of crashing.

---

## 7. Overall Architecture

entity → repository → service → ui(Main)

Flow:
User Input → Main(UI) → Service → Repository → Data stored/updated

