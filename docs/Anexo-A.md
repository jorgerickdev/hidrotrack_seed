# Anexo A - Alcance y MVP

## Objetivo

Definir claramente los límites de la primera iteración del proyecto HydroTrack Seed, identificando qué funcionalidades serán implementadas durante la Actividad 3 y cuáles formarán parte de futuras etapas del proyecto transversal.

---

# Alcance del Proyecto

La primera iteración de HydroTrack Seed tiene como propósito construir una aplicación web capaz de obtener, procesar y mostrar información pública relacionada con estaciones de servicio utilizando una API oficial como fuente de datos.

El sistema deberá permitir la consulta de información relevante por parte del usuario utilizando una interfaz basada en componentes que siga principios modernos de desarrollo web y accesibilidad.

La aplicación se desarrollará como una Single Page Application (SPA), ejecutándose íntegramente en el navegador y consumiendo información desde servicios externos mediante peticiones HTTP.

---

# Funcionalidades Incluidas

Las siguientes funcionalidades forman parte del alcance aprobado para esta iteración.

## Consulta de Datos

- Obtención de información desde una API pública.
- Soporte para procesamiento de datos en formato JSON.
- Integración de información externa en la aplicación.

## Interfaz de Usuario

- Aplicación de página única.
- Interfaz basada en componentes React.
- Visualización estructurada de la información.
- Actualización dinámica del contenido sin recarga completa de la página.

## Geolocalización

- Obtención automática de la ubicación del usuario.
- Uso de la ubicación como criterio de búsqueda.

## Ubicación Manual

- Introducción manual de una ubicación.
- Búsquedas alternativas cuando la geolocalización no esté disponible.
- Soporte para simulación de consultas desde ubicaciones diferentes.

## Resultados

- Presentación de estaciones de servicio.
- Visualización de precios.
- Visualización de dirección.
- Visualización de información relevante recibida desde la API.

## Filtrado

- Filtrado por marca.
- Filtrado por criterios definidos durante el desarrollo.

## Accesibilidad

- Cumplimiento de criterios WCAG nivel AA.
- Navegación mediante teclado.
- Etiquetado semántico adecuado.
- Formularios accesibles.

## Control de Versiones

- Uso de Git.
- Registro de cambios mediante commits.
- Publicación del código en repositorio remoto.

---

# Funcionalidades Opcionales

Las siguientes funcionalidades aportan valor al proyecto y podrán implementarse en función del tiempo disponible.

- Identificación de la estación más cercana.
- Identificación de la estación más económica.
- Búsqueda dentro de un radio determinado.
- Visualización de horarios.
- Aplicación de descuentos por fidelización.
- Estaciones en ruta.

Estas funcionalidades no condicionan la viabilidad básica del proyecto, pero aumentan su valor funcional y académico.

---

# Fuera de Alcance

Las funcionalidades siguientes no forman parte de esta iteración.

## Gestión de Usuarios

- Registro.
- Inicio de sesión.
- Recuperación de contraseñas.
- Gestión de perfiles.

## Persistencia Local

- Bases de datos propias.
- Almacenamiento permanente de consultas.
- Históricos de usuario.

## Gestión Empresarial

- Administración de estaciones.
- Modificación de precios.
- Gestión de inventarios.
- Operaciones comerciales.

## Aplicaciones Móviles

- Aplicación Android.
- Aplicación iOS.

## Integraciones Avanzadas

- Pasarelas de pago.
- Sistemas de facturación.
- Integraciones ERP.
- Integraciones empresariales externas.

---

# Definición de MVP

## Producto Mínimo Viable

El proyecto se considerará funcional y apto para evaluación cuando pueda demostrar correctamente las siguientes capacidades:

### Obtención de Información

- Consumir datos desde la API seleccionada.
- Procesar respuestas correctamente.

### Ubicación

- Obtener ubicación automática.
- Permitir ubicación manual.

### Presentación

- Mostrar estaciones obtenidas.
- Mostrar información relevante al usuario.

### Filtrado

- Aplicar al menos un criterio de filtrado funcional.

### Arquitectura

- Implementación mediante componentes React.

### Accesibilidad

- Cumplimiento de nivel AA en los elementos desarrollados.

### Documentación

- Memoria PDF.
- Repositorio Git.
- Evidencias de funcionamiento.

---

# Criterio de Finalización

La iteración será considerada completada cuando:

✅ Todos los criterios de aceptación definidos en el documento principal se encuentren satisfechos.

✅ El MVP sea demostrable.

✅ La aplicación pueda ejecutarse sin errores críticos.

✅ La documentación requerida esté completada.

✅ El repositorio se encuentre actualizado y accesible.

---

# Estado del Documento

Versión: 1.0

Estado: Aprobado 13 Noviembre 2026

Proyecto: HydroTrack Seed

Clasificación: Anexo A