# Tarea 3
Responde además esta pregunta, que es la que importa: ¿por qué se separan los errores
4xx de los 5xx? ¿Qué cambia entre unos y otros desde el punto de vista de quién tiene
la culpa?

R/ La diferencia radica en la responsabilidad del error, se adjudica al cliente y genera un error de tipo 4xx cuando el cliente manda una petición mal formulada, en cambio, si la petición esta bien formulada, pero hubo un error a nivel de servidor, se devuelve un error de tipo 5xx, dando a entender que el error no esta en la petición sino en la demora de la respuesta de la base de datos o algún otro tipo de falla a nivel de servidor. Separandolos se entiende mejor de que parte es el error y se puede proceder a una solución concreta más eficientemente.


¿en qué se diferencian los criterios de aceptación cuando pides un
recurso y cuando pides una colección?

R/ Los criterios de aceptación se diferencian en una única cosa, si le pasas un id a la petición de tipo get, por medio del URI, va a interpretar eso como una petición de busqueda por Id, en cambio si mandas la petición sin id, va a interpretar la petición como un listar general del recurso, dependiendo de lo que se mande en la URI es lo que interpreta y devuelve el servidor.

# Tarea 4
¿Este caso de prueba pasó o falló? Justifica tu respuesta.

R/ El caso de prueba pasó ya que estaba predeterminado para generar un error y testear la respuesta del servidor ante dicho error, la cual fue la esperada, un 404, lo que se espera cuando se manda una petición sobre un recurso que no existe en la base de datos.

# Tarea 6
¿qué observaste? ¿Por qué crees que ocurre eso? ¿Cómo comprobarías, en una
API real, que el recurso se creó de verdad?

R/ Observé que no hubó cambios en el id después de haber ejecutado la misma petición tipo post 5 veces seguidas, y al listar con get la colección de dicho recurso no veo el que estoy instertando, entonces supongo que solo sirve para simular la respuesta de un servidor y no hay una interacción real. En una API real revisaría el recurso haciendo una petición mandando el id especifico del que cree con el metodo post, así si me lo devuelve confirmo que en efecto si se creo correctamente

# Tarea 7
¿qué diferencia encontraste entre ambas respuestas? ¿Cuál usarías para
corregir un error de escritura en un solo campo, y por qué?

R/ La diferencia que note es que en el metodo PUT se borraron todos los campos que no edite, y se mantuvo el que mande, y con el metodo patch solo altero el campo que mande manteniendo el valor intacto en los otros, es decir que uno edita parcialmente y el otro edita todo asumiendo que lo que no se envia se borra. Para un hipotetico caso donde no quiero alterar todos los datos de un recurso, usaría el metodo patch, manteniendo los cambios que aplique y los valores que tenían los campos que no edite.

# Tarea 8 
Investiga qué significa que un método HTTP sea idempotente. Luego determina
cuáles de los cinco métodos lo son y cuáles no.
R/ Un método es idempotente cuando la respuesta de la petición siempre es la misma, de los 5 metodos GET, PUT y DELETE son idempotentes 

Compruébalo en Postman: ejecuta varias veces la misma petición PUT y luego varias
veces la misma POST. ¿Qué diferencia observas en el resultado?

R/ Observé que al repetir varias veces la petición tipo PUT no hubo cambios aparentes en la respuesta, en cambio con la peticion tipo POST, cada vez que se enviaba me generaba un nuevo id.

# Tarea 9
1. Content-Type: Indica el formato multimedia del cuerpo de la respuesta enviada por el servidor, así como la codificación de caracteres utilizada.
Es importante al probar una API porque permite al cliente saber con exactitud cómo procesar y parsear la informcación recibida. Sin esta cabecera, el cliente no sabría si debe interpretar la respuesta como JSON, HTML, texto plano o un archivo binario.

2. Cache-Control: Especifica las directivas de almacenamiento en caché que deben seguir el cliente y los intermediarios. En la respuesta de JSONPlaceholder suele devolver max-age=43200 o no-cache

3. Access-Control-Allow-Origin: Es una cabecera fundamental del protocolo CORS (Cross-Origin Resource Sharing). Indica si la respuesta puede ser compartida y consumida por un sitio web con un dominio, puerto o protocolo distinto al del servidor.

# Tarea 10
¿cómo se llama ese tipo de caso de prueba? ¿Por qué se dice que los
defectos se concentran ahí?
R/ Este tipo de prueba se conoce como prueba de valores limite (Boundary value analysis). se dice que los defectos se concentran ahí por varias razones, al ser valores limites normalmente puede llegar a faltar una validacion,o puede haber un error tipografico que hace que el sistema no responda correctamente al sobrepasar cierto limite, y este tipo de cosas se concentran en los puntos min min-1 y max max+1, por eso se hace necesario testearlos, para probar validaciones, verificar que no haya errores tipograficos entre otras cosas.