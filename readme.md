# Blog Project - Inicialización con Django y App `posts`

Proyecto web de Blog desarrollado con **Django**, estructurado con el proyecto principal `blog_project` en la raíz del repositorio y la aplicación modular `posts`.

## Estructura del Repositorio

```text
.
├── blog_project/          # Configuración principal del proyecto Django
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py        # Incluye 'posts.apps.PostsConfig', idioma 'es-ar' y zona horaria de Buenos Aires
│   ├── urls.py
│   └── wsgi.py
├── posts/                 # Aplicación encargada de gestionar las publicaciones del blog
│   ├── migrations/
│   │   └── __init__.py
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   └── views.py
├── .gitignore             # Excluye venv/, db.sqlite3 y archivos temporales (__pycache__)
├── manage.py              # Script de administración de Django en la raíz del proyecto
├── requirements.txt       # Dependencias del proyecto (Django)
└── README.md              # Documentación de instalación y puesta en marcha
```

## Requisitos Previos

- **Python 3.10+** instalado en el sistema.
- **Git** instalado para clonar el repositorio.

## Instalación y Ejecución Paso a Paso

1. **Clonar el repositorio** y acceder a la carpeta del proyecto:
   ```bash
   git clone <URL_DE_TU_REPOSITORIO>
   cd <NOMBRE_DE_TU_REPOSITORIO>
   ```

2. **Crear y activar el entorno virtual (`venv`)**:
   - En Windows (PowerShell / CMD):
     ```bash
     python -m venv venv
     venv\Scripts\activate
     ```
   - En Linux / macOS:
     ```bash
     python3 -m venv venv
     source venv/bin/activate
     ```

3. **Instalar las dependencias desde `requirements.txt`**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Aplicar las migraciones iniciales de la base de datos local**:
   ```bash
   python manage.py migrate
   ```

5. **Levantar el servidor de desarrollo**:
   ```bash
   python manage.py runserver
   ```
   Una vez iniciado, abrí tu navegador en `http://127.0.0.1:8000/` para verificar que el servidor de Django esté funcionando correctamente.
