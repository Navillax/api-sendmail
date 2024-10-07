# Web Service de Envío de Correo 👋 😃 📨

\*Este es un web service desarrollado en PHP para el envío de correos electrónicos. El servicio recibe una solicitud HTTP que contiene el nombre, correo electrónico y el mensaje, valida los datos y envía un correo.

### Descripción

Este web service permite recibir datos y enviar un correo electrónico utilizando la función `mail` de PHP.

---

### <🛠> Instalación </🛠>

1. Clona el repositorio o descarga el archivo PHP.
2. Sube el archivo PHP a tu servidor web.
3. Asegúrate de tener configurado un servidor web con soporte para PHP.
4. Modifica la variable `$webmaster_email` con la dirección de correo del webmaster.

   ```php
   $webmaster_email = 'tu_correo@dominio.com';
   ```

5. Verifica que tu servidor tenga habilitado el envío de correos a través de la función `mail`.

---

### <📊> Uso </📊>

Estos son algunos de los resultados que recibirás tras realizar diferentes pruebas:

```json
{
  "name": "Tu Nombre",
  "email": "tu_correo@dominio.com",
  "message": "Tu mensaje aquí"
}

✅👍 Éxito:

{
  "status": "success",
  "message": "Correo enviado correctamente."
}
❌🗄️ Error en los datos:

{
  "status": "error",
  "message": "Datos inválidos."
}

❌📩 Error en el envío del correo:

{
  "status": "error",
  "message": "Error al enviar el correo."
}
```

---

### <📫> Ejemplo de solicitud desde un cliente HTTP </📫>

```http

POST    http://localhost/api/v1/endpoint-webservice/
Content-Type: "application/json"

{
    "name":"Odofre Tamayo",
    "email":"odofregofre@ejemplo.com",
    "message":"Mi nombre significa buen hombre."
}

```

---

## ¡Hasta luego! 😎
