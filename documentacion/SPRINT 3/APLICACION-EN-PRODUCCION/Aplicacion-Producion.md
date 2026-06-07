# Aplicación en Producción

El sistema desarrollado para el Jardín Infantil Semillero de Ibagué cuenta con una arquitectura de despliegue híbrida y moderna, diseñada para garantizar tanto el aislamiento del entorno de desarrollo como la escalabilidad y seguridad en producción.

---

## Configuración de Contenedores y Ejecución Local

Con fines de estandarización, portabilidad y aprendizaje práctico en la gestión de infraestructura, se implementó la contenedorización de la aplicación mediante Docker. Esto asegura que cualquier miembro del equipo pueda ejecutar el sistema en su entorno local con las mismas características de producción.

### Manifiestos Esenciales

El repositorio del proyecto incluye los siguientes manifiestos esenciales para este proceso:

- **Dockerfile**: Archivo de configuración que define los pasos secuenciales para construir la imagen base de la aplicación.
- **docker-compose.yml**: Archivo de orquestación que define los servicios, redes virtuales y volúmenes necesarios para levantar el contenedor de la aplicación de forma unificada mediante un único comando.

---

## Análisis de Evidencias de Ejecución Local

De acuerdo con el flujo de trabajo desarrollado y las pruebas de infraestructura registradas en la rama `dev/actions`, se documenta el comportamiento analítico del proceso de virtualización:

### 1. Construcción y Despliegue de Contenedores

Mediante la ejecución del comando `docker compose up –build`, el motor de Docker procesa secuencialmente los manifiestos de configuración y exporta las imágenes base, generando un contenedor ejecutable con todas las dependencias integradas.

**Ilustración 36** - Construcción y despliegue de contenedores

<img width="815" height="403" alt="image" src="https://github.com/user-attachments/assets/416d1166-1cbb-4ad2-a9b3-40c693dab0f2" />

> **Nota**: Construcción y despliegue de contenedores. Fuente: Elaboración propia (2026).

### 2. Validación del Ciclo de Vida y Variables de Entorno

Al inicializar el servicio del framework (`next start`) dentro del contenedor en el puerto 3000, el servidor ejecuta las rutinas de verificación de variables de entorno requeridas:

```
[v0] Error en getTestimonials: Error: your project's URL and Key are required to create a Supabase client!
```

Este comportamiento es correcto y responde al diseño de arquitectura segura estipulado en los registros de decisión de arquitectura (ADR). La excepción demuestra la existencia de un mecanismo estricto de validación que previene la ejecución con configuraciones incompletas.

**Ilustración 37** - Validación del ciclo de vida y variables de entorno

<img width="841" height="291" alt="image" src="https://github.com/user-attachments/assets/943ee4cd-9728-4dbc-b45c-801a7d37d823" />

> **Nota**: Validación del ciclo de vida y variables de entorno. Fuente: Elaboración propia (2026).

---

## Referencias

- [Arquitectura General del Sistema - DOCKER.md](https://github.com/Carolt10/Desarrollo-Proyecto-Buenos-habitos-Alimenticios/blob/main/DOCKER.md)
