# 🏠 HogarYA — Sistema de Gestión Inmobiliaria

![Java](https://img.shields.io/badge/Java-17-orange?logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-4.x-6DB33F?logo=springboot&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring%20Data%20JPA-59666C?logo=spring&logoColor=white)
![Thymeleaf](https://img.shields.io/badge/Thymeleaf-005F0F?logo=thymeleaf&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?logo=apachemaven&logoColor=white)

> Aplicación web para la **gestión integral de una inmobiliaria**: propiedades, publicaciones, contratos y facturación, con seguimiento del ciclo de vida de cada operación.

---

## 📋 Descripción

**HogarYA** es un sistema desarrollado como Trabajo Final, que permite a una inmobiliaria administrar todo su negocio desde una única aplicación web: cargar y publicar propiedades, generar contratos de alquiler/venta, emitir facturas y llevar el registro de personas y ubicaciones.

El proyecto se construyó siguiendo una **arquitectura por capas** y un desarrollo guiado por **historias de usuario (HU)**, con control de estados y reglas de negocio en cada entidad (por ejemplo, no se puede eliminar una propiedad con un contrato activo).

---

## ✨ Funcionalidades principales

- 🏘️ **Propiedades** — alta, baja, modificación y listado, con tipos de propiedad, estados de disponibilidad y validación de duplicados.
- 📢 **Publicaciones** — gestión de avisos con control de publicaciones activas y reglas de eliminación.
- 📄 **Contratos** — creación, modificación y baja, con estados y trazabilidad.
- 🧾 **Facturación** — emisión y gestión de facturas, medios de pago y estados.
- 👤 **Personas** — administración de propietarios/inquilinos.
- 📍 **Ubicaciones** — gestión de provincias y ciudades.
- 🕓 **Historial de estados** — auditoría de los cambios de estado de propiedades, publicaciones, contratos y facturas.
- ✅ **Validaciones y excepciones de negocio** — manejo de errores propio y mensajes claros al usuario.

---

## 🛠️ Tecnologías

| Categoría | Tecnología |
|---|---|
| Lenguaje | **Java 17** |
| Framework | **Spring Boot 4** (Web MVC) |
| Persistencia | **Spring Data JPA** (Hibernate) |
| Vistas | **Thymeleaf** |
| Base de datos | **MySQL** |
| Validación | **Bean Validation** (spring-boot-starter-validation) |
| Build | **Maven** (con wrapper `mvnw`) |

---

## 🏗️ Arquitectura

Proyecto organizado en **capas** bajo el paquete `com.desi`:

```
com.desi
├── entidades      → modelos JPA (Propiedad, Publicacion, Contrato, Factura,
│                     Persona, Ciudad, Provincia...) + enums de estados e historial
├── accesoDatos    → repositorios (Spring Data JPA)
├── servicios      → lógica de negocio (interfaces + impl)
├── presentacion   → controladores Spring MVC
└── excepciones    → excepciones de negocio propias
```

Las vistas se encuentran en `src/main/resources/templates` (Thymeleaf), con fragmentos reutilizables como la barra de navegación.

---

## 🚀 Cómo ejecutarlo

### Requisitos
- **JDK 17**
- **MySQL** en ejecución
- Maven (o usar el wrapper `mvnw` incluido)

### Pasos
```bash
# 1. Clonar el repositorio
git clone https://github.com/Josefinaac95/TrabajoFinal_Inmobiliaria-HogarYA.git
cd TrabajoFinal_Inmobiliaria-HogarYA

# 2. Crear la base de datos en MySQL (ejemplo)
#    CREATE DATABASE hogarya;

# 3. Configurar tus credenciales de MySQL en:
#    src/main/resources/application.properties

# 4. Levantar la aplicación
./mvnw spring-boot:run        # en Windows: mvnw.cmd spring-boot:run
```

La app queda disponible en **http://localhost:8080**

---

## 👥 Autores

Trabajo Final desarrollado en equipo:

- **Josefina Acevedo** — [@Josefinaac95](https://github.com/Josefinaac95)
- David Reigenborn
- Ignacio Oroño
- Franco Zambuto

---

<p align="center">Desarrollado como proyecto académico · Java + Spring Boot 🌱</p>
