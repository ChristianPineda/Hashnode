---
title: "How to: Publicar página web estática en Azure Storage"
seoTitle: "Publicar página web estática en Azure Storage"
seoDescription: "Publicar página web estática en Azure Storage"
datePublished: Wed Mar 09 2022 23:21:56 GMT+0000 (Coordinated Universal Time)
cuid: cl0k6r7p908902nnvdfd7crb2
slug: how-to-publicar-pagina-web-estatica-en-azure-storage
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1646867073310/AT7DiUbFe.jpg
tags: azure, web-development, web, webdev, storage

---

Si no quieres leer el blog con las instrucciones, puedes ver el video en mi Threadit, actualizaré esta entrada de blog cuando esté disponible en mi canal de Youtube (: 

[Mira mi Threadit para esta entrada de blog ;)](https://threadit.app/thread/i6uo9ux50wbe08g1x3af/message/as352qmfr6mw9vc0eaeln0oi?utm_medium=referral-notification)

Para este video usé una página que ya había construido anteriormente para la práctica de LaunchX de Innovaccion virtual y así no fuera tedioso verme construir la página web, puedes buscar muchos templates en Google que para esta ocasión sea un **único archivo de HTML**, ya que el servicio de web estática en blob storage no admite más.

Después de descargar el template de tu elección, lo descomprimes y lo abres con Visual Studio Code o el editor de tu preferencia, recomiendo usarlo junto con la extensión Live Server.

[Descargar Visual Studio Code](https://code.visualstudio.com/download)

[Descargar Azure Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-node-azure-pack)

[Descargar Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)

Nota: En este servicio no se pueden usar carpetas ni poner otros archivos que no sean el index y el 404 (al menos hasta donde yo pude intentar)

1. Crea tu recurso desde el portal de Azure, recuerda que necesitas tener ya una cuenta:

2. [Crea tu cuenta de almacenamiento entrando aquí](http://portal.azure.com/)

3. Al entrar busca el servicio Azure Storage en el panel izquierdo y da click en él

4. Configura tu suscripción (lo más seguro es que solo tengas una)

5. Selecciona un grupo de recursos

6. Dale un nombre cool ;)

7. Elige la ubicación adecuada, la más cercana a ti o a tu público objetivo
8. Busca "Sitio Web Estático" y da click
9. Crea tus archivos index y 404 (no podrás editarlo)
10. En Visual Studio code abre tu extensión Azure Tools, en tu cuenta de Storage>Contenedores>Web notarás que no hay nada
11. Abre el portal de Azure y selecciona "Contenedores" y luego en "Web" en el panel de servicios de tu Azure Storage, ahí podrás cargar tus dos archivos HTML
12. Actualiza tu página para verificar los archivos
13. Verifica que tu servicio esté ya disponible en línea
14. Agrega tu propio dominio a tu servicio, desde la pestaña red y dominio personalizado (el tiempo de espera depende de tu proveedor)

Si alguien cree que hay más cosas que hacer en este servicio o hacer alguna corrección, podría compartirnos :D

Puedes crear un blog igual que este, entrando a Hashnode, ¡es gratis!

[Crea tu blog con Hashnode](https://hashnode.com/@elpincode/joinme)

Ó solicita un tutorial en español, [escríbeme](https://www.linkedin.com/in/elpincode/)

¡Saludos! :D