# 🏋️‍♂️ HealthU – Plataforma de Gestión Fitness y Retos 

**HealthU** es una solución digital integral diseñada para **automatizar la gestión de gimnasios**, **promover hábitos saludables** y **gamificar la experiencia de entrenamiento** para aprendices del SENA y usuarios en general.  
El sistema está compuesto por tres módulos principales: **Web Administrador**, **App Móvil** y **Backend RESTful**, desplegados en la nube mediante **AWS**.

---

## 🚀 Tecnologías Principales

| Módulo | Tecnologías | Descripción |
|--------|--------------|-------------|
| 🌐 **Frontend Web (Administrador)** | Angular 19, Bootstrap 5, TypeScript | Interfaz administrativa para gestionar usuarios, rutinas, desafíos y métricas. |
| 📱 **App Móvil (Aprendiz)** | Flutter (Dart) | Aplicación para aprendices con registro de medidas, retos, progreso y validación por QR. |
| ⚙️ **Backend REST API** | Spring Boot 3, Spring Security (JWT), JPA, MySQL | Pruebas unitarias (Junit5, Mockito)| Servicio central que gestiona autenticación, usuarios, desafíos y rutinas. |
| ☁️ **Infraestructura** | AWS EC2, RDS, SCP/SSH Deployment | Despliegue en nube con base de datos MySQL en RDS y servidores EC2. |

---

## 🌍 URL de Producción

