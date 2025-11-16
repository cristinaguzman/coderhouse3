# 📘 Proyecto 3 – Plataforma de Gestión de Cursos  
**Angular 17 — Coderhouse**

Este proyecto corresponde a la **Tercera Entrega del Proyecto Final** del curso de Angular de Coderhouse.  
Se trata de una aplicación web para gestionar:

- **Alumnos**
- **Cursos**
- **Inscripciones**
- **Usuarios (solo admin)**
- **Autenticación con roles**
- **Layout completo con Toolbar + Sidenav**
- **Consumo de API (MockAPI)**

El objetivo es aplicar en un solo proyecto todo lo aprendido durante la cursada: módulos, routing avanzado, guards, servicios, interceptores, comunicación con API, lazy loading, buenas prácticas y arquitectura escalable.

---

# ⭐ Características principales del proyecto

### 🔐 Autenticación
- Login con email y contraseña.
- Servicio `AuthService` conectado a MockAPI.
- Token almacenado en `localStorage`.
- Usuario actual disponible mediante un `BehaviorSubject`.

### 💼 Roles
- Rol **admin** → acceso a *Usuarios* + todo el sistema.
- Rol **user** → acceso a secciones funcionales (alumnos, cursos, inscripciones).
- `RoleGuard` protege rutas según permisos.

### 🛡 Protección de rutas
- `AuthGuard` evita el acceso sin login.
- Redirecciones automáticas cuando no hay sesión activa.

### 🧱 Arquitectura modular
- Módulo `auth/`
- Módulo `layout/`
- Módulo `core/` (servicios, guards, interceptores)
- Módulo `shared/`
- Feature modules:
  - `alumnos/`
  - `cursos/`
  - `inscripciones/`
  - `usuarios/`

Con Lazy Loading en todas las secciones.

### 🧭 Layout profesional
- Toolbar con nombre del usuario + logout
- Sidenav dinámico según rol
- Router outlet principal

### 📚 Conexión a MockAPI
El proyecto utiliza endpoints REST para manejar:

- Usuarios
- Alumnos
- Cursos
- Inscripciones

Incluye CRUD según corresponde.

---

# 🏗 Tecnologías utilizadas

- Angular 17
- TypeScript
- RxJS
- HTML + CSS
- MockAPI
- Angular Routing
- Interceptors + Guards
- LocalStorage para persistencia simple

---

# 📁 Estructura del proyecto

```
src/
 ├── app/
 │   ├── auth/
 │   ├── core/
 │   ├── layout/
 │   ├── features/
 │   │   ├── alumnos/
 │   │   ├── cursos/
 │   │   ├── inscripciones/
 │   │   └── usuarios/
 │   ├── app-routing.module.ts
 │   └── app.module.ts
 ├── assets/
 ├── environments/
 ├── index.html
 ├── main.ts
 └── styles.css
```

---

# 🚀 Cómo ejecutar el proyecto

### 1. Clonar repositorio
```bash
git clone https://github.com/TU-USUARIO/proyecto3-angular.git
cd proyecto3-angular
```

### 2. Instalar dependencias
```bash
npm install
```

### 3. Configurar MockAPI
En:

```
src/environments/environment.ts
```

Coloca la URL base de tu API:

```ts
export const environment = {
  production: false,
  apiUrl: "https://mockapi.io/tuproject/api"
};
```

### 4. Ejecutar el servidor
```bash
ng serve -o
```

---

# 🧪 Usuarios de prueba

| Email         | Contraseña | Rol    |
|---------------|------------|--------|
| admin@test.com | 123456     | admin  |
| user@test.com  | 123456     | user   |

---

# ✔ Funcionalidades por sección

## 🔹 Alumnos
- Listado
- Detalle de alumno
- Ver cursos inscritos
- Desinscribir alumno

## 🔹 Cursos
- Listado de cursos disponibles

## 🔹 Inscripciones
- Vista general de inscripciones
- Preparado para ampliar en el proyecto final

## 🔹 Usuarios (admin)
- Listado de usuarios registrados

---

# 🔧 Buenas prácticas aplicadas
- Arquitectura escalable
- Lazy Loading
- Guards para seguridad
- Interceptor de autenticación
- RxJS para manejo de estado
- Models tipados en TypeScript
- Código organizado en modules

---

# 🙋‍♀️ Autora

**Cristina Guzmán Valdés**  
Diseñadora UX/UI · Frontend en formación  
Chile 🇨🇱
