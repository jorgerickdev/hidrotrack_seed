# Anexo D - Tecnologías Utilizadas y Justificación Técnica

## Objetivo

Documentar las tecnologías seleccionadas para el desarrollo de HydroTrack Seed y justificar su utilización en función de los objetivos académicos, funcionales y operativos del proyecto.

---

# Criterios de Selección Tecnológica

La selección de tecnologías se realizó considerando los siguientes criterios:

- Alineación con los objetivos de la actividad.
- Facilidad de aprendizaje y mantenimiento.
- Compatibilidad con el entorno de desarrollo.
- Reproducibilidad del entorno de trabajo.
- Separación entre desarrollo e infraestructura.
- Posibilidad de evolución futura del proyecto.
- Validación temprana del funcionamiento en un entorno servidor.

---

# Principios Tecnológicos del Proyecto

Las decisiones tecnológicas adoptadas para HydroTrack Seed se fundamentan en los siguientes principios.

## PT-01 Separación de Entornos

Mantener el sistema operativo anfitrión libre de dependencias académicas temporales.

Las herramientas, librerías y entornos de ejecución requeridos por el proyecto serán alojados en una infraestructura independiente.

---

## PT-02 Entorno Centralizado

Centralizar el desarrollo sobre una única plataforma de trabajo.

Esto permite disponer de una ubicación única para código, documentación, configuración y pruebas.

---

## PT-03 Validación en Entorno Real

Desarrollar y validar la aplicación directamente sobre un servidor Ubuntu Server para reducir las diferencias entre el entorno de desarrollo y el entorno final de ejecución.

De esta forma, el comportamiento de la aplicación puede verificarse continuamente sin necesidad de realizar suposiciones acerca de su funcionamiento una vez desplegada.

---

## PT-04 Reproducibilidad

Garantizar que el entorno de desarrollo pueda reconstruirse de forma consistente mediante el uso de contenedores y documentación técnica.

---

## PT-05 Alineación Académica

Utilizar tecnologías que permitan cumplir directamente los objetivos de aprendizaje de la actividad.

---

## PT-06 Evolución del Proyecto

Seleccionar tecnologías que permitan extender el sistema durante futuras iteraciones del proyecto transversal sin necesidad de rediseños significativos.

---

# Tecnologías de Aplicación

## React

### Función

Framework utilizado para la construcción de la interfaz de usuario.

### Justificación

React permite implementar una arquitectura basada en componentes reutilizables, requisito alineado con los objetivos de la actividad.

Su modelo de componentes facilita la separación de responsabilidades, mejora la mantenibilidad del código y simplifica la incorporación de nuevas funcionalidades en futuras iteraciones.

### Aplicación en el Proyecto

- Header.
- Buscador.
- Resultados.
- Filtros.
- Footer.

---

## Vite

### Función

Entorno de construcción y servidor de desarrollo para aplicaciones React.

### Justificación

Permite disponer de un entorno de desarrollo moderno, ligero y de rápida ejecución.

Facilita el desarrollo iterativo y reduce los tiempos de espera durante la construcción y prueba de la aplicación.

### Aplicación en el Proyecto

- Inicialización del proyecto.
- Ejecución local.
- Construcción de versiones de prueba.

---

## Axios

### Función

Biblioteca para la realización de peticiones HTTP.

### Justificación

La actividad requiere el consumo de una API externa.

Axios simplifica la comunicación con servicios REST y proporciona una interfaz clara para el tratamiento de respuestas y errores.

### Aplicación en el Proyecto

- Consulta de datos públicos.
- Procesamiento de respuestas JSON.
- Gestión de errores de comunicación.

---

# Tecnologías de Desarrollo

## Git

### Función

Sistema de control de versiones.

### Justificación

Permite registrar la evolución del desarrollo, mantener un historial de cambios y gestionar versiones del proyecto.

### Aplicación en el Proyecto

- Seguimiento de cambios.
- Construcción del historial de desarrollo.
- Soporte para la bitácora del proyecto.

