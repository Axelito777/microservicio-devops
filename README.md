# 🚀 Microservicio DevOps - Gestión de Inventario

## 📌 Descripción del Proyecto

Este proyecto corresponde a un microservicio de gestión de inventario desarrollado en Java con Spring Boot.
Su objetivo es servir como base para la implementación de un pipeline DevOps, integrando control de versiones, trabajo colaborativo y automatización mediante CI/CD.

---

## 🌿 Estrategia de Ramificación: GitFlow

Para este proyecto se utilizó el modelo **GitFlow**, ya que permite organizar el trabajo colaborativo de manera clara y estructurada.

### 🔹 Ramas principales

* `main`: contiene el código en estado de producción.
* `develop`: rama de integración donde se consolidan las nuevas funcionalidades.

### 🔹 Ramas de soporte

* `feature/<nombre>`: desarrollo de nuevas funcionalidades.
* `hotfix/<nombre>`: corrección de errores críticos en producción.

###  Justificación

Se eligió GitFlow porque:

* Permite trabajar en paralelo sin afectar producción.
* Facilita la trazabilidad del código.
* Es ideal para equipos de desarrollo colaborativo.

---

## 👥 Flujo de Trabajo Colaborativo

El flujo de trabajo utilizado fue el siguiente:

1. Creación de rama desde `develop`:

   ```
   git checkout develop
   git checkout -b feature/nueva-funcionalidad
   ```

2. Desarrollo y commits:

   ```
   git add .
   git commit -m "Cambio Del modelo"
   ```

3. Subida de cambios:

   ```
   git push origin feature/
   ```

4. Creación de Pull Request hacia `develop`.

5. Revisión de código por otro integrante.

6. Merge a `develop`.

### 🔥 Hotfix

1. Se crea desde `main`
2. Se corrige el error
3. PR hacia `main`

---

## 📝 Convenciones de Commits

Se utilizaron mensajes de commit estandarizados:

* `feat:` nueva funcionalidad
* `fix:` corrección de errores
* `docs:` cambios en documentación
* `refactor:` mejoras internas del código
* `test:` pruebas

Ejemplo:

```
feat: agregar endpoint para crear producto
```

---

## 🏷️ Naming de Ramas

* `feature/nombre-funcionalidad`
* `hotfix/nombre-error`

Ejemplos:

```
feature/login
feature/registro-producto
hotfix/error-
```

---

## 🔄 Estrategia de Merge

* Las ramas `feature` se integran a `develop` mediante Pull Request.
* La rama `develop` se integra a `main` cuando está estable.
* Los `hotfix` se integran directamente a `main`.

---

## ⚙️ Integración Continua (CI/CD)

Se configuró **GitHub Actions** para automatizar el flujo de integración.

### 📌 Funcionamiento

El pipeline se ejecuta cuando:

* Se hace `push` a la rama `develop`
* Se crea un `pull request` hacia `main`

### 📌 Tareas del pipeline

* Clonar el repositorio
* Ejecutar tareas básicas (validación de integración)

Esto permite:

* Detectar errores rápidamente
* Mantener calidad del código
* Automatizar procesos DevOps

---

## 📁 Estructura del Proyecto

```
src/
 ├── controller/
 ├── service/
 ├── repository/
 ├── model/
 ├── dto/
```

---



---

## 📌 Conclusión

Este proyecto permitió aplicar conceptos de:

* Control de versiones con Git
* Trabajo colaborativo
* Estrategias de ramificación
* Automatización con GitHub Actions

---

## 👤 Integrantes

* Matias Molina
* Axel Subiabre

---
