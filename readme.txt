# Documentación

Para la solución de este ejercicio se ocupo el framework Postman

## Primeros pasos 
* Se ingresa a la url https://petstore.swagger.io/ donde seenter code here encuentra la documentación sobre apis de una "PetStore"
* Se copia la url https://petstore.swagger.io/v2/swagger.json para realizar la importación de la api en Postman 
* Abrir Postman, clic en el botón "Importar" (Import) y pegamos la url anteriormente copiado 
 * A continuación se presenta en pantalla las colecciones disponibles de la Api

## Añadir una mascota a la tienda

Para añadir una nueva mascota es necesario tomar en cuenta el body de la peticion que se hará, según la documentación presentada el body en formato json es el siguiente:

		      
    Pet{
		"id":"",
		"category":{
			"id":"",
			"name":"",
		},
		"name": " ",
		"photoUrls":[
		],
		"tags":[
		  {
			"id": 0,
			"name": " "
		  }
		],
		"status": " "
		} 


En este caso ingresaremos un perro de nombre bruno. (Script a utilizar, se encuenta en el documento scriptCrearMascota.json). 
Una vez que se tiene la estructura con los datos que se realizará las pruebas, se debe:
* Abrir la colección "Add a new pet to the store" 
* Nos fijamos que la petición sea de tipo Post
* Se elige la opción Body y se pega el codigo anteriormente realizado
* Finalmente se envía los datos ingresados. 
Si la petición se realizó correctamente, Postman presenta como respuesta un mensaje con el status 200 OK, en la parte medio del framework. 
Y finalmente presenta el mismo código en enviado en la partes posterior del framework. (Resultado de la petición, captura de pantalla. CrearMascota.png)


## Consultar la mascota ingresada previamente (Búsqueda por ID)

Para la consulta de la mascota que se agregó, nos dirigimos a la colección "Find pet by ID" y se da un clic, en este caso, se requiere ingresar el ID de la mascota que se agregó. 
El parámetro de entrada se llama **"petId"**, el id de la mascota ingresada es el numero 9999998. 
Si se ingresa un valor correcto la respuesta de la petición es el mensaje  "Status 200 OK", si la consulta es incorrecta saldran los mensajes 400 ó 404. (Resultado de la petición, captura de pantalla. BusquedaMascotaId.png)

## Actualizar el nombre de la mascota y el estatus de la mascota a "sold"

Para actualizar los datos de una mascota seleccionada, nos dirigimos a la colección "Updates a pet in the store with form data" donde nos permite buscar a la mascota que deseamos modificar por el ID y nos da la opción de modificar los campos name y  status.
Parametro de entrada

 - petId--> 9999998

Campos a modificar
* name-->Draco
* status-->sold

Si la petición se realizó correctamente, Postman presenta como respuesta un mensaje con el status 200 OK . (Resultado de la petición, captura de pantalla. ModificarMascota1.png y ModificarMascota2.png)

## Consultar la mascota modificada por estatus (Búsqueda por estatus) 

Para la busqueda de la mascota modificada por estatus, nos dirigimos a la colección "Finds Pets by status" donde nos permite buscar a la mascota por el estatus.
En este caso el parametro de query es el campo status y el valor de este campo es "sold". (Resultado de la petición, captura de pantalla. BuscarMascotaStatus.png)