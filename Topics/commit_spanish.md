# 📌 Cómo escribir buenos mensajes de commit en GitHub

## **1️⃣ Estructura de un commit bien escrito**

```plaintext
<tipo>(<área opcional>): <breve descripción>

<Cuerpo opcional explicando más detalles sobre el cambio, si es necesario. 
Puede incluir qué motivó el cambio o cómo afecta al sistema.>

<Pie opcional con referencias a issues o breaking changes>
```

---

## **2️⃣ Tipos de commits más usados en GitHub (Conventional Commits)**

| **Tipo**    | **Propósito** |
|------------|-------------|
| **feat**    | Nueva funcionalidad |
| **fix**     | Corrección de un error |
| **docs**    | Cambios en la documentación |
| **style**   | Cambios de formato (sin afectar el código) |
| **refactor**| Mejoras en el código sin cambiar su comportamiento |
| **test**    | Agregar o modificar pruebas |
| **chore**   | Tareas de mantenimiento (como actualizar dependencias) |
| **perf**    | Mejoras de rendimiento |
| **ci**      | Cambios en la configuración de CI/CD |
| **build**   | Cambios en el sistema de compilación o dependencias |

---

## **3️⃣ Ejemplos prácticos de commits en GitHub**

✅ **Agregar una nueva funcionalidad**  
```plaintext
feat(auth): add JWT authentication middleware

Implemented JWT-based authentication for protected routes. 
Users now need a valid token to access API endpoints.

Closes #45
```

✅ **Corrección de un bug**  
```plaintext
fix(login): resolve incorrect password validation

Fixed a bug where users could log in with an incorrect password 
due to a missing validation step.

Fixes #102
```

✅ **Actualizar documentación**  
```plaintext
docs(readme): add setup instructions for Docker

Updated README with detailed instructions on how to run 
the project inside a Docker container.
```

✅ **Refactorización de código**  
```plaintext
refactor(database): optimize queries for better performance

Rewrote SQL queries to reduce response time by 30%. 
No changes to existing functionality.
```

✅ **Actualizar dependencias sin afectar el código**  
```plaintext
chore(deps): update eslint to version 8.2.1
```

---

## **4️⃣ Buenas prácticas en GitHub**

🔹 Usa el **imperativo** ("Add feature" en vez de "Added feature").  
🔹 Mantén la primera línea en **50 caracteres o menos**.  
🔹 Si necesitas más detalles, agrégalos en el cuerpo del commit (máx. **72 caracteres por línea**).  
🔹 **Relaciona issues** con `Fixes #ID` o `Closes #ID` para que GitHub cierre el issue automáticamente.  
🔹 Evita mensajes genéricos como `update` o `fix bug`, sé más descriptivo.  

---

## **📌 Cómo hacer un buen commit en GitHub desde la terminal**

```sh
git commit -m "feat(cart): add discount functionality for bulk orders"
```

O si necesitas más detalles:

```sh
git commit -m "feat(cart): add discount functionality for bulk orders" -m "Customers now receive a 10% discount if they purchase 10+ items."
```

Si ya hiciste un commit pero quieres corregirlo:

```sh
git commit --amend
```