# Ejercicio 4 - Docker Compose

#### **Desplegar la aplicación cmatrix utilizando docker-compose.** 

**Entregar los siguientes pantallazos y lo comandos empleados para resolver el ejercicio:** 

Crearemos un contenedor usando la aplicación cmatrix, para ello generamos un archivo Dockerfile en nuestro directorio de trabajo:

![image-20230208195950675](./assets/image-20230208195950675.png)

Ahora construimos el contenedor:

```
docker build -t cmatrix .
```

Ahora subiremos ese contenedor a nuestra cuenta de DockerHub, para ello nos logueamos:

```
docker login
```

![image-20230208200212031](./assets/image-20230208200212031.png)

Ponemos una etiqueta a nuestro contenedor, lo vinculamos a nuestra cuenta y lo subimos a DockerHub:

```
docker tag cmatrix javiesca/cmatrix:latest
```

```
docker push javiesca/cmatrix:latest
```

![image-20230208200418002](./assets/image-20230208200418002.png)

Una vez hecha la imagen y subida a nuestra DockerHub continuamos con el ejercicio.

- **Pantallazo donde se vea el fichero *docker-compose.yaml*.** 

  ![image-20230210085651423](./assets/image-20230210085651423.png)

  Este es la ultima configuración probada, he probado con múltiples configuraciones y ninguna me muestra el efecto pese a que el contenedor está arrancado.

  

  ![image-20230210085843513](./assets/image-20230210085843513.png)

  

- **Pantallazo donde se vea la aplicación funcionando.** 

  Ejecutamos el comando:

  ```
  docker run -it cmatrix
  ```

  ![image-20230210090034844](./assets/image-20230210090034844.png)

- **Explicar brevemente cómo funciona esta aplicación.**

Esta aplicación es un programa que muestra una animación de caracteres al estilo "Matrix". Muestra una combinación de caracteres ASCII que puedes personalizar en diferentes colores y velocidad de caída.

