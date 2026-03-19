# 🛒 Microservicio de Inventario — MS-INVENTARIO

Microservicio desarrollado en Java con Spring Boot para la gestión de inventario de una tienda. Permite administrar productos con su stock, descripción, nombre y demás atributos relacionados.

**Integrantes:**
- Axel Subiabre
- Matias Molina

**Asignatura:** Ingeniería DevOps — DOY0101  
**Institución:** Duoc UC

---

## 📋 Descripción del Proyecto

Este repositorio corresponde a la Evaluación Parcial N°1 de la asignatura Ingeniería DevOps. El objetivo es implementar un flujo de trabajo DevOps completo utilizando Git, GitHub y GitHub Actions sobre un microservicio de inventario previamente desarrollado.

---

## 🌿 Estrategia de Ramificación — GitFlow

Se eligió **GitFlow** como estrategia de ramificación por las siguientes razones:

- Permite separar claramente el código en producción (`main`) del código en desarrollo (`develop`).
- Facilita el trabajo colaborativo en paralelo mediante ramas `feature/`.
- Permite gestionar errores críticos de forma ordenada mediante ramas `hotfix/` sin interrumpir el desarrollo normal.
- Es ideal para proyectos con ciclos de desarrollo estructurados y entregas definidas.

### Diagrama del flujo

```
main
 └── develop
       ├── feature/modelo-producto
       └── feature/controller-producto

main ←── hotfix/error (arreglo urgente directo a main)
```

---

## 🌱 Naming de Ramas

| Prefijo | Uso | Ejemplo |
|---|---|---|
| `main` | Código estable en producción | `main` |
| `develop` | Integración y pruebas | `develop` |
| `feature/` | Nueva funcionalidad | `feature/modelo-producto` |
| `hotfix/` | Arreglo urgente en producción | `hotfix/error` |

### Ramas del proyecto

- `main` — código base del microservicio
- `develop` — rama de integración
- `feature/modelo-producto` — se agregó el modelo de producto
- `feature/controller-producto` — se agregó el controlador de producto
- `hotfix/error` — se corrigió un error crítico en producción

---

## 📝 Convenciones de Commits

Se utilizó el estándar **Conventional Commits** para mantener trazabilidad del código:

| Prefijo | Uso |
|---|---|
| `feat:` | Nueva funcionalidad |
| `fix:` | Corrección de un error |
| `hotfix:` | Arreglo urgente en producción |
| `ci:` | Cambios en la configuración de CI/CD |
| `docs:` | Cambios en documentación |
| `refactor:` | Refactorización de código |

### Ejemplos

```
feat: agrega modelo de producto con atributos nombre, stock y descripcion
fix: corrige validacion de stock negativo
hotfix: corrige error critico en endpoint de productos
ci: agrega github actions para CI pipeline
docs: actualiza README con convenciones del equipo
```

---

## 🔀 Flujo de Merge

### Features → Develop
1. Se crea la rama `feature/` desde `develop`
2. Se realizan los cambios y se hace `push`
3. Se abre un **Pull Request** hacia `develop`
4. El compañero revisa y aprueba
5. Se realiza el merge

### Develop → Main
1. Una vez probados todos los cambios en `develop`
2. Se abre un **Pull Request** hacia `main`
3. Se revisa y aprueba
4. Se realiza el merge

### Hotfix → Main y Develop
1. Se crea la rama `hotfix/` desde `main`
2. Se corrige el error
3. Se abre **Pull Request** hacia `main`
4. Se abre **Pull Request** hacia `develop` (para mantenerla actualizada)

---

## 👥 Estrategia de Revisión de Pull Requests

- Todo Pull Request debe ser revisado y aprobado por el compañero antes del merge.
- No se permite hacer merge directo a `main` sin Pull Request.
- Se deben revisar los cambios en el código antes de aprobar.
- En caso de conflictos, se resuelven en conjunto antes del merge.

---

## ⚙️ GitHub Actions — CI Pipeline

Se configuró un workflow de integración continua en `.github/workflows/ci.yml` que se ejecuta automáticamente en los siguientes eventos:

- **Push a `develop`** — compila y testea los cambios nuevos
- **Pull Request a `main`** — valida que el código esté listo para producción

### ¿Qué hace el pipeline?

1. Clona el repositorio
2. Configura Java 17
3. Compila el proyecto con Maven (`mvn compile`)
4. Ejecuta los tests (`mvn test`)

### Rol en CI/CD

Este pipeline cumple la función de **Integración Continua (CI)**, automatizando la verificación del código cada vez que se integran cambios. Permite detectar errores de compilación o tests fallidos antes de llegar a producción, reduciendo el riesgo de desplegar código defectuoso.

---

## 🤖 Uso de Inteligencia Artificial

Durante el desarrollo de este proyecto se utilizó **Claude (Anthropic)** como herramienta de apoyo para:

- Orientación sobre el flujo de trabajo con GitFlow
- Explicación de comandos Git y su uso correcto
- Apoyo en la redacción y estructura de este README
- Consultas sobre la configuración de GitHub Actions

Todas las decisiones técnicas, justificaciones y reflexiones personales fueron elaboradas por los integrantes del equipo. El contenido generado con IA fue revisado y validado según los requerimientos del proyecto.

Referencia de citación: https://bibliotecas.duoc.cl/ia

---

## 📌 Conclusiones

### Axel Subiabre
*Me parecio una evaluacion muy llamativa ya que yo no tenia un conocimiento muy claro de como usar github y con esta evaluacion pude aprender a trabajar github mas profesionalmente*

### Matias Molina
*(Escribir reflexión personal aquí — sin uso de IA, explicando tu aprendizaje y contribución al proyecto)*

---

## 🛠️ Tecnologías

- Java 17
- Spring Boot
- Maven
- Git / GitHub
- GitHub Actions