# Sistema de Gestión Educativa 🎓

Aplicación web para gestionar usuarios, cursos, notas y materias, desarrollada con Node.js, Express, MongoDB y Docker.

## Características principales ✨
- **Autenticación JWT**: Protección de rutas con tokens.
- **Roles de usuario**: Control de acceso (estudiantes, profesores, administradores).
- **CRUD completo**: Gestión de usuarios, cursos, notas y materias.
- **Plantillas Pug**: Interfaz dinámica con vistas para login, dashboard, cursos, etc.
- **Dockerizado**: Facilita el despliegue con contenedores.

## Prerrequisitos 📋
- Docker y Docker Compose instalados.
- Git (opcional, para clonar el repositorio).

## Instalación 🚀

### 1. Clonar el repositorio
```bash
git clone https://github.com/d2b74/Dynacord-devops.git
cd Dynacord-devops
```
### 2.Ejecutar el proyecto con Docker Compose
```bash
docker-compose up -d --build
```

### 3.Acceder a la aplicación

http://localhost:3000

## ⚠️ Importante: Configuración de finales de línea para `mongo-init/restore.sh` ⚠️

Es **muy importante** que el archivo `mongo-init/restore.sh` use finales de línea LF (no CRLF), para evitar problemas al ejecutar los scripts en entornos Linux o Docker.

### Cómo asegurarte de que `restore.sh` tenga finales de línea LF:

- **En VSCode**, abre `mongo-init/restore.sh`
- En la esquina inferior derecha, si ves `CRLF`, haz clic ahí
- Selecciona `LF`
- Guarda el archivo

Si usas otro editor, busca la opción para cambiar el fin de línea a LF.

---

Sin esta configuración, es posible que el script falle al correr dentro del contenedor Docker o en sistemas Unix.

