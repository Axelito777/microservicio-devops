# 🚀 Microservicio DevOps - Gestión de Inventario

## 📌 Descripción

Este proyecto corresponde a un microservicio de gestión de inventario desarrollado en Java utilizando Spring Boot.
El objetivo es implementar una base sólida para un pipeline DevOps, aplicando control de versiones, trabajo colaborativo y automatización mediante CI/CD.

---

## 🌿 Estrategia de Ramificación: GitFlow

Se implementó el modelo **GitFlow** para organizar el desarrollo del proyecto.

### 🔹 Ramas principales

* `main`: contiene la versión estable del sistema (producción).
* `develop`: rama de integración donde se consolidan los cambios.

### 🔹 Ramas de trabajo utilizadas en este proyecto

* `feature/modelo-producto`
* `feature/controller-producto`
* `hotfix/error`

### ✅ Justificación

Se eligió GitFlow porque:

* Permite trabajo paralelo sin afectar producción.
* Mejora la organización del equipo.
* Facilita la trazabilidad de cambios.
* Es ideal para entornos colaborativos en DevOps.

---

## 👥 Flujo de Trabajo Colaborativo

Se simuló un entorno de desarrollo en equipo utilizando GitHub.

### 🔄 Flujo aplicado

1. Creación de ramas feature desde `develop`
2. Desarrollo de funcionalidades en paralelo:

   * Modelo de producto
   * Controlador de producto
3. Uso de commits con mensajes claros
4. Creación de Pull Requests hacia `develop`
5. Revisión de código entre integrantes
6. Integración de cambios mediante merge

### 🔥 Hotfix

Se implementó una corrección urgente:

* Rama: `hotfix/error`
* Origen: `main`
* Destino: `main`

---

## 📝 Convenciones de Commits

Se utilizaron las siguientes convenciones:

* `feat:` nueva funcionalidad
* `fix:` corrección de errores
* `docs:` cambios en documentación
* `refactor:` mejora del código
* `test:` pruebas

### 📌 Ejemplo

```
feat: creación del modelo Producto
fix: corrección de error en API
```

---

## 🏷️ Naming de Ramas

Se siguieron estándares para nombrar ramas:

* `feature/nombre-funcionalidad`
* `hotfix/nombre-error`

### 📌 Ejemplos reales del proyecto

```
feature/modelo-producto
feature/controller-producto
hotfix/error
```

---

## 🔄 Estrategia de Merge

* `feature` → `develop` mediante Pull Request
* `develop` → `main` cuando el sistema está estable
* `hotfix` → `main` directamente

Se utilizó revisión de código antes de cada merge para asegurar calidad.

---

## ⚙️ Integración Continua (CI/CD)

Se configuró **GitHub Actions** para automatizar el proceso de integración.

### 📌 Ejecución del pipeline

* Push a `develop`
* Pull Request hacia `main`

### 📌 Funcionalidad

* Clonación del repositorio
* Ejecución de tareas básicas de validación

### 🎯 Beneficios

* Detección temprana de errores
* Automatización del flujo de trabajo
* Mejora en la calidad del código

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



## 📌 Conclusión

El desarrollo de este proyecto permitió aplicar:

* Control de versiones con Git
* Estrategias de ramificación (GitFlow)
* Trabajo colaborativo con Pull Requests
* Automatización con GitHub Actions

---

## 👤 Integrantes

* Axel Subiabre
* Matías Molina

---
