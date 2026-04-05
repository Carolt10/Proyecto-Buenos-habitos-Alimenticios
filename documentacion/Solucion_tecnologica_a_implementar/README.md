# Solución Tecnológica a Implementar

## Descripción del sistema

El sistema consiste en el desarrollo de un sitio web interactivo titulado “Alimentación Saludable Infantil”. En donde su propósito principal es informar, educar y sensibilizar a los padres y acudientes del Jardín Infantil Semillero de la ciudad de Ibagué con respecto a la importancia de los hábitos alimenticios. Además, fomenta la colaboración comunitaria al permitir que los padres compartan sus historias de éxito y aporten distintos materiales o información que consideren útil para otros usuarios.

## Arquitectura general de la solución

El proyecto migra a una arquitectura Server-Side Rendering (SSR) y Client-Side Rendering (CSR) utilizando el App Router de Next.js 16, lo que garantiza un rendimiento optimo y un SEO superior. La arquitectura general de la solución puede ser consultada en el Anexo del presente documento.

### Arquitectura general de la solución

La comunicación se organiza bajo un modelo de responsabilidad compartida entre el cliente y el servidor:

**Capa de presentación (Front end):** Construuida con React 19 y TypeScript. Sigue ua lógica similar al MVVM, donde los componentes de React actúan como la Vista y el estado interno (hooks) gestiona la lógica del ViewModel, asegurando que la interfaz se actualice en tiempo real según los datos del usuario.

**Capa de lógica (Back end):** En lugar de una API REST tradicional, el sistema utiliza Server Actions. Estas son funciones asíncronas seguras que se ejecutan exclusivamente en el servidor, eliminando la necesidad de gestionar endpoints manuales y reduciendo la latencia.

**Capa de Datos (BaaS):** Delegada a Supabase, que proporciona una base de datos PostgreSQL robusta. La comunicación es directa y segura mediante el cliente de Supabase, protegido por políticas de seguridad de nivel de fila (RLS).

<img width="826" height="931" alt="image" src="https://github.com/user-attachments/assets/5505cfcc-1821-4714-a53c-dbf5e0f236b0" />

## Tecnologías que se utilizarán
El sitio web utiliza herramientas de vanguardia para asegurar la escalabilidad y calidad del código como, por ejemplo:

<img width="744" height="537" alt="image" src="https://github.com/user-attachments/assets/ada1c396-5fea-46e0-92a8-899fcce6e25b" />

## Beneficios esperados del sistema

Concientización parental: Servir como un canal amplificador de conocimiento para que los padres tomen decisiones informadas sobre la nutrición de sus hijos.

**Reducción de riesgos de salud:** Contribuir a la disminución del consumo de productos azucarados y ultraprocesados, previniendo enfermedades metabólicas desde edades tempranas.

**Velocidad de respuesta:** El uso de Server Actions simplifica la comunicación entre el front end y el back end, permitiendo que las interacciones (como guardar un caso de éxito o testimonio) sea casi instantáneo.

**Experiencia de usuario fluida:** La combinación de Shadcn/ui y Tailwind CSS 4 garantiza una interfaz moderna, totalmente adaptada a dispositivos móviles y accesible para todos los padres.

**Escalabilidad sencilla:** La arquitectura basada en componentes y el backend como servicio (Baas) permiten añadir nuevas funciones sin necesidad de reestructurar el sistema existente.