> 🔗 **Web Administrador (Angular):**  
> [http://54.227.38.102/iniciar-sesion](http://54.227.38.102/iniciar-sesion)

> ⚙️ **Backend (Spring Boot):**  
> http://54.227.38.102:8080/swagger-ui/index.html#/ *(Docuemntacion API)*

> 📱 **App Móvil (Flutter):**  
> Consume los mismos endpoints del backend mediante peticiones HTTP. Actualemnte se está implementando servicio en play store.
> 
> https://drive.google.com/file/d/17waOUCgcvLc0fbgeb0Kby-N6DRWqN3l5/view?usp=sharing (instalador directo .apk)

---

## 🧩 Características Principales

### 🔐 Autenticación y Seguridad
- Inicio de sesión con JWT.
- Roles de usuario (Administrador / Aprendiz / Entrenador).

### 🧑‍💻 Módulo Administrador (Web)
- Registro y gestión de aprendices.
- Asignación y seguimiento de rutinas.
- Creación y control de desafíos motivacionales.
- Visualización de métricas (gráficas, rankings y promedios).

### 💪 Módulo Aprendiz (App Móvil)
- Registro de medidas físicas y progreso.
- Escaneo de códigos QR para validar rutinas/desafíos.
- Visualización de estadísticas personales.
- Ranking general de aprendices.

### 📊 Dashboard
- Total de aprendices activos.
- Promedio de horas entrenadas.
- Ranking top 20 de aprendices por puntos y horas.

---

## 🧾 Requisitos Previos

### 🔧 Backend
- Java 17+
- Maven 3.8+
- MySQL 8+
- Spring Boot 3+

### 🌐 Frontend Web
- Node.js 20+
- Angular CLI 19+
- Bootstrap 5.3+

### 📱 App Móvil
- Flutter SDK 3.7+
- Android Studio o VS Code

---
# 📂 Estructura del Repositorio – SenaHealthU

Este repositorio contiene todos los componentes del proyecto **HealthU**, una plataforma integral para la gestión de gimnasios, registro de hábitos saludables y seguimiento de retos lúdicos de aprendices SENA.  
Incluye el **backend**, los **frontends web y móvil**, y la **documentación técnica** centralizada.

---

## 🏗️ Estructura General

```
SenaHealthU/
├── .git/ # Carpeta de control de versiones Git
├── back-SenaGym/ # Backend en Spring Boot (API REST)
├── front-senaHealthU/ # Frontend web en Angular
├── mobile-healthU/ # Aplicación móvil en Flutter
└── Documentacion/ # Documentos técnicos, reportes e informes
```


---

## 📦 Descripción de Carpetas

### ⚙️ `back-SenaGym/`
Contiene el **módulo backend** desarrollado en **Spring Boot 3**.  
Provee los servicios REST que conectan la base de datos MySQL con las interfaces web y móvil.

**Contenido principal:**
- `src/main/java/com/gym/...` → código fuente del backend.  
- `src/main/resources/application.properties` → configuración de conexión (MySQL, JWT, etc).  
- `pom.xml` → dependencias y build con Maven.

**Tecnologías:** Java 17, Spring Boot, Spring Security, JPA, MySQL, Lombok.

---

### 🌐 `front-senaHealthU/`
Interfaz **web administrativa** desarrollada en **Angular 19**.  
Permite gestionar usuarios, rutinas, desafíos, métricas y roles de acceso.

**Contenido principal:**
- `/src/app/` → componentes, servicios y vistas.  
- `/src/environments/` → variables de entorno.  
- `/dist/` → compilado de producción para despliegue.

**Tecnologías:** Angular, TypeScript, Bootstrap 5, RxJS.

---

### 📱 `mobile-healthU/`
Aplicación **móvil para aprendices**, desarrollada en **Flutter**.  
Permite registrar medidas, participar en retos, escanear QR, y visualizar el progreso personal.

**Contenido principal:**
- `/lib/` → pantallas, widgets y servicios HTTP.  
- `/assets/` → imágenes y animaciones.  
- `/android/` y `/ios/` → configuraciones de plataforma.

**Tecnologías:** Flutter 3, Dart, HTTP, Shared Preferences, Mobile Scanner.

---

### 🗂️ `Documentacion/`
Carpeta dedicada a los documentos de apoyo y entregables del proyecto:
- Diagramas de arquitectura y casos de uso.
- Informe técnico y memoria del proyecto.
- Presentaciones, manuales y documentación funcional.

**Formato esperado:** `.pdf`, `.docx`, `.pptx`, `.md`.

---

## 🔧 Requisitos mínimos para desarrollo

| Módulo | Requisitos |
|--------|-------------|
| Backend | Java 17+, Maven 3.8+, MySQL 8+ |
| Frontend Web | Node.js 20+, Angular CLI 19+ |
| App Móvil | Flutter SDK 3.7+, Android Studio / VS Code |
| Documentación | Visualizador PDF / Editor de texto |

---

## 🌍 Despliegue Actual

| Módulo | Entorno | URL |
|--------|----------|------|
| Web (Angular) | AWS EC2 | [http://54.227.38.102/iniciar-sesion](http://54.227.38.102/iniciar-sesion) |
| Backend (Spring Boot) | AWS EC2 / RDS | API REST interna |
| Base de Datos | AWS RDS MySQL | Gestiona usuarios, rutinas y desafíos |
| App Móvil (Flutter) | Android / iOS | Consume la API REST del backend |

---

## 🧭 Propósito del Repositorio

Este repositorio agrupa **todos los módulos del ecosistema HealthU** en un único espacio Git, facilitando:
- El mantenimiento coordinado entre backend, frontend y app móvil.  
- El control de versiones centralizado.  
- La documentación integral del proyecto.  
- La colaboración entre desarrolladores y administradores del sistema.

---

## 👨‍💻 Equipo de Desarrollo

| Nombre | Rol | Especialidad |
|---------|------|--------------|
| Santiago Arias | Desarrollador Full Stack | Angular · Flutter · Spring Boot |
| Equipo HealthU | Colaboradores | Frontend · Backend · DevOps |
| Eduardo Moreno | Santiago Quilindo | David Mera - Jenifer E. | 

---

> 💚 *“HealthU – tu esfuerzo, nuestro motor. Una comunidad forjada en disciplina, tecnología y salud.”*
