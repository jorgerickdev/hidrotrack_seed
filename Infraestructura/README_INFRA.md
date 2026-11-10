# Cyber10-27
# LAB-REACT-001
## Infraestructura de Desarrollo React para Actividad 3

**Proyecto:** Cyber10-27  
**Laboratorio:** LAB-REACT-001  
**Fecha:** Noviembre 2026  
**Estado:** Operativo  

---

# Introducción

LAB-REACT-001 forma parte de la infraestructura académica del proyecto **Cyber10-27**, un entorno de aprendizaje con fecha objetivo de finalización en octubre de 2027.

El propósito de este laboratorio es proporcionar una plataforma aislada para el desarrollo de aplicaciones React sin instalar herramientas de desarrollo directamente en la estación principal de trabajo.

La infraestructura permite desarrollar, ejecutar y probar aplicaciones web modernas utilizando React, Node.js y Axios dentro de contenedores Docker ejecutados sobre la Bestia Escolar.

---

# ¿Qué es Cyber10-27?

Cyber10-27 es un proyecto personal de aprendizaje orientado al desarrollo progresivo de competencias en:

```text
Infraestructura
Linux
Windows Server
Docker
Programación
Desarrollo Web
Minería de Datos
Bases de Datos
Ciberseguridad
```

El nombre del proyecto proviene de:

```text
10 = Octubre
27 = Año 2027
```

fecha establecida para alcanzar los objetivos generales de formación.

---

# ¿Qué es la Bestia Escolar?

La Bestia Escolar es un servidor Ubuntu Server dedicado exclusivamente a:

```text
Prácticas académicas
Programación
Aprendizaje
Laboratorios
Minería de Datos
React
PHP
Python
```

Su función es evitar que las actividades de aprendizaje afecten la infraestructura empresarial del proyecto.

---

# Separación de Infraestructura

Cyber10-27 está dividido en dos grandes áreas.

## Carril Empresarial

```text
Windows Server
Active Directory
DNS
La Bestia (Debian)
Infraestructura empresarial
Servicios Linux
```

Objetivo:

```text
Simular un entorno profesional.
```

---

## Carril Académico

```text
Bestia Escolar
Docker
React
PHP
Python
Laravel
Jupyter
Prácticas universitarias
```

Objetivo:

```text
Aprender y experimentar sin comprometer
la estabilidad del entorno empresarial.
```

---

# Arquitectura General

```text
┌────────────────────────────────────────────┐
│                VICTUS                      │
│                Pop!_OS                     │
├────────────────────────────────────────────┤
│ VS Code                                    │
│ Firefox                                    │
│ CherryTree                                 │
│ Remote SSH                                 │
│ SSHFS                                      │
└────────────────────────────────────────────┘
                    │
                    │ SSH
                    ▼
┌────────────────────────────────────────────┐
│            BESTIA ESCOLAR                  │
│             Ubuntu Server                  │
│            192.168.0.112                   │
├────────────────────────────────────────────┤
│ Docker                                     │
│ Docker Compose                             │
│ Desarrollo                                 │
└────────────────────────────────────────────┘
                    │
                    ▼
┌────────────────────────────────────────────┐
│              LAB-REACT-001                 │
├────────────────────────────────────────────┤
│ Node.js                                    │
│ npm                                        │
│ React                                      │
│ Vite                                       │
│ Axios                                      │
└────────────────────────────────────────────┘
                    │
                    ▼
┌────────────────────────────────────────────┐
│               Firefox                      │
│      http://192.168.0.112:5173             │
└────────────────────────────────────────────┘
```

---

# Diagrama de Red

```text
                           INTERNET
                               │
                               ▼
                    Router Principal Casa
                               │
        ┌──────────────────────┴──────────────────────┐
        │                                             │
        ▼                                             ▼

     Red Casa                                Red Cyber10-27
                                               192.168.0.0/24
                                                      │
                                                      ▼
                                              Router Cyber10-27
                                                      │
             ┌────────────────────────────────────────┼────────────────────────────────────────┐
             │                                        │                                        │
             ▼                                        ▼                                        ▼

         Victus                                 Bestia Escolar                         Windows Server
      192.168.0.x                             192.168.0.112                           192.168.0.x
```

---

# Puertos Utilizados

