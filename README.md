# taller-postman-orozco

# Marco Contextual
Tarea 1 #### ¿Qué es una API REST?
Una API Rest es un conjunto de reglas que se usan  con el fin de estructurar una aplicación para permitir su comunicación con otras aplicaciones haciendo uso de la internet por medio del protocolo HTTP

Qué significa que una API sea «REST»

Que una API sea REST significa que trata la información como recursos identificables por URLs, utiliza los métodos HTTP estándar para interactuar con ellos, no guarda estado de sesión en el servidor y entrega representaciones ligeras (casi siempre JSON) para mantener el sistema desacoplado y escalable.

Qué es un recurso y qué es un endpoint

Un recurso es la unidad que representa la informacion que se esta pidiendo por medio del llamado a la api, por ejemplo si se necesita listar productos, el recurso sería producto y la petición sería GET
El endpoint por otro lado representa la URI a la cual se hace la petición un ejemplo usando el recurso anterior serí: /localhost/api/producto

## Fuente

Fielding, R. T. (2000). Architectural Styles and the Design of Network-based Software Architectures [Tesis doctoral, University of California, Irvine]. UC Irvine Electronic Theses and Dissertations. https://ics.uci.edu/~fielding/pubs/dissertation/top.htm


# Métodos HTTP
![alt text](image.png)

## Fuente
Internet Engineering Task Force. (2022). HTTP Semantics (RFC N.º 9110). https://www.rfc-editor.org/rfc/rfc9110.html


# Códigos de estado

1xx Son informaticos indican que la petición fue recibida y el servidor continúa el proceso 

2xx Simbolizan éxito en las peticiones enviadas, indicando que la acción solicitada fue recibida, entendida y aceptada correctamente

3xx Simbolizan redirección indicando que el cliente debe tomar medidas adicionales para completar la petición

4xx Simbolizan errores a nivel del cliente indicando que la solicitud contiene sintaxis incorrecta o no puede ser procesada por culpa del cliente.

5x Simbolizan errores a nivel del servidor indicando que el servidor falló al intentar procesar una solicitud aparentemente válida.

## Ejemplos

1. 100 Continue: El servidor confirma que recibió los encabezados de la solicitud y que el cliente puede proceder a enviar el cuerpo (body).

2. 200 Ok: La solicitud HTTP estándar se procesó correctamente y el servidor devuelve los datos solicitados. 

3. 301 Moved Permanently: El recurso solicitado ha sido trasladado permanentemen a una nueva URL especificada en la respuesta.

4. 404 Not Found: El servidor no pudo encontrar el recurso solicitado (La URL está mal escrita o ya no existe).

5. 500 Internal Server Error: Ocurrió una condición inesperada en el backend (Un bug en el código, fallo en la base de datos, entre otros).


# Cómo reproducir este taller

Para importar y ejecutar los ejercicios del taller en tu propio entorno local usando Postman, sigue estos pasos:

1. Clonar el repositorio:
   ```bash
   git clone [https://github.com/tu-usuario/taller-postman-orozco.git](https://github.com/tu-usuario/taller-postman-orozco.git)
   cd taller-postman-orozco

2. Importar la colección en Postman:

Abre la aplicación Postman.

Haz clic en el botón Import ubicado en la esquina superior izquierda.

Selecciona o arrastra el archivo coleccion.json que se encuentra en la raíz del proyecto.

Haz clic en Import para cargar todas las peticiones con sus respectivos Tests automatizados.

3. Ejecutar las peticiones:

Selecciona cualquier petición dentro de la colección cargada.

Presiona el botón Send para interactuar con la API pública JSONPlaceholder.

Revisa la pestaña Test Results en la parte inferior para comprobar la ejecución de las aserciones automatizadas de la Tarea 13.

# Archivos de este repositorio
A continuación se detalla el propósito de cada carpeta y archivo dentro del proyecto:

**README.md**: Documento principal del proyecto que contiene la guía general, el marco conceptual, tablas comparativas y las instrucciones de reproducción.

**coleccion.json**: Colección exportada desde Postman en formato v2.1 que incluye todas las peticiones HTTP configuradas, encabezados, cuerpos de solicitud y scripts de pruebas automatizadas (Tests).

**hallazgos.md**: Documento de análisis con las observaciones técnicas del taller, incluyendo la comparación entre PUT y PATCH, el comportamiento de idempotencia, el análisis de límites (BVA) y el código de las pruebas automatizadas creadas en la Tarea 13.

**evidencias/**: Carpeta destinada a guardar las capturas de pantalla organizadas por tareas:

**01-get-recurso.png**: Captura de consulta exitosa a un recurso individual (GET /posts/1).

**02-get-coleccion.png**: Captura del listado completo de la colección (GET /posts).

**03-error-404.png**: Captura de prueba con un recurso inexistente (GET /posts/9999).

**04-post-creacion.png**: Captura del registro de un nuevo elemento mediante POST.

**05-test-automatico.png**: Captura de la ejecución y aprobación de los tests en la pestaña Test Results.

**conclusiones.md**: Resumen final de aprendizajes obtenidos durante las pruebas de la API.

**image.png / image-1.png a image-7.png**: Capturas de pantalla adicionales generadas durante la realización de las diferentes pruebas del taller.
