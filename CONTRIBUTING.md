# Guía de Contribución - `jfinfotest/proyecto-final-bases-datos`

¡Hola! Nos alegra mucho que quieras contribuir a este proyecto. Tu ayuda es fundamental para mantener la calidad y el éxito de nuestro sistema de bases de datos.

Esta guía establece las normas y flujos de trabajo para asegurar que el desarrollo sea fluido, colaborativo y profesional.

---

## 1. Convención de Ramas (Branching Strategy)

Utilizamos un modelo basado en ramas descriptivas para mantener el historial limpio:

*   `main`: Rama principal. Solo recibe código probado y aprobado mediante PR.
*   `develop`: Rama de integración para nuevas funcionalidades.
*   `feature/nombre-tarea`: Para nuevas funcionalidades (ej: `feature/implementar-triggers-auditoria`).
*   `bugfix/nombre-bug`: Para corrección de errores no críticos (ej: `bugfix/error-conexion-db`).
*   `hotfix/nombre-urgencia`: Para correcciones críticas en producción (ej: `hotfix/seguridad-inyeccion-sql`).

---

## 2. Conventional Commits

Seguimos el estándar de [Conventional Commits](https://www.conventionalcommits.org/). Cada mensaje de commit debe seguir este formato:

`<tipo>(<alcance opcional>): <descripción corta>`

### Tipos permitidos:
*   `feat`: Nueva funcionalidad.
*   `fix`: Corrección de un error.
*   `docs`: Cambios en documentación.
*   `style`: Cambios de formato (espacios, comas, etc.) que no afectan la lógica.
*   `refactor`: Cambios que no corrigen errores ni añaden funcionalidades.
*   `test`: Añadir o corregir tests.
*   `chore`: Tareas de mantenimiento, dependencias, etc.

**Ejemplos:**
*   `feat(auth): implementar validación de roles en base de datos`
*   `fix(query): corregir join en reporte de ventas`
*   `docs: actualizar diagrama entidad-relación`

---

## 3. Flujo de Trabajo de Pull Requests (PR)

Para enviar tus cambios:

1.  **Sincroniza:** Asegúrate de tener tu rama actualizada con `develop` antes de abrir el PR.
2.  **Checklist del PR:**
    *   [ ] He ejecutado los tests locales y todos pasan.
    *   [ ] El código sigue los estándares definidos.
    *   [ ] He documentado los cambios (si aplica).
    *   [ ] He eliminado código muerto o comentarios de depuración.
3.  **Descripción:** Incluye una descripción clara de qué hace el PR, por qué es necesario y cómo probarlo.
4.  **Revisión:** Todo PR requiere al menos una aprobación de un revisor asignado antes de ser fusionado.

---

## 4. Estándares de Código y Buenas Prácticas

Para mantener la calidad del proyecto, nos adherimos a los siguientes principios:

*   **Código Limpio (Clean Code):** Nombres de variables y funciones descriptivos en inglés (o español consistente).
*   **SQL:**
    *   Palabras reservadas en MAYÚSCULAS (`SELECT`, `FROM`, `WHERE`).
    *   Uso de alias claros en tablas.
    *   Evitar `SELECT *`; especificar siempre las columnas necesarias.
*   **Documentación:** Todo procedimiento almacenado, función o trigger complejo debe incluir un comentario breve explicando su propósito y parámetros.
*   **Seguridad:** Nunca incluir credenciales, tokens o datos sensibles en el repositorio. Utilizar variables de entorno (`.env`).
*   **Atomicidad:** Los commits deben ser atómicos (un cambio lógico por commit).

---

## 5. ¿Necesitas ayuda?

Si tienes dudas sobre cómo implementar algo o encuentras un problema, abre un **Issue** en el repositorio describiendo el inconveniente. Estaremos encantados de apoyarte.

¡Gracias por contribuir a `jfinfotest/proyecto-final-bases-datos`!