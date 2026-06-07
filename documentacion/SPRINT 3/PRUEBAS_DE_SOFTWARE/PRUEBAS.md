# Pruebas de Software

Las pruebas de Software son un control de calidad que se realiza antes de lanzar un desarrollo al público, es un proceso en el que se hace pasar el código por distintos posibles escenarios ya sea en situaciones ideales como en contextos problemáticos.

---

## Pruebas Unitarias

Para validar la robustez del sitio web se implementaron pruebas unitarias utilizando **Vitest**, un framework de testing de última generación optimizado para entornos modernos.

### Objetivo de pruebas unitarias

Las pruebas se dividieron en dos capas:

- **Capa de Backend:** Donde se verificó de manera aislada la lógica de negocio, las funciones utilitarias compartidas (backend, shared, utils) y los módulos principales como por ejemplo education y testimonials.

- **Capa de Frontend:** Se testearon los servicios encargados de la comunicación con las APIs (education/services, recipes/services, testimonials/services), garantizando que la transferencia y el modelado de datos sea correcto y consistente.

#### Ilustración 31 - Pruebas Unitarias

<img width="922" height="236" alt="image" src="https://github.com/user-attachments/assets/80d2b655-574e-403b-92b8-ce0de026ef42" />

> Nota. Pruebas unitarias. Fuente: Elaboración propia (2026).

### Análisis de pruebas unitarias

Como se observa en el reporte de cobertura (code coverage) generado, el proyecto alcanzó un **100% de efectividad** en todas las métricas evaluadas:

- **Statement y Lines (100%):** Garantiza que cada instrucción y línea de código escrita en los módulos fue ejecutada y validada por la suite de pruebas.

- **Functions (100%):** Confirma que la totalidad de los métodos y funciones declaradas responden correctamente al ser invocados.

- **Branches (100%):** Es el indicador más crítico, ya que demuestra que se probaron todos los caminos lógicos (estructuras condicionales if/else, manejo de excepciones y flujos alternos).

Este resultado del **100% de cobertura** mitiga significativamente la aparición de regresiones y certifica la alta calidad, mantenibilidad y estabilidad técnica del software desarrollado.

---

## Pruebas de Integración

Son una fase de control de calidad de software en la que se evalúa cómo interactúan y se comunican entre sí diferentes módulos, componentes o sistemas que ya han sido aprobados individualmente en las pruebas unitarias.

### Objetivo de pruebas de integración

Las pruebas de integración buscan asegurar:

- **Los servicios del Frontend** realicen las peticiones HTTP correctas y que el Backend reciba, procese e integre esos datos en sus módulos correspondientes.

- **Las funciones compartidas** actúen de manera cohesiva como el tejido conectivo del sistema, garantizando que los datos transformados en el servidor se reflejen con exactitud en la interfaz de usuario.

- **El sistema mantenga la integridad y la consistencia** de los datos cuando diferentes módulos operan en conjunto ante escenarios reales de uso.

#### Ilustración 32 - Pruebas de integración

<img width="922" height="167" alt="image" src="https://github.com/user-attachments/assets/85695a46-ebd1-4b85-b1ba-154dc4eb5e9c" />

> Nota. Pruebas de integración. Fuente: Elaboración propia (2026).

### Análisis de pruebas de integración

El reporte demuestra un escenario ideal de integración, alcanzando un **100% de cobertura** en todas las métricas conjuntas por lo que podemos concluir:

- **Acoplamiento correcto (100% Branches & Functions):** Al estar integrados los módulos de educación, testimonios y recetas, el 100% en Branches indica que las reglas de validación cruzada y los flujos de control funcionan perfectamente en conjunto.

- **Flujo de Datos Limpio (100% Lines & Statements):** Cada línea de código destinada a conectar las solicitudes de los usuarios con la lógica del servidor fue ejecutada con éxito. No existen rutas de datos desaprovechadas ni comunicaciones fallidas entre capas.

---

## Pruebas EndToEnd - E2E

Las pruebas EndToEnd son una metodología de verificación de software diseñada para evaluar el comportamiento del sistema desde la perspectiva del usuario final, las pruebas E2E validan el sitio web en su totalidad como un sistema integrado.

### Objetivo de pruebas EndToEnd

En este proyecto las pruebas E2E se diseñaron con el objetivo de garantizar la integridad de la experiencia de usuario y el correcto funcionamiento del sistema lo cual buscaba validar:

- **Flujos completos de usuario:** Un usuario puede interactuar con la interfaz del Frontend, navegar por los módulos como Educación o Recetas, rellenar formularios o consumir contenido y que estas acciones se reflejen correctamente en toda la aplicación.

- **Persistencia y sincronización:** Los datos creados, modificados o eliminados durante la sesión del usuario se reflejen de manera inmediata y consistente en la aplicación.

- **Validación de entorno real:** Validar que el software responda correctamente ante la latencia de red, renderizado de componentes en tiempo real y validaciones de seguridad de extremo a extremo.

### Análisis de pruebas EndToEnd

Las pruebas EndToEnd implementadas se ejecutaron de manera automatizada, simulando clicks, entradas de texto y navegaciones a velocidades reales de procesamiento.

Los resultados obtenidos fueron **completamente satisfactorios**, demostrando que el sistema es capaz de soportar los flujos críticos de la aplicación sin presentes quiebres en la interfaz, pérdidas de datos o comportamientos inesperados.

#### Vídeo de pruebas EndToEnd

Como sustento y demostración del correcto funcionamiento automatizado de estos flujos críticos, se adjunta el siguiente registro en video donde se observa a la herramienta interactuar con la plataforma:

**Enlace:** https://youtu.be/rY4vZyQYkm0