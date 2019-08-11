/_______________________  Descargar MONGODB  _____________________/
https://www.mongodb.com/


/_______________________  Comandos basicos  _____________________/

use testingDB                       (Crea una nueva base de datos con el nombre *testingDB*)
db                                  (nos muestra en que base de datos estamos actualmente)
show dbs                            (muestra todas las bases de datos disponibles)
show collections                    (muestra todas las colecciones de una base de datos)
db.productos.drop                   (elimina una coleccion)
db.dropDatabase()                   (elimina una base de datos)
db.createCollection("productos")    (crea una nueva coleccion en la base de datos)
db.CollectionName.find()            (nos muestra todos los productos de una coleccion)
db.CollectionName.find().pretty()   (nos muestra todos los productos de una coleccion en formato legible)


/_______________________  agregar valores una coleccion testing _____________________/


db.usuarios.insert({
    "id": "1",
    "nama": "karem beatriz",
    "lastName": "tamayo",
    "gender": "F",
    "birthDay": "April"
})
db.usuarios.insert({
    "id": "1",
    "nama": "Soraida ",
    "lastName": "Lopez",
    "gender": "F",
    "birthDay": "November"
})
db.usuarios.insert({
    "id": "1",
    "nama": "oto daniel",
    "lastName": "tamayo",
    "gender": "M",
    "birthDay": "February"
})


/_______________________  editar valores una coleccion testing _____________________/
db.usuarios.update({
    "nama": "jose alejandro"
},
{
    $set:{"lastName": "TAMAYO"}
}
)



/_______________________  eliminar valores una coleccion testing _____________________/
db.usuarios.deleteOne({
    "nama": "jose alejandro"
})



/_______________________  consultas valores una coleccion testing _____________________/
db.usuarios.find().pretty()
db.usuarios.findOne().pretty()
