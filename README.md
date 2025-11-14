📌 Appweb_Linkdgamehub– Plataforma de Juegos en la Nube con React, Java Microservices y Estructuras de Datos

Aplicación web que consume la API de GamePix para mostrar videojuegos mediante un iframe, soportada por una arquitectura de microservicios en Java, múltiples estructuras de datos personalizadas y un frontend moderno en React.

Este proyecto simula un modelo de negocio digital, integrando almacenamiento de usuarios, enrutamiento de microservicios y consumo de APIs externas.

se deja funcionamiento serveless por ai quieren montarlo a la nube

---

🏗️ Arquitectura General

La solución está dividida en tres grandes componentes:

### 1️⃣ Frontend – React (Puerto 5173)

Desarrollado con React.

Consume los microservicios para obtener datos.

Integra la API de GamePix mostrando los juegos mediante iframe.

Comunicación con los backend vía HTTP.


2️⃣ Backend 1 – Microservicio A (Puerto 8081)

Encargado de:

Gestión de juegos

Estructuras de datos:

Tabla Hash

Árbol Binario de Búsqueda

Cola de Prioridad

Este microservicio procesa la lógica y expone endpoints REST.


3️⃣ Backend 2 – Microservicio B (Puerto 8082)

Se encarga de:

Gestión de usuarios

Seguridad básica

Conexión a base de datos

Endpoints para login, registro y consulta de perfiles


4️⃣ Base de Datos – PostgreSQL (Puerto 5432)

Almacena:

Datos de usuarios

Configuración

Opciones del sistema


---

🧩 Tecnologías Utilizadas

Frontend
React 
JavaScript 
HTML, CSS


Backend
Java 17
Spring Boot
Arquitectura de microservicios

Estructuras de datos implementadas manualmente:
TablaHash
Árbol binario
Cola de prioridad



Base de Datos
PostgreSQL
JPA 
---

🚀 Cómo Ejecutar el Proyecto
A continuación los pasos completos para levantar cada componente localmente.

---

📌 1. Ejecutar la Base de Datos (PostgreSQL – Puerto 5432)
base de datos de usuarios
---

📌 2. Ejecutar Microservicio 1 (Java – Puerto 8081)

Este microservicio maneja la lógica de videojuegos y estructuras de datos.

Desde el proyecto del backend 1:

mvn spring-boot:run

Esto arrancará en:

👉 http://localhost:8081


---

📌 3. Ejecutar Microservicio 2 (Java – Puerto 8082)

Encargado del manejo de usuarios y conexión con PostgreSQL.

Ejecuta:

mvn spring-boot:run

Disponible en:

👉 http://localhost:8082


---

📌 4. Ejecutar el Frontend React (Puerto 5173)

Desde la carpeta del frontend:

npm install
npm run dev

Disponible en:

👉 http://localhost:5173


---

🔗 Comunicación entre módulos

El Frontend (5173) consulta a:

Microservicio de juegos → http://localhost:8081

Microservicio de usuarios → http://localhost:8082


El microservicio de usuarios usa PostgreSQL en:

localhost:5432

Los juegos de GamePix son renderizados mediante un:
<iframe src={gameUrl} />

---

🎮 Consumo de la API de GamePix

El frontend realiza peticiones a GamePix para obtener:

Listado de juegos

Información por categorías

URLs de carga dentro del iframe

Los microservicios pueden procesar, filtrar o almacenar estos datos con las estructuras definidas.


---

📂 Estructuras de Datos Implementadas

🔹 Tabla Hash

Para mapear y acceder a juegos o usuarios rápidamente.

🔹 Árbol Binario

Para búsquedas ordenadas y filtrado eficiente.

🔹 Cola de Prioridad

Para rankings, tendencias o seleccionar juegos destacados.

Estas estructuras están integradas en la lógica del microservicio 8081.