| Servicio | Puerto | Uso |
|----------|---------|------|
| SSH | 22 | Administración remota |
| Jupyter Lab | 8888 | LAB-AAMD-001 |
| PHP | 8080 | LAB-PHP-001 |
| phpMyAdmin | 8081 | Administración MariaDB |
| React + Vite | 5173 | LAB-REACT-001 |
| MariaDB | 3306 | Base de datos |

---

# Infraestructura

## Carpeta de Infraestructura

```text
~/contenedores/lab-react-001
```

Contenido:

```text
Dockerfile
docker-compose.yml
.env
docs
capturas
memoria
backups
```

---

# Desarrollo

Ubicación:

```text
~/Desarrollo/react
```

---

# Dockerfile

```dockerfile
FROM node:22-alpine

WORKDIR /workspace

CMD ["sh"]
```

---

# Docker Compose

```yaml
services:

  react:

    build: .

    container_name: lab-react-001

    working_dir: /workspace

    volumes:
      - /home/rick-server/Desarrollo/react:/workspace

    ports:
      - "5173:5173"

    stdin_open: true

    tty: true

    restart: unless-stopped
```

---

# Herramientas Instaladas

Dentro del laboratorio:

```text
✅ Node.js
✅ npm
✅ React
✅ Vite
✅ Axios
✅ Git
```

---

# Creación del Proyecto React

Ejecutado desde el contenedor:

```bash
npm create vite@latest .
```

Configuración:

```text
Framework:
React

Variant:
JavaScript

Lint:
ESLint
```

---

# Axios

Instalación:

```bash
npm install axios
```

Resultado:

```text
Axios disponible para peticiones AJAX.
```

---

# Estructura del Proyecto

```text
react

└── vite-project

    ├── public
    ├── src
    │
    ├── docs
    ├── capturas
    ├── memoria
    ├── backups
    │
    ├── package.json
    ├── package-lock.json
    └── vite.config.js
```

---

# Integración con VS Code

Flujo validado:

```text
VS Code

↓

Remote SSH

↓

Bestia Escolar

↓

Attach to Running Container

↓

lab-react-001
```

Resultado:

```text
✅ Desarrollo remoto operativo.
```

---

# Validación

Archivo:

```text
src/App.jsx
```

Contenido de prueba:

```jsx
function App() {
  return (
    <>
      <h1>🚀 LAB-REACT-001</h1>
      <p>React funcionando correctamente.</p>
      <p>Cyber10-27</p>
    </>
  )
}

export default App
```

Resultado:

```text
🚀 LAB-REACT-001

React funcionando correctamente.

Cyber10-27
```

---

# Flujo de Trabajo

## Inicio

```bash
ssh rick-server@192.168.0.112
```

```bash
cd ~/contenedores/lab-react-001

docker compose up -d
```

```bash
montar_carpeta
```

Abrir VS Code.

Conectar:

```text
Remote SSH
↓
Bestia Escolar
↓
Attach to Running Container
↓
lab-react-001
```

Abrir:

```text
/workspace/react/vite-project
```

---

## Desarrollo

Modificar:

```text
src/App.jsx
```

Guardar.

Hot Reload:

```text
Automático
```

---

## Finalización

```text
Ctrl + C
```

```bash
docker compose down
```

```bash
desmontar_carpeta
```

Cerrar SSH.

---

# Aplicación Académica

Este laboratorio será utilizado para desarrollar la Actividad 3:

```text
React
AJAX (Axios)
API REST
Geolocalización
Procesamiento JSON
Interfaz de usuario
```

orientada al sistema de consulta de gasolineras.

---

# Estado Final

```text
LAB-REACT-001

✅ Docker
✅ Node.js
✅ npm
✅ React
✅ Vite
✅ Axios
✅ VS Code Remote
✅ Dev Container
✅ Puerto 5173 publicado
✅ Hot Reload
✅ Desarrollo remoto
✅ Proyecto React validado
✅ Listo para Actividad 3
```

---

# Conclusión

LAB-REACT-001 proporciona una plataforma completa para el desarrollo de aplicaciones React dentro del ecosistema Cyber10-27.

La infraestructura permite trabajar desde la Victus utilizando Visual Studio Code mientras la ejecución real ocurre dentro de la Bestia Escolar mediante Docker, manteniendo la estación principal limpia y reduciendo la complejidad de administración.

Con este laboratorio operativo, el equipo puede comenzar inmediatamente el desarrollo de componentes React, llamadas AJAX mediante Axios y consumo de API REST, utilizando una infraestructura reproducible y alineada con los objetivos del proyecto Cyber10-27.