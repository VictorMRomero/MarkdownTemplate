# 📌 How to Write Good Commit Messages on GitHub

## **1️⃣ Structure of a Well-Written Commit**

```plaintext
<type>(<optional scope>): <short description>

<Optional body explaining more details about the change if necessary.
It can include what motivated the change or how it affects the system.>

<Optional footer with references to issues or breaking changes>
```

---

## **2️⃣ Common Commit Types on GitHub (Conventional Commits)**

| **Type**    | **Purpose** |
|------------|-------------|
| **feat**    | New feature |
| **fix**     | Bug fix |
| **docs**    | Documentation changes |
| **style**   | Formatting changes (no code logic changes) |
| **refactor**| Code improvements without changing functionality |
| **test**    | Adding or modifying tests |
| **chore**   | Maintenance tasks (e.g., updating dependencies) |
| **perf**    | Performance improvements |
| **ci**      | CI/CD configuration changes |
| **build**   | Changes in the build system or dependencies |

---

## **3️⃣ Practical Examples of Commits on GitHub**

✅ **Adding a new feature**  
```plaintext
feat(auth): add JWT authentication middleware

Implemented JWT-based authentication for protected routes. 
Users now need a valid token to access API endpoints.

Closes #45
```

✅ **Fixing a bug**  
```plaintext
fix(login): resolve incorrect password validation

Fixed a bug where users could log in with an incorrect password 
due to a missing validation step.

Fixes #102
```

✅ **Updating documentation**  
```plaintext
docs(readme): add setup instructions for Docker

Updated README with detailed instructions on how to run 
the project inside a Docker container.
```

✅ **Refactoring code**  
```plaintext
refactor(database): optimize queries for better performance

Rewrote SQL queries to reduce response time by 30%. 
No changes to existing functionality.
```

✅ **Updating dependencies without affecting code**  
```plaintext
chore(deps): update eslint to version 8.2.1
```

---

## **4️⃣ Best Practices on GitHub**

🔹 Use the **imperative mood** ("Add feature" instead of "Added feature").  
🔹 Keep the first line **under 50 characters**.  
🔹 If more details are needed, include them in the body (max **72 characters per line**).  
🔹 **Reference issues** with `Fixes #ID` or `Closes #ID` to automatically close the issue on GitHub.  
🔹 Avoid generic messages like `update` or `fix bug`, be more descriptive.  

---

## **📌 How to Make a Good Commit on GitHub from the Terminal**

```sh
git commit -m "feat(cart): add discount functionality for bulk orders"
```

Or if more details are needed:

```sh
git commit -m "feat(cart): add discount functionality for bulk orders" -m "Customers now receive a 10% discount if they purchase 10+ items."
```

If you already made a commit but want to amend it:

```sh
git commit --amend
```