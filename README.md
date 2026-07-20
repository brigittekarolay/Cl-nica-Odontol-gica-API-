# Sistema Web para la Gestión de una Clínica Dental

## Integrantes


- Velasquez Puma Brigitte Karolay
- Ticona Nina Valeria Abigai
- Lerma Ccopa Jhonatan Javier

## Descripción del proyecto

Este proyecto consiste en el desarrollo de una aplicación web para la administración integral de una clínica dental, implementando una arquitectura cliente-servidor.

El sistema está dividido en dos componentes principales:

- **Backend:** desarrollado con Django y Django REST Framework, encargado de la lógica del negocio, gestión de la base de datos y exposición de una API REST.
- **Frontend:** desarrollado con React y Vite, encargado de ofrecer una interfaz moderna, dinámica e interactiva para los usuarios.

La aplicación permite administrar pacientes, especialistas, especialidades, citas, historiales clínicos, procedimientos, tratamientos sugeridos, presupuestos y pagos, facilitando la gestión diaria de una clínica dental.

---

# Objetivos del proyecto

- Desarrollar una API REST utilizando Django REST Framework.
- Implementar una interfaz web moderna con React.
- Gestionar la información clínica mediante el ORM de Django.
- Facilitar la administración de pacientes y especialistas.
- Centralizar la información médica y administrativa.
- Aplicar una arquitectura desacoplada entre frontend y backend.

---

# Tecnologías utilizadas

## Backend

- Python
- Django
- Django REST Framework
- SQLite
- Swagger
- ORM de Django
- CORS
- simple JWT

## Frontend

- React
- Vite
- JavaScript / TypeScript
- HTML5
- CSS

## Herramientas

- Git
- Node.js
- npm
- Entorno virtual (`venv`)

---

# Estructura general del proyecto

```
├── clinic
│   ├── __init__.py
│   ├── admin.py
│   ├── api_urls.py
│   ├── apps.py
│   ├── models.txt
│   ├── permissions.py
│   ├── tests.py
│   ├── api_urls.py
│   ├── migrations
│   ├── serializers
│   ├── api_views
│   ├── models
├── clinica-frontend
│   ├── README.md
│   ├── index.html
│   ├── package-lock.json
│   ├── package.json
│   ├── tsconfig.app.json
│   ├── tsconfig.json
│   ├── tsconfig.node.json
│   └── vite.config.ts
│   ├── public
│   ├── src
│   │   ├── App.css
│   │   ├── App.tsx
│   │   ├── api
│   │   ├── assets
│   │   ├── components
│   │   ├── context
│   │   ├── hooks
│   │   ├── index.css
│   │   ├── main.tsx
│   │   ├── pages
│   │   └── types
├── config
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── manage.py
├── package-lock.json
├── package.json
├── requirements.txt
```

---

# Funcionalidades principales

El sistema permite administrar:

- Pacientes.
- Especialistas.
- Especialidades.
- Citas odontológicas.
- Procedimientos.
- Historiales clínicos.
- Tratamientos sugeridos.
- Presupuestos.
- Detalle de presupuestos.
- Pagos.
- Consumo de servicios REST desde React.

---

# Requisitos previos

Antes de ejecutar el proyecto se recomienda tener instalado:

- Python 3.12 o superior
- Node.js 18 o superior
- npm
- Git
- Entorno virtual de Python

---

# Instalación del Backend

## 1. Clonar el repositorio

```bash
git clone https://github.com/brigittekarolay/Cl-nica-Odontol-gica-API-
```

## 2. Ingresar al proyecto

```bash
cd Cl-nica-Odontol-gica-API-
```

## 3. Crear un entorno virtual

```bash
python -m venv venv
```

### ¿Qué es un entorno virtual?

Un entorno virtual permite aislar las dependencias del proyecto para evitar conflictos con otras aplicaciones instaladas en el sistema.

## 4. Activar el entorno virtual

### Windows (PowerShell)

