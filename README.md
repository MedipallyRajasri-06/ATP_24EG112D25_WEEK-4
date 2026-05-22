# Week 4 Assignments
## Project Structure

| Directory/File | Description |
| :--- | :--- |
| `project1/` | Basic HTML structure, paragraphs, formatting (bold/italic), and unordered lists. |
| `project2/` | Profile page implementation using images, ordered lists, and links. |
| `assets/` | Static assets like images used in the projects. |

## Detailed Breakdown

### 1. Basic HTML Elements (`project1`)
- **Structure**: Implementation of standard HTML5 boilerplate.
- **Formatting**: Use of `<b>` and `<i>` tags for text styling.
- **Lists**: Practice with unordered lists (`<ul>`) to display items.
- **Links**: Basic navigation using anchor (`<a>`) tags.

### 2. Pochi the Cat Profile (`project2`)
- **Headers**: Structured content using `<h1>` and `<h3>` tags.
- **Images**: Embedding images with the `<img>` tag and using alignment attributes.
- **Ordered Lists**: Displaying profile details using `<ol>` tags.
- **Horizontal Rules**: Separating content sections with `<hr>`.
- **Links**: Integration of external links to animal shelters and societies.

## How to View

1. Open the desired project folder (`project1` or `project2`).
2. Open the `index.html` file in any modern web browser to view the rendered page.
   Week 4: Security, Authentication & Content Management

Authentication: Implementing User Registration and Login with password hashing.
Security: Using JSON Web Tokens (JWT) and HTTP-Only Cookies for session management.
Authorization: Role-Based Access Control (RBAC) using custom middleware.
Complex Data Modeling: Relational data handling in MongoDB using Mongoose References and Population.
|middlewares/VerifyToken.js- JWT validation and Role-based authorization logic APIs/CommonAPI.js-Public routes for registration, login, and logout. APIs/AuthorAPI.js- Protected routes for article management (CRUD). models/ArticleModel.js-Schema for articles with nested comments and user references. server.js-Main entry point with advanced global error handling.

Features & Implementation

Security & Authentication
Bcryptjs: Used for salting and hashing passwords (12 rounds) before storage.
JWT (JSON Web Tokens): Signed tokens contain user identity and roles, enabling stateless authentication.
Cookies: Tokens are sent via httpOnly cookies to mitigate XSS (Cross-Site Scripting) risks.
Authorization (RBAC)
A custom verifyToken middleware ensures that only authenticated users with the correct role (e.g., AUTHOR, USER) can access specific endpoints.
Ownership verification: Ensuring authors can only modify or delete their own articles.
Article Management System
Schemas: Articles include nested commentSchema and timestamps for tracking creation/updates.
Soft Delete: Implementation of isArticleActive flag to allow data recovery and audit trails.
CRUD Logic: Authors can publish, edit, and toggle the status of their articles.
