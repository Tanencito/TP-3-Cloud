# :cloud: Computación en la nube: Trabajo Práctico 3

## :bust_in_silhouette: Datos personales

- Nombre: **Daniel Dumont**
- Legajo: **43848**

## :crystal_ball: Instalación

### Correr proyecto

```bash
Primero borramos todas las imagenes que existan en Docker:
docker container rm dynamodb

Después creamos la red:
docker network create awslocal

Ahora descargamos la imagen del shell y la compartimos para que la API se pueda comunicar con la tabla:
docker run --rm -p 8000:8000 --network awslocal --name dynamodb amazon/dynamodb-local:1.15.0 -jar DynamoDBLocal.jar -sharedDb

Por último, ingresamos a la carpeta del proyecto por medio del panel de comandos y ejecutamos lo siguiente para levantar la API:
sam local start-api --docker-network awslocal

Accedemos a:
http://localhost:8000/shell y copiamos el código de Tablas.txt

Por último, podemos hacer las consultas http.
```