```powershell
.\venv\Scripts\activate
```

### Windows (CMD)

```cmd
venv\Scripts\activate.bat
```

### Linux / macOS

```bash
source venv/bin/activate
```

## 5. Instalar las dependencias

```bash
pip install -r requirements.txt
```

## 6. Configurar las variables de entorno

Editar el archivo `.env` con la configuración correspondiente.

Ejemplo:

```env
DATABASE_URL=postgresql://usuario:contraseña@host:puerto/nombre_db
SECRET_KEY=tu_clave_secreta
DEBUG=True
```

## 7. Aplicar las migraciones

```bash
python manage.py migrate
```

### ¿Qué son las migraciones?

Las migraciones permiten crear y actualizar la estructura de la base de datos a partir de los modelos definidos en Django.

## 8. Crear un superusuario (opcional)

```bash
python manage.py createsuperuser
```

El sistema solicitará:

- Nombre de usuario
- Correo electrónico
- Contraseña

Este usuario tendrá acceso completo al panel administrativo.

## 9. Ejecutar el servidor

```bash
python manage.py runserver
```

El backend estará disponible en:

```text
http://127.0.0.1:8000/
```

---

# Instalación del Frontend

Ingresar a la carpeta del frontend.

```bash
cd clinica-frontend
```

Instalar las dependencias.

```bash
npm install
```

Ejecutar el servidor de desarrollo.

```bash
npm run dev
```

El frontend estará disponible en:

```text
http://localhost:5173/
```

---

# API REST

El backend implementa una API REST desarrollada con Django REST Framework.

Entre las principales operaciones disponibles se encuentran:

- Gestión de pacientes.
- Gestión de especialistas.
- Gestión de especialidades.
- Registro de citas.
- Administración de procedimientos.
- Gestión de historiales clínicos.
- Registro de tratamientos sugeridos.
- Administración de presupuestos.
- Registro de pagos.

La comunicación entre el frontend y el backend se realiza mediante solicitudes HTTP utilizando formato JSON.

---

# Organización del Backend

La aplicación Django está organizada en distintos módulos:

| Carpeta | Descripción |
|----------|-------------|
| models | Modelos de la base de datos |
| serializers | Conversión entre modelos y JSON |
| api_views | Endpoints de la API REST |
| views | Vistas tradicionales de Django |
| templates | Plantillas HTML |
| migrations | Migraciones de la base de datos |

---

# Organización del Frontend

El proyecto React se encuentra organizado por responsabilidades.

| Carpeta | Descripción |
|----------|-------------|
| api | Comunicación con la API REST |
| assets | Recursos estáticos |
| components | Componentes reutilizables |
| context | Gestión del estado global |
| hooks | Hooks personalizados |
| pages | Páginas del sistema |
| types | Tipos e interfaces |

---

# Tecnologías utilizadas

| Tecnología | Uso |
|------------|-----|
| Python | Lenguaje principal |
| Django | Framework Backend |
| simple JWT | Seguridad |
| Swagger drf_spectacular | Documentación |
| Django REST Framework | Desarrollo de API REST |
| PosgreSQL | Base de datos |
| React | Frontend |
| Vite | Empaquetador y servidor de desarrollo |
| JavaScript / TypeScript | Desarrollo del cliente |
| HTML5 | Estructura de la interfaz |
| CSS | Diseño de la interfaz |
| Git | Control de versiones |

---

# Conclusión

Este proyecto implementa una solución web para la gestión integral de una clínica dental mediante una arquitectura desacoplada entre backend y frontend.

El backend desarrollado con **Django** y **Django REST Framework** proporciona una API REST robusta para la administración de la información clínica, mientras que el frontend construido con **React** y **Vite** ofrece una experiencia de usuario moderna, dinámica e intuitiva.

La estructura modular del proyecto facilita su mantenimiento, escalabilidad y la incorporación de nuevas funcionalidades, convirtiéndolo en una base sólida para el desarrollo de sistemas de gestión clínica.
