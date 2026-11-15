# Anexo E - Arquitectura Funcional

## Objetivo

Definir la arquitectura funcional de HydroTrack Seed utilizando una estructura basada en componentes, alineada con los objetivos académicos de la actividad y con los principios de reutilización, mantenimiento y escalabilidad establecidos para el proyecto.

La arquitectura presentada servirá como base para la implementación de la aplicación utilizando React.

---

# Relación con la Actividad

Uno de los objetivos principales de la actividad consiste en desarrollar la solución utilizando un enfoque basado en componentes.

Por este motivo, la arquitectura de HydroTrack Seed se encuentra organizada mediante componentes funcionales independientes, cada uno con responsabilidades claramente definidas.

Esta estructura facilita:

- Reutilización de código.
- Mantenimiento de la aplicación.
- Escalabilidad futura.
- Separación de responsabilidades.
- Cumplimiento de los objetivos académicos de la actividad.

---

# Arquitectura General

```text
App
│
├── Header
│
├── Buscador
│   ├── UbicaciónManual
│   ├── Geolocalización
│   ├── SelectorMarca
│   └── BotónBuscar
│
├── Filtros
│
├── Resultados
│   ├── ListaResultados
│   └── TarjetaGasolinera
│
└── Footer
```

---

# Descripción de Componentes

## App

### Función

Componente principal de la aplicación.

### Responsabilidades

- Coordinar el funcionamiento general.
- Gestionar el estado principal.
- Integrar todos los componentes.
- Controlar el flujo general de información.

---

## Header

### Función

Elemento identificador de la aplicación.

### Responsabilidades

- Mostrar el nombre del proyecto.
- Mostrar información descriptiva.
- Proporcionar identidad visual al sistema.

### Entradas

Ninguna.

### Salidas

Información visual para el usuario.

---

## Buscador

### Función

Capturar los parámetros necesarios para realizar las consultas.

### Responsabilidades

- Obtener ubicación.
- Capturar criterios de búsqueda.
- Iniciar consultas.

### Entradas

Información proporcionada por el usuario.

### Salidas

Parámetros de búsqueda.

---

## Ubicación Manual

### Función

Permitir introducir una ubicación manualmente.

### Responsabilidades

- Capturar una ubicación alternativa.
- Validar datos ingresados.

### Entradas

Texto proporcionado por el usuario.

### Salidas

Ubicación seleccionada.

---

## Geolocalización

### Función

Obtener la posición actual del usuario.

### Responsabilidades

- Solicitar permisos.
- Obtener coordenadas.
- Notificar errores de acceso.

### Entradas

Permiso del navegador.

### Salidas

Latitud y longitud.

---

## SelectorMarca

### Función

Permitir seleccionar una marca específica.

### Responsabilidades

- Mostrar marcas disponibles.
- Capturar selección del usuario.

### Entradas

Listado de marcas.

### Salidas

Marca seleccionada.

---

## BotónBuscar

### Función

Iniciar el proceso de búsqueda.

### Responsabilidades

- Validar parámetros.
- Disparar consulta.

### Entradas

Datos del formulario.

### Salidas

Solicitud de búsqueda.

---

## Filtros

### Función

Refinar los resultados obtenidos.

### Responsabilidades

- Filtrar por marca.
- Filtrar por precio.
- Filtrar por distancia.
- Filtrar por combustible.

### Entradas

Resultados obtenidos.

### Salidas

Resultados filtrados.

---

## Resultados

### Función

Presentar la información obtenida.

### Responsabilidades

- Organizar resultados.
- Coordinar la presentación de estaciones.

### Entradas

Información procesada.

### Salidas

Visualización para el usuario.

---

## ListaResultados

### Función

Contener el conjunto de estaciones obtenidas.

### Responsabilidades

- Gestionar colecciones de resultados.
- Generar elementos individuales.

### Entradas

Listado de estaciones.

### Salidas

Tarjetas de estaciones.

---

## TarjetaGasolinera

### Función

Representar una estación individual.

### Responsabilidades

- Mostrar nombre.
- Mostrar dirección.
- Mostrar precios.
- Mostrar distancia.
- Mostrar información adicional.

### Entradas

Información de una estación.

### Salidas

Visualización estructurada.

---

## Footer

### Función

Mostrar información complementaria.

### Responsabilidades

- Identificación académica.
- Información técnica.
- Referencias generales.

### Entradas

Ninguna.

### Salidas

Información visual.

---

# Flujo de Comunicación entre Componentes

```text
Usuario
    │
    ▼
Buscador
    │
    ▼
App
    │
    ▼
Consulta API
    │
    ▼
Procesamiento
    │
    ▼
Resultados
    │
    ▼
ListaResultados
    │
    ▼
TarjetaGasolinera
```

---

# Estado de los Componentes

## MVP

Componentes obligatorios:

- App
- Header
- Buscador
- Geolocalización
- Ubicación Manual
- Resultados
- ListaResultados
- TarjetaGasolinera
- Footer

---

## Incremento 1

- Filtros
- SelectorMarca
- Cálculo de distancia
- Estación más económica

---

## Futuras Iteraciones

- White List
- Black List
- Historial
- Sistema de recomendaciones
- Preferencias de usuario

---

# Principios Arquitectónicos

## Separación de Responsabilidades

Cada componente deberá tener una responsabilidad claramente definida.

---

## Reutilización

Los componentes deberán diseñarse para facilitar su reutilización en futuras iteraciones.

---

## Accesibilidad

Todos los componentes deberán cumplir criterios WCAG nivel AA.

---

## Escalabilidad

La arquitectura deberá permitir incorporar nuevas funcionalidades sin modificar significativamente los componentes existentes.

---

## Mantenibilidad

La estructura deberá facilitar correcciones, pruebas y evolución del sistema.

---

# Relación con Otros Anexos

| Documento | Relación |
|------------|-----------|
| Resumen Ejecutivo | Define la visión general |
| Anexo A | Define el alcance y MVP |
| Anexo B | Define dependencias y riesgos |
| Anexo C | Define historias de usuario y flujos |
| Anexo D | Define tecnologías utilizadas |

---

# Criterio de Aceptación del Anexo

El anexo se considerará completado cuando:

✅ Todos los componentes principales estén identificados.

✅ Exista una responsabilidad claramente definida para cada componente.

✅ La arquitectura permita implementar las historias de usuario del Anexo C.

✅ La arquitectura permita construir el MVP definido en el Anexo A.

✅ La estructura sea compatible con React y desarrollo basado en componentes.

---

# Estado del Documento

**Versión:** 1.0

**Estado:** Aprobado

**Proyecto:** HydroTrack Seed

**Clasificación:** Anexo E