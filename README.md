## tema de docker

Docker fue utilizado para cargar una base de datos en local con una imagen.

### correr docker

```
docker compose up
docker compose --env-file [dir_name] up
#correr un servicio especifico
docker compose up -d pgadmin
```

para que agarre el archivo de environment al momento de correr por primera vez:

```
docker compose --env-file .env up

```

### Entrar dentro del contenedor:

```
docker-compose exec [nombre del servicio/contenedor] bash
```

dentro del contenedor podemos conectarnos a postgress de la siguiente manera:

```
mysql -h localhost -u servero -p
```

### `Usando Mysql workbench`

durante el intento de usar en linux, parece que hay algún tipo de bloqueo cuando se instala por la tienda
de ubuntu. Para corregir el error encontré una [página](https://www.ingenieriazeros.com/2020/06/solucion-workbench-ubuntu-AppArmor.html)
que mostraba la solución.

```
snap connect mysql-workbench-community:password-manager-service
snap connect mysql-workbench-community:ssh-keys
```
