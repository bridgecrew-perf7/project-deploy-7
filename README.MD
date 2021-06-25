# Archivos para despliegue de aplicación flask/react, a traves de dos containers docker, utilizando traefik como proxy reverso:

## DEMO corriendo en instancia de AMAZON EC2

* [FRONTEND](http://54.94.217.113/)
* [API](http://54.94.217.113/api/doc)

Usuarios de prueba:
* nacosta
* fcorvalan
* fdiaz
* admin

La contraseña de todos los usuarios es `1234`

Tanbién se puede realizar el log in desde swagger para probar las apis, haciendo click en Authorize.

## Despliegue:
 
* Importante tener docker y docker-compose instalado*.

Clonar repo y posicionarme en el: 
```bash
$ git clone https://github.com/eneacosta/coins-front.git

$ cd coins-front
```

Modificar variable `DOMAIN`  archivo `.env`, por el dominio o ip publica de donde esta corriendo el sistema (`localhost` en caso de correrlos localmente).

Levantar los containers: 
```bash
$ docker-compose up
```

Levantar los containers en el background: 
```bash
$ docker-compose up -d
```

Realizados estos pasos deberia estar corriendo el frontend en la raiz de su dominio, y la api en dominio/api.