---

## GitHub

### Función

Repositorio remoto del proyecto.

### Justificación

Permite centralizar el código fuente y la documentación.

Proporciona una copia de respaldo permanente y facilita la trazabilidad del desarrollo.

### Aplicación en el Proyecto

- Almacenamiento del repositorio.
- Gestión de versiones.
- Publicación del proyecto.

---

# Tecnologías de Infraestructura

## Bestia Escolar

### Función

Servidor principal de desarrollo del proyecto.

### Descripción

Servidor de desarrollo basado en Ubuntu Server 26.04 utilizado como plataforma principal para la construcción del proyecto HydroTrack Seed.

Su propósito es proporcionar un entorno centralizado para el desarrollo, pruebas y validación del proyecto antes de su despliegue final.

### Servicios Utilizados

- Docker.
- Samba.
- SSH.
- Visual Studio Code Remote.

### Justificación

Permite ejecutar y verificar directamente el comportamiento de la aplicación en un entorno servidor real durante todo el ciclo de desarrollo.

---

## Docker

### Función

Plataforma de contenedores.

### Justificación

Permite aislar el entorno de desarrollo y garantizar que el proyecto pueda ejecutarse de manera consistente independientemente del sistema anfitrión.

### Aplicación en el Proyecto

- Contenedor LAB-REACT-001.
- Gestión de dependencias.
- Reproducción del entorno de trabajo.

---

## Samba

### Función

Compartición de archivos entre sistemas.

### Justificación

Permite acceder a los recursos alojados en la Bestia Escolar desde el entorno de trabajo principal sin necesidad de duplicar información.

### Aplicación en el Proyecto

- Intercambio de archivos.
- Gestión documental.
- Acceso al repositorio de trabajo.

---

## Visual Studio Code Remote SSH

### Función

Desarrollo remoto.

### Justificación

Permite editar y ejecutar código directamente sobre la infraestructura de desarrollo manteniendo una experiencia integrada para el usuario.

### Aplicación en el Proyecto

- Desarrollo remoto.
- Gestión del código fuente.
- Integración con contenedores.

---

# Tecnologías Evaluadas y No Utilizadas

## Bases de Datos

No se incorporan bases de datos en la primera iteración debido a que la información se obtiene dinámicamente desde una API externa.

---

## Aplicaciones Móviles

Se descartan para esta fase debido a que el alcance del proyecto contempla únicamente una aplicación web.

---

## Frameworks Alternativos

No se consideran otros frameworks frontend debido a que React satisface los requisitos académicos y técnicos definidos para la actividad.

---

# Arquitectura Tecnológica Resultante

```text
Usuario
    │
    ▼
React
    │
    ▼
Axios
    │
    ▼
API Pública
    │
    ▼
JSON
    │
    ▼
Procesamiento
    │
    ▼
Resultados
```

Infraestructura de soporte:

```text
Bestia Escolar
│
├── Ubuntu Server 26.04
├── Docker
├── Samba
├── SSH
└── VS Code Remote
```

---

# Relación con los Objetivos Académicos

| Objetivo | Tecnología |
|-----------|------------|
| Desarrollo por componentes | React |
| Consumo de API | Axios |
| Procesamiento JSON | Axios + JavaScript |
| Aplicación Web | React + Vite |
| Control de versiones | Git |
| Infraestructura reproducible | Docker |
| Entorno servidor real | Bestia Escolar |

---

# Criterio de Aceptación del Anexo

El anexo se considerará completado cuando:

✅ Todas las tecnologías utilizadas estén identificadas.

✅ Exista una justificación para cada tecnología seleccionada.

✅ Se documente la infraestructura empleada.

✅ Exista relación entre las tecnologías y los objetivos del proyecto.

✅ La arquitectura tecnológica general se encuentre definida.

---

# Estado del Documento

**Versión:** 1.0

**Estado:** Aprobado

**Proyecto:** HydroTrack Seed

**Clasificación:** Anexo D