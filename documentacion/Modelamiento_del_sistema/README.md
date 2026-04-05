# Modelamiento del Sistema

Esta sección contiene el modelamiento y diagramas del sistema para el proyecto de hábitos alimenticios saludables

# Diagrama estructural
En este diagrama se describen como están relacionados los sistemas por dentro, además de mostrar como están estructurado los diferentes servicios y base de datos utilizados en el proyecto. El diagrama estructural original puede ser consultado en el Anexo del presente documento.

<img width="1003" height="754" alt="image" src="https://github.com/user-attachments/assets/2a99dd3f-6ae0-4ce9-9214-738fde6a9e4f" />

Nota. Representación visual del diagrama estructural. Fuente: Elaboración propia en Daw.io.

# Diagrama de comportamiento

En este diagrama de secuencia se describe como el proceso de interacción entre el sistema y el usuario al momento de consultar una receta o descargar un archivo PDF, mostrando la comunicación entre el cliente, el servidor, la base de datos y el servicio de almacenamiento. El diagrama de comportamiento original puede ser consultado en el Anexo del presente documento.

<img width="910" height="476" alt="image" src="https://github.com/user-attachments/assets/b5e8ecf1-64bf-49d4-809c-f04de6cbdbfb" />

Nota. Representación visual del diagrama de comportamiento. Fuente: Elaboración propia en Daw.io.

# Diagrama de caso de uso

En este diagrama se evidencia de forma sencilla las funciones del sistema desde la perspectiva del usuario, además de observarse como es la interacción para acceder al contenido de cada nodo. El diagrama de caso de uso original puede ser consultado en el Anexo del presente documento.

<img width="907" height="666" alt="image" src="https://github.com/user-attachments/assets/6014d37b-a8f1-4f51-9249-35a6ad7607e3" />

Nota. Representación visual del diagrama de caso de uso. Fuente: Elaboración propia en Daw.io.

# Diagrama entidad-relación (ER)

Este diagrama se usa para diseñar o depurar bases de datos relacionales en proyectos de software. En este diagrama las tablas no se relacionan entre sí mismas porque no se poseen roles como usuario o administrador al ser un sitio web de acceso libre. El diagrama de entidad relación original puede ser consultado en el Anexo del presente documento.

<img width="734" height="462" alt="image" src="https://github.com/user-attachments/assets/487cdaf9-9366-4eb7-b821-a04c80ee319d" />

Nota. Representación visual del diagrama de entidad relación. Fuente: Elaboración propia en Daw.io.

# Descripción general de las entidades principales del sistema

En la primera tabla de videos educativos se denota que es la encargada de gestionar los contenidos multimedia, almacenando recursos externos como YouTube, además entre sus atributos destaca el control sobre el autor y su tipo, también incluyendo metadatos técnicos como la duración y categoría.

La segunda tabla articulas información representa el repositorio de conocimientos o blogs del sistema, ofreciendo lecturas específicas y artículos de interés a los usuarios, además de que se enfoca en el contenido y el tiempo de lectura, siendo datos valiosos para la experiencia del usuario.

La tercera tabla recetas es la más específica del sistema enfocándose en la parte practica y nutricional entregando guías bien explicada para la preparación de alimentos saludables, teniendo atributos importantes como la lista de ingredientes, tiempo, porción y dificultad, incluyendo un campo de calificación permitiendo interacción En el ranking de las recetas.



