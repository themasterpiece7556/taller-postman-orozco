# Metodo PUT 
![alt text](image-1.png)
# Metodo PATCH 
![alt text](image-2.png)
# Id más alto que devuelve 200
![alt text](image-3.png)
# Primer id que devuelve 404
![alt text](image-4.png)
# Recurso albums
![alt text](image-6.png)
# Recurso photos
![alt text](image-7.png)
# Ruta anidada
![alt text](image-5.png)
# Pruebas 
1. Prueba 1
Código: pm.test("El tiempo de respuesta es menor a 500 ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(500);
});

Sirve para verificar el tiempo de respuesta

2. prueba 2 
Codigo: pm.test("El objeto contiene el campo 'title' de tipo String", function () {
    const responseData = pm.response.json();
    
    // Si la respuesta es un arreglo (ej. GET /posts), tomamos el primer elemento
    const post = Array.isArray(responseData) ? responseData[0] : responseData;
    
    pm.expect(post).to.have.property('title');
    pm.expect(post.title).to.be.a('string');
});

Sirve para verificar la presencia y el tipo de datos de campos clave

3. prueba 3

Codigo: pm.test("La respuesta contiene exactamente 100 publicaciones", function () {
    const responseData = pm.response.json();
    
    // Verificamos que sea un arreglo y que su longitud sea 100
    pm.expect(responseData).to.be.an('array');
    pm.expect(responseData.length).to.eql(100);
});

Sirve para verificar la cantidad de elementos en una lista