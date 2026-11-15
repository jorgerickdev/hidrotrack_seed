# Anexo B - Riesgos, Dependencias y Supuestos

## Objetivo

Identificar los factores internos y externos que pueden afectar el desarrollo de HydroTrack Seed, documentar los elementos necesarios para su construcción y establecer las condiciones asumidas durante la planificación del proyecto.

---

# Riesgos del Proyecto

## R-01 Disponibilidad de la API

### Descripción

La aplicación depende de una fuente de datos externa administrada por terceros.

### Impacto

Alto.

### Consecuencia

La aplicación no podrá obtener información actualizada si el servicio no se encuentra disponible.

### Mitigación

- Diseñar el sistema para detectar errores de conexión.
- Informar al usuario cuando los datos no estén disponibles.
- Utilizar datos de prueba durante el desarrollo.

---

## R-02 Cambios en la Estructura de los Datos

### Descripción

La API puede modificar el formato de respuesta sin previo aviso.

### Impacto

Alto.

### Consecuencia

El procesamiento de datos podría dejar de funcionar correctamente.

### Mitigación

- Mantener el código desacoplado del formato específico.
- Validar los datos recibidos antes de procesarlos.
- Centralizar el procesamiento de respuestas.

---

## R-03 Restricciones de Geolocalización

### Descripción

El usuario puede negar permisos de ubicación al navegador o el dispositivo puede no disponer de geolocalización.

### Impacto

Medio.

### Consecuencia

No será posible obtener automáticamente la posición actual.

### Mitigación

- Proporcionar entrada manual de ubicación.
- Diseñar la aplicación para funcionar sin geolocalización.

---

## R-04 Limitaciones de Tiempo

### Descripción

El proyecto posee una fecha límite académica definida.

### Impacto

Alto.

### Consecuencia

Algunas funcionalidades de valor añadido podrían quedar fuera de la primera versión.

### Mitigación

- Priorizar el MVP.
- Desarrollar mediante incrementos funcionales.
- Mantener una lista diferenciada entre funcionalidades obligatorias y opcionales.

---

## R-05 Accesibilidad

### Descripción

El cumplimiento de criterios WCAG nivel AA requiere validaciones adicionales durante el desarrollo.

### Impacto

Medio.

### Consecuencia

Podrían ser necesarias modificaciones sobre componentes ya desarrollados.

### Mitigación

- Aplicar accesibilidad desde la fase de diseño.
- Revisar cada componente antes de considerarlo terminado.
- Utilizar HTML semántico desde la primera implementación.

---

# Dependencias Externas

Las siguientes dependencias son administradas por terceros y no se encuentran bajo control directo del proyecto.

## Fuente de Datos

- Portal de Datos Abiertos del Gobierno de España.
- Servicio público de precios de carburantes.

## Navegador

- Soporte para JavaScript moderno.
- Soporte para peticiones HTTP.
- Soporte para geolocalización.
- Soporte para HTML5 y CSS3.

## Conectividad

- Acceso a Internet para consultar los servicios externos.
- Disponibilidad de la API durante el período de desarrollo.

---

# Dependencias de Desarrollo

Las siguientes dependencias forman parte del entorno de construcción del proyecto.

## Infraestructura de Desarrollo

### Bestia Escolar

Servidor de desarrollo basado en Ubuntu Server 26.04 utilizado como plataforma principal para la construcción del proyecto HydroTrack Seed.

Su propósito es proporcionar un entorno centralizado para el desarrollo, pruebas y validación del proyecto antes de su despliegue final.

Permite ejecutar y verificar directamente el comportamiento de la aplicación en un entorno servidor real durante todo el ciclo de desarrollo.Servidor de desarrollo basado en Ubuntu Server 26.04 utilizado como plataforma principal para la construcción del proyecto HydroTrack Seed.

### Funciones Principales

- Ejecución del entorno de desarrollo.
- Hospedaje de contenedores Docker.
- Almacenamiento centralizado del código fuente.
- Acceso remoto mediante SSH.
- Compartición de recursos mediante Samba.
- Integración con Visual Studio Code mediante Remote SSH.
- Soporte para pruebas y ejecución de aplicaciones durante el desarrollo.

La Bestia Escolar constituye la infraestructura principal del proyecto durante la fase académica y proporciona un entorno controlado, reproducible y aislado para el desarrollo de software.

### Justificación

La utilización de un servidor dedicado permite separar el entorno de desarrollo del sistema operativo principal, favoreciendo la reproducibilidad, la organización del proyecto y la administración centralizada de herramientas y dependencias.

### Servicios de Apoyo

- Docker.
- Samba.
- SSH.
- Visual Studio Code Remote.

---

## Frameworks y Librerías

- React.
- Vite.
- Axios.

---

## Gestión del Proyecto

- Git.
- GitHub.

---

## Documentación

- Resumen Ejecutivo.
- Anexos.
- Bitácora de Desarrollo.
- Memoria Técnica.

---

# Supuestos del Proyecto

Durante la planificación se asumen las siguientes condiciones.

## S-01

La API pública continuará disponible durante el período de desarrollo.

## S-02

La información pública podrá ser reutilizada de acuerdo con las condiciones establecidas por el proveedor de los datos.

## S-03

El navegador utilizado dispondrá de soporte para JavaScript moderno y geolocalización.

## S-04

La infraestructura de desarrollo permanecerá operativa durante todo el proyecto.

## S-05

El repositorio Git permanecerá disponible para el almacenamiento y seguimiento del código.

## S-06

El desarrollo será realizado por una sola persona utilizando una metodología ágil adaptada a proyectos individuales.

---

# Estrategia General de Gestión de Riesgos

La gestión de riesgos se realizará mediante:

- Desarrollo incremental.
- Entregables verificables.
- Documentación continua.
- Control de versiones.
- Revisiones periódicas.
- Priorización del MVP.

---

# Criterio de Aceptación del Anexo

El anexo se considerará completado cuando:

✅ Los riesgos principales del proyecto estén identificados.

✅ Las dependencias externas y de desarrollo estén documentadas.

✅ Los supuestos utilizados para la planificación estén definidos.

✅ Exista una estrategia básica de mitigación para los riesgos de mayor impacto.

---

# Estado del Documento

**Versión:** 1.0

**Estado:** Aprobado

**Proyecto:** HydroTrack Seed

**Clasificación:** Anexo B