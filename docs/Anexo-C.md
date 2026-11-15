# Anexo C - Mapa de Trabajo y Flujo Funcional

## Objetivo

Definir las necesidades del usuario, los servicios que proporcionará la aplicación y la forma en que dichos servicios serán soportados por el sistema durante la primera iteración de HydroTrack Seed.

Este documento representa la transición entre los requerimientos funcionales y el diseño técnico de la solución.

---

# Priorización de Historias

Las historias de usuario se clasifican en tres niveles de prioridad.

## MVP

Funcionalidades mínimas necesarias para considerar la aplicación operativa y apta para evaluación.

## Incremento 1

Funcionalidades de valor añadido que mejoran la experiencia del usuario y aumentan la utilidad práctica de la aplicación.

## Futuras Iteraciones

Funcionalidades previstas para la evolución del proyecto transversal y que no forman parte de la primera iteración.

---

# Historias de Usuario

## HU-01 Consulta de Estaciones Cercanas

**Prioridad:** MVP

Como usuario

Quiero localizar estaciones de servicio cercanas a mi ubicación

Para poder decidir dónde abastecer combustible.

---

## HU-02 Consulta Mediante Ubicación Manual

**Prioridad:** MVP

Como usuario

Quiero introducir manualmente una ubicación

Para consultar estaciones desde una zona distinta a mi posición actual.

---

## HU-03 Consulta de Precios

**Prioridad:** MVP

Como usuario

Quiero visualizar los precios disponibles en cada estación

Para comparar opciones y elegir la más conveniente.

---

## HU-04 Filtrado por Marca

**Prioridad:** MVP

Como usuario

Quiero filtrar resultados por marca

Para localizar estaciones pertenecientes a una empresa específica.

---

## HU-05 Visualización de Resultados

**Prioridad:** MVP

Como usuario

Quiero visualizar la información obtenida de forma clara y estructurada

Para comprender rápidamente los resultados de mi búsqueda.

---

## HU-06 Consulta de Horarios

**Prioridad:** Incremento 1

Como usuario

Quiero visualizar los horarios de servicio

Para saber si una estación se encuentra disponible.

---

## HU-07 Consulta de Estación Más Económica

**Prioridad:** Incremento 1

Como usuario

Quiero identificar la estación más económica

Para reducir mis gastos de combustible.

---

## HU-08 Consulta de Estaciones en Ruta

**Prioridad:** Incremento 1

Como usuario

Quiero identificar estaciones localizadas dentro de mi trayecto

Para evitar desplazamientos innecesarios.

---

## HU-09 Consulta de Estaciones Recomendadas

**Prioridad:** Futura Iteración

Como usuario

Quiero visualizar estaciones consideradas confiables

Para identificar rápidamente opciones recomendables.

---

## HU-10 Gestión de Lista Blanca

**Prioridad:** Futura Iteración

Como usuario

Quiero registrar estaciones favoritas

Para disponer de una lista personal de referencia.

---

## HU-11 Consulta de Lista Blanca

**Prioridad:** Futura Iteración

Como usuario

Quiero consultar únicamente mis estaciones favoritas

Para acceder rápidamente a mis opciones habituales.

---

## HU-12 Gestión de Lista Negra

**Prioridad:** Futura Iteración

Como usuario

Quiero marcar estaciones que deseo evitar

Para excluirlas de mis búsquedas habituales.

---

## HU-13 Exclusión de Estaciones No Deseadas

**Prioridad:** Futura Iteración

Como usuario

Quiero ocultar estaciones registradas en mi lista negra

Para mejorar la calidad de los resultados obtenidos.

---
## HU-14 Acceso Universal a la Información

**Prioridad:** MVP

Como usuario

Quiero poder utilizar la aplicación mediante mecanismos accesibles

Para acceder a la información independientemente de mis capacidades o del dispositivo utilizado.

---

## HU-15 Identificación de la Estación Más Cercana

**Prioridad:** Incremento 1

Como usuario

Quiero conocer cuál es la estación más cercana a mi ubicación

Para reducir el tiempo de desplazamiento.

---

### Criterios Asociados

- Navegación mediante teclado.
- Formularios etiquetados.
- Uso de HTML semántico.
- Compatibilidad con tecnologías de asistencia.
- Cumplimiento de WCAG nivel AA.

# Casos de Uso

## CU-01 Obtener Ubicación

Obtención automática de coordenadas mediante los servicios de geolocalización del navegador.

---

## CU-02 Introducir Ubicación Manual

Captura manual de una ubicación proporcionada por el usuario.

---

## CU-03 Consultar Estaciones

Obtención de datos desde la API pública seleccionada.

---

## CU-04 Consultar Precios

Procesamiento y visualización de precios disponibles en estaciones de servicio.

---

## CU-05 Aplicar Filtros

Filtrado dinámico de resultados según los criterios seleccionados.

---

## CU-06 Visualizar Resultados

Presentación estructurada de la información obtenida.

---

# Flujo del Usuario

```text
Usuario
    │
    ├── Permitir geolocalización
    │
    └── Introducir ubicación manual
            │
            ▼
      Solicitar búsqueda
            │
            ▼
      Aplicar filtros
            │
            ▼
      Revisar resultados
            │
            ▼
      Seleccionar estación
            │
            ▼
      Tomar decisión
```

---

# Flujo Funcional del Sistema

```text
Interfaz React
    │
    ▼
Captura de parámetros
    │
    ▼
Validación
    │
    ▼
Axios
    │
    ▼
API Oficial
    │
    ▼
Respuesta JSON
    │
    ▼
Procesamiento
    │
    ▼
Filtrado
    │
    ▼
Presentación
```

---

# Flujo de Procesamiento

```text
Recepción de datos
    │
    ▼
Validación
    │
    ▼
Normalización
    │
    ▼
Extracción de información
    │
    ▼
Aplicación de reglas
    │
    ▼
Generación de resultados
```

---

# Flujo de Desarrollo

```text
Requerimientos
    │
    ▼
Planificación
    │
    ▼
Arquitectura
    │
    ▼
React
    │
    ▼
Integración API
    │
    ▼
Geolocalización
    │
    ▼
Filtros
    │
    ▼
Accesibilidad
    │
    ▼
Pruebas
    │
    ▼
Documentación
```

---

# Resultado Esperado

Al finalizar la primera iteración el usuario deberá ser capaz de:

- Consultar estaciones de servicio.
- Obtener información basada en una ubicación automática o manual.
- Consultar precios.
- Filtrar resultados.
- Visualizar información procesada de forma estructurada.
- Tomar decisiones basadas en datos procedentes de fuentes oficiales.

---

# Relación con el MVP

Las historias HU-01 a HU-05 constituyen el Producto Mínimo Viable definido en el Anexo A.

Las historias HU-06 a HU-08 corresponden a mejoras funcionales de la primera iteración.

Las historias HU-09 a HU-13 forman parte de la visión futura del proyecto transversal y no forman parte del alcance inicial.

---

# Criterio de Aceptación del Anexo

El anexo se considerará completado cuando:

✅ Las necesidades del usuario estén documentadas.

✅ Existan historias de usuario claramente definidas.

✅ Los casos de uso estén identificados.

✅ Los flujos de usuario y del sistema estén definidos.

✅ La priorización esté alineada con el MVP del proyecto.

✅ Exista trazabilidad entre requerimientos, historias de usuario y desarrollo.

---

# Estado del Documento

**Versión:** 1.0

**Estado:** Aprobado

**Proyecto:** HydroTrack Seed

**Clasificación:** Anexo C