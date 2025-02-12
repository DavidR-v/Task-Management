# Task-Management
Prueba técnica
Sistema de Gestión de Tareas

Este es un sistema de gestión de tareas desarrollado como parte de una prueba técnica. El proyecto incluye un backend en Node.js con autenticación JWT, un frontend en React para la interfaz de usuario, y una base de datos PostgreSQL para la persistencia de datos. Además, se han implementado pruebas unitarias y se ha documentado la API RESTful.

Tabla de Contenidos
1. [Requisitos Previos](#requisitos-previos)
2. [Instalación y Ejecución](#instalación-y-ejecución)
   - [Backend](#backend)
   - [Frontend](#frontend)
3. [Detalles Técnicos](#detalles-técnicos)
4. [Pruebas Unitarias](#pruebas-unitarias)
5. [Resultados de las Pruebas](#resultados-de-las-pruebas)
6. [Endpoints de la API](#endpoints-de-la-api)
7. [Autor](#autor)



Requisitos Previos

Asegúrate de tener instalado lo siguiente en tu máquina:

- Node.js (versión LTS recomendada)
- PostgreSQL(configurado y en ejecución)
- Git
- Visual Studio Code** u otro editor de código
- Postman (para probar la API)



Instalación y Ejecución**

Backend

1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu-usuario/task-management.git
   cd task-management/backend
   ```

2. Instala las dependencias:
   ```bash
   npm install
   ```

3. Configura las variables de entorno:
   Crea un archivo `.env` en la carpeta `backend/` con el siguiente contenido:
   ```env
   PORT=5000
   DB_HOST=localhost
   DB_USER=postgres
   DB_PASSWORD=tu_contraseña
   DB_NAME=task_management
   JWT_SECRET=secret_key
   ```

4. Inicia el servidor:
   ```bash
   npm start
   ```
   El backend estará disponible en `http://localhost:5000`.


Frontend

1. Navega a la carpeta `frontend`:
   ```bash
   cd ../frontend
   ```

2. Instala las dependencias:
   ```bash
   npm install
   ```

3. Inicia la aplicación:
   ```bash
   npm start
   ```
   El frontend estará disponible en `http://localhost:3000`.



Detalles Técnicos

Tecnologías Utilizadas
- Frontend: React, Axios, React Router DOM.
- Backend: Node.js, Express, Sequelize, JWT.
- Base de Datos: PostgreSQL.
- Pruebas Unitarias: Jest, Supertest.
- Herramientas: Postman (documentación de API), Git (control de versiones).

Estructura del Proyecto

- Backend:
  - `src/controllers/`: Controladores para manejar la lógica de negocio.
  - `src/models/`: Modelos de la base de datos (User, Task).
  - `src/routes/`: Rutas RESTful.
  - `src/middleware/`: Middleware para autenticación y validaciones.
- Frontend*:
  - `src/components/`: Componentes reutilizables.
  - `src/pages/`: Páginas principales (Login, Register, Tasks).
  - `src/App.js`: Configuración de rutas.


Pruebas Unitarias

Las pruebas unitarias cubren las siguientes áreas:
- Autenticación: Registro e inicio de sesión.
- CRUD de Tareas: Creación, lectura, actualización y eliminación.
- Validaciones: Manejo de entradas inválidas (fechas, estados, prioridades).

Cómo Ejecutar las Pruebas
Desde la carpeta `backend`, ejecuta:
```zsh
npm test
```

Para generar un reporte de cobertura:
```zsh
npm test -- --coverage
```



//Resultados de las Pruebas

El resultado de las pruebas unitarias muestra una cobertura del 90% o más. Los reportes de cobertura están disponibles en la carpeta `backend/coverage/`.

Ejemplo de salida:
```
 PASS  tests/auth.test.js
 PASS  tests/task.test.js

Test Suites: 2 passed, 2 total
Tests:       10 passed, 10 total
Snapshots:   0 total
Time:        2.5s
Ran all test suites.
```



//Endpoints de la API

La API RESTful expone los siguientes endpoints:

//Autenticación
- `POST /api/register`: Registro de usuarios.
- `POST /api/login`: Inicio de sesión.

//Gestión de Tareas
- `GET /api/tasks`: Listar tareas (filtradas por estado y prioridad).
- `POST /api/tasks`: Crear una nueva tarea.
- `PUT /api/tasks/:id`: Actualizar una tarea existente.
- `DELETE /api/tasks/:id`: Eliminar una tarea.

Documentación completa disponible en Postman.

//Autor

Desarrollado por Jesus David Rentería.  
Contacto: phmixt@gmail.com  
GitHub: [https://github.com/DavidR-v](https://github.com/DavidR-v)

