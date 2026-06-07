Aplicación en producción 
El sistema desarrollado para el Jardín Infantil Semillero de Ibagué cuenta con una arquitectura de despliegue híbrida y moderna, diseñada para garantizar tanto el aislamiento del entorno de desarrollo como la alta disponibilidad, seguridad y automatización en el entorno de producción. A continuación, detalla la configuración técnica de ambos componentes:
Configuración de contenedores y ejecución local
Con fines de estandarización, portabilidad y aprendizaje práctico en la gestión de infraestructura, se implementó la contenedorización de la aplicación mediante Docker. Esto asegura que cualquier miembro del equipo de desarrollo o evaluador pueda ejecutar el proyecto localmente bajo las mismas condiciones de producción, aislando por completo las dependencias del sistema operativo anfitrión.
El repositorio del proyecto incluye los siguientes manifiestos esenciales para este proceso:
•	Dockerfile: Archivo de configuración que define los pasos secuenciales para construir la imagen base de la aplicación.
•	docker-compose.yml: Archivo de orquestación que define los servicios, redes virtuales y volúmenes necesarios para levantar el contenedor de la aplicación de forma unificada mediante un único comando, mapeando el puerto local para su consumo accesible vía navegador web en http/localhost:3000.
Análisis de evidencias de ejecución local
De acuerdo con el flujo de trabajo desarrollado y las pruebas de infraestructura registradas en la rama dev/actions, se documenta el comportamiento analítico del proceso de virtualización:
•	Construcción y despliegue de contenedores: Mediantes la ejecución del comando docker compose up –build, el motor de Docker procesa secuencialmente los manifiestos de configuración y exporta las capas correspondientes. Este proceso compila satisfactoriamente la imagen bajo la etiqueta desarrollo-proyecto-buenos-habitos-alimenticios-app:latest. Posteriormente, el orquestador inicializa de manera óptima la red virtual dedicada (desarrollo-proyecto-buenos-habitos-alimenticios_default) y pone en marcha el contenedor.
Ilustración 36 - Construcción y despliegue de contenedores
 
Nota. Construcción y despliegue de contenedores. Fuente: Elaboración propia (2026).

•	Validación del ciclo de vida y variables de entorno: Al inicializar el servicio del framework (next start) dentro del contenedor en el puerto 3000, el servidor ejecuta las rutinas de verificación de conectividad. Durante esta fase, el sistema arroja la siguiente excepción controlada en los registros de la consola:
[v0] Error en getTestimonials: Error: your project’s URL and Key are required to create a Supabase client!
Este comportamiento es correcto y responde al diseño de arquitectura segura estipulado en los registros de decisión de arquitectura (ADR). La excepción demuestra la existencia de un mecanismo estricto de validación para las variables de entorno. Al no estar parametrizadas las credenciales del servicio Supabase dentro del archivo .env local asignado al contenedor, el cliente de la base de datos restringe la conexión para salvaguardar la integridad de la infraestructura. Para habilitar el funcionamiento local pleno, se requiere la inyección previa de las llaves NEXT_PUBLIC_SUPABASE_URL y NEXT_PUBLIC_SUPABASE_ANON_KEY en las variables del entorno virtualizado.
Ilustración 37 - Validación del ciclo de vida y variables de entorno
 
Nota. Validación del ciclo de vida y variables de entorno. Fuente: Elaboración propia (2026).

Enlace de la arquitectura general del sistema
https://github.com/Carolt10/Desarrollo-Proyecto-Buenos-habitos-Alimenticios/blob/main/DOCKER.md 
