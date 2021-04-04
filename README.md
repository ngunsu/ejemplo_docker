# Ejemplos

## Ejemplo 1

Servir /html/index.html utilizando apache

```bash
docker run -it -p 2020:80 -v $PWD:/usr/local/apache2/htdocs/ httpd:2.4.46-alpine
```

Verificar en el navegador [localhost:2020](http://localhost:2020)

## Ejemplo 2

Crear nuestra propia imagen, utilizando apache como base

- Paso  1: Crear imagen

```bash
docker build -f dockerfile_ejemplo2/Dockerfile . --tag newserver
```

- Correr ejemplo

```bash
docker run -it -p 2020:80 newserver
```

Verificar en el navegador [localhost:2020](http://localhost:2020)
