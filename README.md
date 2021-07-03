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

# Modelo-Vista-Controlador
> Fue implemetado en el proyecto

> [Vista](https://drive.google.com/file/d/1necEE59KAS9suh62vpm8jaPFVtEAGDjo/view?usp=sharing)


> [Modelo entidad relacion](https://drive.google.com/file/d/1xRNeSnZx5EV0IobMmrqyBDilnm2SJ0RG/view?usp=sharing)

> [Versio de oracle instalada](https://drive.google.com/file/d/1N97qdpXuRVQkDuK-chbjdxk36KmldAhN/view?usp=sharing)

> [Version de angular instalada](https://drive.google.com/file/d/18DHE6NqfYa6FfPP6SGt5NreXLKNnWSQh/view?usp=sharing)

> [Version de nodejs y npm](https://drive.google.com/file/d/1ed78CreDInNZKWG_RYN8KkvcEnviPGxj/view?usp=sharing)
