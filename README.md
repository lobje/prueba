# Manejo e Implementacion de Archivo 
## Proyecto 2   201314059

 >Se inicia con la [instalacion de docker](https://linuxhint.com/install_configure_docker_ubuntu/)
 #
 >Descargar la imagen, tardara algo de tiempo 
 
    docker pull dockerhelp/docker-oracle-ee-18c
#
>Se crea el contenedor de oracle 18c

    docker run -it -p 1521:1521 --name nombre_que_desee dockerhelp/docker-oracle-ee-18c
    sh post_install.sh
#
>Comando a ejecutar en sql

    sqlplus
    #user: sys as sysdba
    #pass: oracle
    alter session set "_ORACLE_SCRIPT"=true;
#
>Se crea una nuevo usuario y contraseña

    create user nuevo_usuario identified by nueva_contraseña;
#
>Se le otorgan permisos al usuario creado

    grant dba to nuevo_usuario;
 
#

>Cuando el contenedor esta apagado se corre el primer comando

    docker restart codigo_generado_por_docker
    docker exec -it codigo_generado_por_docker  /bin/bash
    sh post_install.sh
 
#
 
>Lo siguiente sera la [instalacion sql oracle developer](https://www.sismonda.com.ar/1193-2020-11-09-sql-developer-en-ubuntu-20-04/)
 
 
#

>Cuando el contenedor ya esta corriendo los datos nuevo_usuario y nueva_contraseña que fueron los definidos anteriormente se usaran para conectar

    connected
    nuevo_usuario
    nueva_contraseña

#

>En mi caso el nombre de usuario y contraseña fueron los que defini arriba

- Name: nombre_para_db
- Usuario: nuevo_usuario
- Contraseña: nueva_contraseña
- Nombre host: localhost
- Puerto: 1521
- Nombre del servicio: ORCL18

# Modelo-Vista-Controlador(MVC)
> es un patrón de arquitectura de software, que separa los datos y principalmente lo que es la lógica de negocio de una aplicación de su representación y el módulo encargado de gestionar los eventos y las comunicaciones.
> [mas informacio.](https://es.wikipedia.org/wiki/Modelo%E2%80%93vista%E2%80%93controlador)

> [Vista](https://drive.google.com/file/d/1necEE59KAS9suh62vpm8jaPFVtEAGDjo/view?usp=sharing)


### [Modelo entidad relacion](https://drive.google.com/file/d/1xRNeSnZx5EV0IobMmrqyBDilnm2SJ0RG/view?usp=sharing)

> **Tabla user:** Usada para almacenar la informacion de los datos del usuario que se registra.
> 
> **Tabla publication:** Usada para almacenar los datos de las publicaciones y que estan asociados a un usuario.
> 
> **Tabla tag:** Encargada de almacenar los diferentes tags que se agrega a una o varias imagen de una publicacion.
> 
> **Tabla list_tag:** Encargada de almacenar la relacion que existe entre un publicacion y un tag.
> 
> **Tabla amigo:** Se encarga de almacenar la relacion de amistad entre 2 usuarios o para almacena una solicitud de amistad.
> 
> **Tabla chat:** Almacena la comunicacion entre 2 usuarios a traves de mensaje.
> 
> **Tabla message:** Se encarga de almacenar toda la comunicacion en un chat asi como tambien esta asociado a un usuario en especifico describiendo quien lo envio. 

## Endpoint

> **router.get('/getUsers',getUsers):** Obtiene todos los usuarios registrados en la base de datos.

> **router.post('/login',login):** Recibe un nombre de usuario y una contraseña y obtiene como resultado un valor regresa un valor que confirma si puede o no accede a la pagian.

> **router.post('/createAccount', newAccount):** Recibe un conjunto de parametro para crear una nueva cuenta en la pagina. 

> **router.post('/updateInfo', updateInfo):** Recibe un conjunto de parametro con valores actualizados y una contraseña que hace la confirmacion de los cambios.

> **router.post('/getPosts', getPosts):** Reccibe el nombre del usuario y retorna las publicaciones asociadas a el.

> **router.post('/createPost', createPost):** Recibe un cojunto de parametros para crear una nueva publicacion.

> **router.post('/searchPost', searchPost):** Buscar y retorna las publicaciones asociado a un tag en espaifico.


## Stored Procedure

> es un grupo de declaraciones PL / SQL al que puede llamar por su nombre y puede o no tener parametros. El Stored Procedure puede tener almacenado un conjunto de sentecias de sql para manipular la Base de datos. [mas informacion.](https://docs.oracle.com/cd/B19306_01/server.102/b14200/statements_6009.htm)


### [Versio de oracle instalada](https://drive.google.com/file/d/1N97qdpXuRVQkDuK-chbjdxk36KmldAhN/view?usp=sharing)

### [Version de angular instalada](https://drive.google.com/file/d/18DHE6NqfYa6FfPP6SGt5NreXLKNnWSQh/view?usp=sharing)

### [Version de nodejs y npm](https://drive.google.com/file/d/1ed78CreDInNZKWG_RYN8KkvcEnviPGxj/view?usp=sharing)
