# 💬 Foro Alura — Challenge ONE

![Java](https://img.shields.io/badge/Java-17+-orange?style=flat-square&logo=java)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-brightgreen?style=flat-square&logo=springboot)
![Spring Security](https://img.shields.io/badge/Spring_Security-JWT-blue?style=flat-square&logo=springsecurity)
![MySQL](https://img.shields.io/badge/Database-MySQL-informational?style=flat-square&logo=mysql)
![Status](https://img.shields.io/badge/STATUS-FINALIZADO-darkgreen?style=flat-square)

> API REST construida con Spring Boot para gestionar tópicos de un foro educativo.
> 4° Challenge del programa Oracle Next Education (ONE) — Formación Backend Java.

---

## ✨ Funcionalidades

- ✅ CRUD completo de **tópicos** (crear, listar, buscar, actualizar, eliminar)
- ✅ Gestión de **usuarios** y **cursos**
- ✅ Autenticación con **Spring Security + Token JWT**
- ✅ Encriptación de contraseñas con **BCrypt**
- ✅ Validaciones según reglas de negocio
- ✅ Persistencia en base de datos **MySQL**
- ✅ Rutas REST siguiendo buenas prácticas

---

## 🛠️ Tecnologías

| Herramienta | Uso |
|---|---|
| Java 17+ | Lenguaje principal |
| Spring Boot | Framework backend |
| Spring Security | Autenticación y autorización |
| JWT | Tokens de acceso |
| MySQL | Base de datos relacional |
| Flyway | Migraciones de BD |
| IntelliJ IDEA | IDE de desarrollo |
| Insomnia | Testing de endpoints |

---

## 📡 Endpoints principales

### 🔐 Autenticación
POST /login           → Genera token JWT
POST /usuarios        → Registra nuevo usuario (password: BCrypt)
GET  /usuarios        → Lista todos los usuarios

### 📚 Cursos
POST /cursos          → Registra un nuevo curso
GET  /cursos          → Lista todos los cursos

### 💬 Tópicos
POST   /topicos       → Crea un nuevo tópico
GET    /topicos       → Lista todos los tópicos
GET    /topicos/{id}  → Detalle de un tópico
PUT    /topicos/{id}  → Actualiza un tópico
DELETE /topicos/{id}  → Elimina un tópico

> ⚠️ Todos los endpoints (excepto `/login`) requieren token JWT en el header:
> `Authorization: Bearer <token>`

---

## ⚙️ Configuración e instalación

```bash
# 1. Clona el repositorio
git clone https://github.com/SamySierraDV/AluraLatam-ForoHub-Challenge-Alura.git

# 2. Configura application.properties
spring.datasource.url=jdbc:mysql://localhost:3306/foro_alura
spring.datasource.username=root
spring.datasource.password=tu_password
api.security.secret=tu_jwt_secret

# 3. Ejecuta el proyecto desde IntelliJ o con Maven
./mvnw spring:boot run
```

---

## 🔑 Credenciales de prueba

| Campo | Valor |
|---|---|
| Email | `admin@foro.com` |
| Password | `admin` *(encriptada con BCrypt)* |

---

## 🤝 Créditos

Desarrollado por **Samy Suarez** como parte del **Challenge ONE — Oracle Next Education G9**
con Alura Latam. Formación Backend Java + Spring Boot.
