# 07 — Calendario y Citas

## Índice

- [Módulo Calendario](#módulo-calendario)
- [Integración con Google Calendar](#integración-con-google-calendar)
- [Eventos en Calendario](#eventos-en-calendario)
- [Módulo Citas](#módulo-citas)

## Módulo Calendario

1. Entramos desde el panel principal al módulo de Calendario, nos aparecerá **esta vista**:

![Calendario](../assets/img/07-calendario_y_citas/paso01_vista-calendario.png)

2. Desde la pestaña que aparece en la imagen, **podemos cambiar la vista**:

![Vista mensual](../assets/img/07-calendario_y_citas/paso02_cambiar-vista.png)

3. Podemos compartir nuestra **disponibilidad**. Desde esta pestaña Compartir en la izquierda de la pantalla, le damos a **My Calendar**, se nos generará un **enlace** y se nos copiará automáticamente en el **portapapeles**.

![Compartir](../assets/img/07-calendario_y_citas/paso03_compartir-calendario.png)

4. Si entramos en ese enlace, nos aparecerá esta vista para **reservar una reunión** y **compartirla**.

![Enlace](../assets/img/07-calendario_y_citas/paso04_enlace-compartir.png)

## Integración con Google Calendar

5. Lo siguiente será **vincular** el calendario **con Google**. Para ello nos vamos a [Google Console](https://console.cloud.google.com/) y creamos un nuevo proyecto como hicimos en el **punto 9** de [05 — Integración con Gmail](05-integracion_gmail.md). Le asignamos, por ejemplo: **Odoo Calendar**.

![Crear proyecto](../assets/img/07-calendario_y_citas/paso05_crear-proyecto.png)

![Nombrar proyecto](../assets/img/07-calendario_y_citas/paso05_nombrar-proyecto.png)
6. Una vez creado **muy importante** haber cambiado de proyecto porque aún seguimos en el proyecto de cuando vinculamos Gmail, y buscamos **Google Calendar API**.

![Buscar plugin](../assets/img/07-calendario_y_citas/paso06_buscar-plugin.png)

7. Habilitamos el **plugin**.

![Habilitar plugin](../assets/img/07-calendario_y_citas/paso07_habilitar-plugin.png)

8. Pulsamos sobre **crear credenciales**, situado a la derecha.

![Crear credenciales](../assets/img/07-calendario_y_citas/paso08_crear-credenciales.png)

9. Seleccionamos el **tipo de credencial**, seleccionando a **datos de los usuarios** y le damos a **siguiente**.

![Tipo de credencial](../assets/img/07-calendario_y_citas/paso09_tipo-credencial.png)

10. Rellenamos la **información de la aplicación**: nombre de la app y nuestro correo. Acto seguido **Guardar y continuar**.

![Datos aplicación](../assets/img/07-calendario_y_citas/paso10_datos-aplicacion.png)

11. Agregamos **permisos**. Le daremos permisos nuestra información de Google (**openid**), procedemos a **buscar** por filtro **Google Calendar API** y seleccionaremos **todos los permisos** de las dos páginas. Y finalmente a **Actualizar**.

![Permiso información personal de Google](../assets/img/07-calendario_y_citas/paso11_info-personal-google.png)

![Permisos GoogleCalendar](../assets/img/07-calendario_y_citas/paso11_permisos-api1.png)

![Permisos GoogleCalendar](../assets/img/07-calendario_y_citas/paso11_permisos-api2.png)

12. Nos aparecerá una lista larga de todos los permisos, abajo del todo, pulsamos **Guardar y continuar**.

![Guardar y continuar](../assets/img/07-calendario_y_citas/paso12_guardar-y-continuar.png)

13. En el siguiente paso, el tipo de aplicación seleccionamos **Aplicación web**, seleccionamos un **nombre** y agregamos una **URI de redireccionamiento**, que será la siguiente:

	- Al dominio de nuestra empresa en Odoo: https://ejemplo.odoo.com/
	- Le añadimos lo siguiente: **google_account/authentication**
	- Quedaría así: https://empresa-ejemplo1.odoo.com/google_account/authentication

Después de eso, le damos a **Crear**.

![Guardar y continuar](../assets/img/07-calendario_y_citas/paso13_id-cliente-oauth.png)

14. Nos dan nuestro **ID de cliente**, y le damos a **Listo**.

![Tus credenciales](../assets/img/07-calendario_y_citas/paso14_tus-credenciales.png)

15. **Ya está creada** la credencial, nos lleva a esta página, le damos a **Credenciales** y pulsamos sobre la que acabamos de crear:

![Odoo Calendario](../assets/img/07-calendario_y_citas/paso15_credencial-odoo-calendario.png)

16. Aquí tendríamos el ID de cliente y el secreto del cliente:

![ID y secreto del cliente](../assets/img/07-calendario_y_citas/paso16_id-y-secreto.png)

17. Nos dirigimos a **Ajustes**, en la sección **Calendario**. Y a la derecha pegamos el **ID y secreto de cliente** donde corresponde. Muy **importante** pulsa **guardar** en la esquina superior izquierda.

![Ajustes de Calendario](../assets/img/07-calendario_y_citas/paso17_ajustes-de-calendario.png)

## Eventos en Calendario

18. Para crear un **evento** en el calendario de Odoo, nos dirigimos al módulo de **Calendario** nuevamente, y con pulsar en el calendario ya estaríamos creando un evento. Para añadir **videollamada** de Odoo, tan solo hay que hacer click al botón **Vídeo** de color verde y se nos creará un enlace. Cuando tengamos todos listo, le damos a **guardar**.

![Nuevo evento](../assets/img/07-calendario_y_citas/paso18_nuevo-evento.png)

19. Se nos crea el evento y podemos **unirnos a la videollamada por** enlace.

![Evento creado](../assets/img/07-calendario_y_citas/paso19_evento-creado.png)

20. Al pulsarle sobre el enlace nos saldrá la típica página para preparar cámara y micrófono y finalmente nos une a la **llamada**.

![Videollamada de Odoo](../assets/img/07-calendario_y_citas/paso20_videollamada.png)

21. Si colgamos, nos aparecerá el **chat de la reunión** con más opciones como **configuración** básica, notificaciones, invitar a más personas, volver a entrar en la llamada, etc. En la barra lateral izquierda están los **otros chats**, en este caso están el general para todos los empleados, el de administradores y el con OdooBot, a parte del chat del evento.

![Chat de evento de Odoo](../assets/img/07-calendario_y_citas/paso21_chat-evento.png)

22. Si volvemos a hacer click al evento como en la imagen del **paso 21**, podemos **editarlo**. Podemos añadir a gente, la duración, podemos poner **recordatorios** cada cierto tiempo, **por notificación, por correo o por SMS**. Enviar mensajes, email, etc. También desde aquí podemos **eliminar el enlace de la Reunión de Odoo** para poder poner el **enlace de otra plataforma**.

![Editar evento](../assets/img/07-calendario_y_citas/paso22_editar-evento.png)

## Módulo Citas

23. Entramos desde el panel principal de Odoo al módulo de **Citas**. Nos encontraremos con esta pantalla. Para crear una, nos dan varias opciones, por ejemplo le pulsaremos a **Reunión**.

![Citas](../assets/img/07-calendario_y_citas/paso23_citas.png)

24. Una vez dado, se nos **crea instantáneamente una reunión**, le podemos cambiar el **nombre**, establecer una **duración**, poder elegir entre una reunión con alguien o reservar un recurso, enlace por **Google Meet** o por **Odoo Conversaciones**. Poder establecer **disponibilidad** por días y horas, etc. En el apartado de opciones hay sobre **programar** **reuniones** semanalmente o de forma flexible, permitir reservas cada cierto tiempo, no permitir cancelación hasta cierto tiempo antes de la reunión, etc

![Configuración cita](../assets/img/07-calendario_y_citas/paso24_configuracion-cita.png)

25. Para compartir esta reunión con quien la tengamos (en este caso conmigo mismo), me **añado** a mí mismo en **usuarios**, y luego le doy a **compartir**. Me ponen un **enlace para copiarlo**, y lo pego en otra pestaña del navegador. Selecciono **día y hora** y me cambia de pantalla para **confirmar**.

![Reservar reunión](../assets/img/07-calendario_y_citas/paso25_reservar-reunion.png)
26. Rellenamos el campo de **número de teléfono** y le damos a **confirmar cita**.

![Confirmar cita](../assets/img/07-calendario_y_citas/paso26_confirmar-cita.png)

27. Ya está la **cita confirmada**.

![Cita programada](../assets/img/07-calendario_y_citas/paso27_cita-programada.png)

28. Si vamos al calendario, veremos la cita.

![Cita programada en calendario](../assets/img/07-calendario_y_citas/paso28_cita-en-calendario.png)
