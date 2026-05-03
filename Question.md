Design and implement a Spring Boot REST API application for a Library Management System using raw JDBC (JdbcTemplate or NamedParameterJdbcTemplate, not Spring Data JDBC) with a layered architecture (Controller/API → Service → Repository) backed by a MySQL database, where you manage Members, Books, and Borrow Records.

Create APIs to register members with fields such as id (auto-generated), name, email, and phone; add books with id (auto-generated), title, author, availableCopies, and price; and allow members to borrow books by providing memberId, bookId, and quantity, where the system generates a borrowId, records the borrow date, sets an automatic return date (7 days from the borrow date), tracks the actual return date, initializes the fine to 0, validates stock availability, and updates remaining copies accordingly.

If a book is returned after the expected return date, apply a fine of 15 Taka per day for each overdue day.

Implement the repository layer using raw SQL queries (INSERT, SELECT, UPDATE) via JdbcTemplate or NamedParameterJdbcTemplate, and include pagination support in GET endpoints (such as retrieving books or borrow records) using request parameters like page and size with SQL LIMIT and OFFSET.

Ensure proper REST practices by using GET for retrieval, POST for creation, path variables for resource identification, request parameters for pagination and filtering, and request bodies for input payloads, resulting in a complete and efficient library workflow system with manual SQL-based persistence and scalable paginated responses.
