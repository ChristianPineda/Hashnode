---
title: "How To: Tu primer contenedor con ASP.NET"
seoTitle: "Docker, ASP.NET,"
datePublished: Sat Apr 09 2022 05:40:37 GMT+0000 (Coordinated Universal Time)
cuid: cl1rfhr2u03lw0wnvh2cm1zib
slug: how-to-tu-primer-contenedor-con-aspnet
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1649375771969/2h4u8Pgo2.png
tags: microservices, docker, microsoft, aspnet, docker-images

---

Si no quieres leer el blog con las instrucciones, puedes ver el video en mi canal de Youtube

[Tu primer contenedor](https://youtu.be/3QSkO2CMmRw)
 
Para comenzar vamos a usar Visual Studio 2022 ya que es más fácil agregar el contenedor. 
[Descargar Visual Studio 2022](https://visualstudio.microsoft.com/es/vs/)

1.Crear proyecto de ASP.NET Core Web API

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649373948508/rCv087w1h.png)
Dar click en **siguiente**

2.Seleccionar versión, marcar 'ninguno' en autenticación, marcar configurar para HTTPS, no marcar 'docker' (porque lo agregaremos después), marcar compatibilidad con OpenAPI

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649374460192/bHSLkpUFU.png)
Dar click en **crear**

Al crearse el proyecto, tendrás una API estilo REST que correra con IIS Express, un servidor de apps web de Microsoft y que podrás correr de forma local en tu máquina.
Como la API está documentada con Swagger (para esto habilitamos OpenAPI) vamos a ver una dirección en el navegador con esta estructura

**https://localhost:44327/swagger/index.html**

3.Solamente contiene un método, que es el GET y nos entrega un resultado aleatorio de 5 estados de clima, para esto debemos dar click en el **GET**, luego en el botón **Try it out** y por último en **Execute**

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649375099983/G2b0-_rfL.png)
Y obtendremos un código de respuesta 200 (OK) y los datos de la API

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649375162185/d4cUq4in6.png)

4.Podemos copiar el URL que viene en Request URL, así podemos ver el JSON directamente, de forma normal, será un texto plano sin formato, te recomiendo descargar esta extensión para formatear el JSON


[Descargar JSON Formatter](https://chrome.google.com/webstore/detail/json-formatter/mhimpmpmffogbmmkmajibklelopddmjf)

Y ahora podrás verlo así

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649375447376/btz4pYpB1.png)

5.Primero, debes tener Docker Desktop instalado, puedes descargarlo aquí

[Descargar Docker](https://www.docker.com/products/docker-desktop/)

Luego, en el explorador de soluciones, da click derecho y luego en **agregar**, luego **compatibilidad con Docker**

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649480376409/gdkYZdQxR.png)
6.Selecciona el SO de tu preferencia, debe funcionar exactamente igual :)

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649480455855/3krCkhLZN.png)

7.Es importante, en este caso, agregar la compatibilidad porque si agregas solamente el archivo de Dockerfile, Visual Studio no va a hacer la configuración necesaria para que funcione correctamente.
Entonces al dar click, se modificará el **.csproj** y se añadrá al proyecto el Dockerfile con lo necesario.
Primero el .csproj:

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649481297586/wKLO1Fwxf.png)
Se agregaron características esenciales, por ejemplo, el objetivo del Framework, o sea net 5, o el que  hayas seleccionado y tambien el objetico de sistema operativo que hayas seleccionado, en este caso elegí Linux.

Luego, la explicación fácil del Dockerfile es:
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649480659657/lHEv0w6KM.png)

```
FROM - Descarga el runtime o el SDK
WORKDIR - Selecciona la carpeta raíz
EXPOSE - Expone los puertos necesarios
RUN - Construye el proyecto
ENTRYPOINT - Acceso a la API
```
8.Ahora vemos que tenemos una nueva opción de compilación, que es la de Docker, y si corremos ISS Express, WSL o Docker, va a correr exactamente igual, sin importar dónde y esto es lo bonito de los contenedores.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649482145045/pHHESMHn2.png)
9.Y bueno, así debe verse al final, igual que cualquier otro sistema.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649482360175/ItKJP0eHM.png)

En el siguiente video y blog, te enseñaré cómo construir y subir un contendor de Dart a Azure para que puedas acceder a él en cualquier momento ;)

Puedes crear un blog igual que este, entrando a Hashnode, ¡es gratis!

[Crea tu blog con Hashnode](https://hashnode.com/@elpincode/joinme)

Ó solicita un tutorial en español, [escríbeme](https://www.linkedin.com/in/elpincode/)

¡Saludos! :D
