# HydroTrack Seed

Proyecto semilla para el desarrollo de una plataforma de consulta, análisis y gestión de información relacionada con estaciones de servicio y combustibles.

---

## Descripción

HydroTrack Seed nace como parte de la Actividad 3 de la asignatura **Desarrollo de Aplicaciones en Red** del octavo semestre de la Ingeniaria en Sistemas Computacionales de la UNir y constituye el primer incremento funcional del proyecto transversal del grado.

El objetivo inicial consiste en desarrollar una aplicación web basada en componentes que permita consumir información desde una API REST pública, obtener la ubicación del usuario y ofrecer información de estaciones de servicio cercanas mediante una interfaz moderna desarrollada con React.

Este repositorio se conservará como punto de partida para futuras actividades académicas y posibles extensiones dentro del proyecto final del grado.

---

## Objetivos Iniciales

- Consumir datos desde una API REST.
- Procesar respuestas en formato JSON.
- Obtener la geolocalización del usuario.
- Mostrar estaciones de servicio cercanas.
- Filtrar resultados por empresa suministradora.
- Filtrar resultados por tipo de combustible.
- Aplicar desarrollo basado en componentes.
- Utilizar AJAX mediante Axios.

---

## Estado del Proyecto

### Fase 0 - Infraestructura

Completada.

Infraestructura base disponible:

- Bestia Escolar
- Docker
- Samba
- SSH
- VS Code Remote
- LAB-REACT-001
- React
- Vite
- Axios

Documentación:

```text
infra/
```

---

### Fase 1 - React

En desarrollo.

Objetivos:

- Componentes
- Props
- useState
- useEffect

---

### Fase 2 - AJAX

Pendiente.

Objetivos:

- Axios
- JSON
- Consumo de API REST

---

### Fase 3 - Geolocalización

Pendiente.

Objetivos:

- navigator.geolocation
- Ubicación del usuario

---

### Fase 4 - Integración API Gasolineras

Pendiente.

Objetivos:

- Consulta de estaciones
- Procesamiento de datos
- Filtrado
- Presentación de resultados

---

## Tecnologías

### Frontend

- React
- Vite
- JavaScript
- HTML5
- CSS3
- Axios

### Infraestructura

- Ubuntu Server
- Docker
- Samba
- SSH
- VS Code Remote

---

## Estructura del Proyecto

```text
hydrotrack-seed
│
├── infra
│   ├── README_INFRA.md
│   └── capturas
│
├── docs
│
├── memoria
│
├── capturas
│
├── backups
│
└── vite-project
    │
    ├── src
    ├── public
    ├── package.json
    └── vite.config.js
```

---

## Entorno de Desarrollo

Servidor:

```text
Bestia Escolar
```

Contenedor:

```text
LAB-REACT-001
```

Acceso:

```text
VS Code Remote SSH
```

Aplicación React:

```text
http://192.168.0.112:5173
```

---

## Historial

### Noviembre 2026

Se establece la infraestructura inicial del proyecto:

- Configuración de Bestia Escolar.
- Implementación de Samba para compartición de archivos.
- Implementación de Docker.
- Creación del contenedor LAB-REACT-001.
- Integración con VS Code Remote.
- Instalación y validación de React y Axios.

Este punto marca el inicio oficial del proyecto HydroTrack Seed.

---

## Próximo Hito

Implementar:

```text
Header
Buscador
Resultados
Footer
```

y realizar la primera consulta a una API REST utilizando Axios.

---

## Licencia

Proyecto académico utilizado para fines educativos dentro del programa de Ingeniería en Sistemas.