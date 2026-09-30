Responde además esta pregunta, que es la que importa: ¿por qué se separan los errores
4xx de los 5xx? ¿Qué cambia entre unos y otros desde el punto de vista de quién tiene
la culpa?

R/ La diferencia radica en la responsabilidad del error, se adjudica al cliente y genera un error de tipo 4xx cuando el cliente manda una petición mal formulada, en cambio, si la petición esta bien formulada, pero hubo un error a nivel de servidor, se devuelve un error de tipo 5xx, dando a entender que el error no esta en la petición sino en la demora de la respuesta de la base de datos o algún otro tipo de falla a nivel de servidor. Separandolos se entiende mejor de que parte es el error y se puede proceder a una solución concreta más eficientemente.


¿en qué se diferencian los criterios de aceptación cuando pides un
recurso y cuando pides una colección?

R/ Los criterios de aceptación se diferencian en una única cosa, si le pasas un id a la petición de tipo get, por medio del URI, va a interpretar eso como una petición de busqueda por Id, en cambio si mandas la petición sin id, va a interpretar la petición como un listar general del recurso, dependiendo de lo que se mande en la URI es lo que interpreta y devuelve el servidor.

