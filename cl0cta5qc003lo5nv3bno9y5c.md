---
title: "How to: Publicar página web estática con Azure Static Web Apps, CI/CD, Github Actions, Dominio y SSL."
seoTitle: "How to: Publicar página web estática con Azure Static Web Apps, CI/CD,"
seoDescription: "How to: Publicar página web estática con Azure Static Web Apps, CI/CD,"
datePublished: Fri Mar 04 2022 19:30:22 GMT+0000 (Coordinated Universal Time)
cuid: cl0cta5qc003lo5nv3bno9y5c
slug: how-to-publicar-pagina-web-estatica-con-azure-static-web-apps-cicd-github-actions-dominio-y-ssl
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1646418930351/Eyh-vAif_.png
tags: github, azure, github-actions-1

---

Si no quieres leer el blog con las instrucciones, puedes ver el video en mi Threadit, actualizaré esta entrada de blog cuando esté disponible en mi canal de Youtube (:
[Mira mi Threadit para esta entrada de blog ;)](https://threadit.app/thread/bua1a2mgb8yb6ulold97/message/tv13ms03kt4dh7f3cyt1i275?utm_medium=referral-link)

También puedes ver algo parecido (pero incompleto, debo agregar XD) en mi participación, en la hora 3 de la [Azure Cloud Week 2022](https://www.youtube.com/watch?v=TPBVx-a4WTk)

[Más información de Azure Static Web Apps](https://azure.microsoft.com/en-us/services/app-service/static/)

Azure Static Web Apps es un servicio **gratuito** para proyectos personales, puede ser el servicio perfecto para que construyas tu CV o hagas tu portafolio como desarrollador.

Para este video usé un template para que no fuera tedioso y largo verme construir la página web, puedes buscar muchos templates en Google o ir a esta página:

[Templates](https://html5up.net/)

Después de descargar el template de tu elección, lo descomprimes y lo abres con Visual Studio Code o el editor de tu preferencia, recomiendo usarlo junto con la extensión Live Server.

[Descargar Visual Studio Code](https://code.visualstudio.com/download)

[Descargar Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)

1. Crea tu recurso desde el portal de Azure, recuerda que necesitas tener ya una cuenta:

[Crea tu Azure Static Web App entrando aquí](http://portal.azure.com/) 

Al entrar busca el servicio y da click en el 

2. Configura tu suscripción (lo más seguro es que solo tengas una)

3. Selecciona un grupo de recursos

4. Dale un nombre cool ;)

5. Elige la ubicación adecuada, la más cercana a ti o a tu público objetivo

6. Conecta tu cuenta de Github y selecciona tu repositorio 

- Crea tu repositorio (antes de buscarlo en Azure)
- Sube los archivos de tu página web (add, commit y push)
- Actualiza tu página para verificar los archivos

7. Selecciona tu rama en el portal de Azure
8. Revisa y crea tu servicio
9. Verifica que tu servicio esté ya disponible en línea
10. Agrega tu propio dominio a tu servico, desde la pestaña dominios personalizados (el tiempo de espera depende de tu proveedor)
11. Recuerda que el certificado de seguridad (SSL) es gratis y se configura de forma automática
12. Verifica el deploy en tu workflow de Github Actions.
El archivo .yml es lo más importante en este servicio, ya que tiene toda configuración necesaria para desplegar actualizaciones.
13. ¡Ya tienes todo listo! 
Ahora puedes modificar todo lo que necesites para tu página web y añadir nuevas características 

Te sugiero comenzar a utilizar git flow para mantener un orden en tu creación de características nuevas.
[Aprende rápido a usar Gitflow](http://danielkummer.github.io/git-flow-cheatsheet/)

Puedes ver mi CV (no actualizado) [aquí](https://cv.oslomx.tech)

Una demo de una app web con Flutter, montada en Azure Static Web Apps [aquí](https://demo.oslomx.tech)

Y una página de mis servicios [aquí](https://portal.oslomx.tech)

Puedes crear un blog igual que este, entrando a Hashnode, ¡es gratis! 

[Crea tu blog con Hashnode](https://hashnode.com/@elpincode/joinme)
 
Ó solicita un tutorial en español, [escríbeme](https://www.linkedin.com/in/elpincode/)

¡Saludos! :D