Responde además esta pregunta, que es la que importa: ¿por qué se separan los errores
4xx de los 5xx? ¿Qué cambia entre unos y otros desde el punto de vista de quién tiene
la culpa?

R/ La diferencia radica en la responsabilidad del error, se adjudica al cliente y genera un error de tipo 4xx cuando el cliente manda una petición mal formulada, en cambio, si la petición esta bien formulada, pero hubo un error a nivel de servidor, se devuelve un error de tipo 5xx, dando a entender que el error no esta en la petición sino en la demora de la respuesta de la base de datos o algún otro tipo de falla a nivel de servidor. Separandolos se entiende mejor de que parte es el error y se puede proceder a una solución concreta más eficientemente.


