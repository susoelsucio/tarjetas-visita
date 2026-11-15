# Tarjetas a contactos

Web app personal para el móvil: haces una foto a una tarjeta de visita y descargas un contacto (`.vcf`) listo para importar en Google Contactos. Funciona con la IA Gemini de Google y no necesita servidor ni instalación.

*English summary: a single-page web app that reads a business card photo with the Gemini API and generates a vCard (.vcf) file to import into your contacts. You bring your own free Gemini API key.*

**Prueba la app:** https://susoelsucio.github.io/tarjetas-visita/

## Cómo se usa

1. Consigue una clave API gratuita de Gemini en [aistudio.google.com](https://aistudio.google.com) (entra con tu cuenta de Google, pulsa *Get API key*). No pide tarjeta de crédito.
2. Abre la web, despliega **Ajustes**, pega tu clave y pulsa **Guardar ajustes**.
3. Pulsa **Hacer foto** (o **Elegir de la galería**) y fotografía la tarjeta.
4. Revisa los datos, corrige lo que haga falta y pulsa **Descargar contacto**.
5. Abre el archivo `.vcf` descargado y elige **Contactos** para importarlo.

En Chrome para Android puedes añadirla a la pantalla de inicio desde el menú (⋮) con **Instalar aplicación**.

## Qué hace

- Extrae nombre, apellidos, cargo, empresa, teléfonos, emails, webs y dirección.
- Si la tarjeta solo tiene empresa, usa el nombre de la empresa también como nombre del contacto.
- Permite elegir el modelo de Gemini y, si uno está saturado o no existe, prueba automáticamente con otros.
- Admite varias fotos a la vez (un contacto por tarjeta).

## Privacidad

- Tu clave de Gemini se guarda **solo en tu navegador** (almacenamiento local). No está en este repositorio ni se envía a ningún sitio salvo a Google.
- Las fotos se envían directamente desde tu móvil a la API de Gemini. Este proyecto no tiene servidor y no guarda ni ve tus fotos ni tus contactos.
- Con la capa gratuita de Gemini, Google puede usar los datos enviados para mejorar sus productos (consulta sus condiciones). Ten en cuenta que las tarjetas contienen datos de terceros.

## Tecnología

Un único archivo `index.html` con HTML, CSS y JavaScript, sin dependencias. Llama a la API REST de Gemini y genera un vCard 3.0 en el navegador.

## Aviso

Proyecto personal, ofrecido tal cual, sin garantías ni soporte. Los nombres de los modelos de Gemini y los límites de la capa gratuita cambian con el tiempo; si algo deja de funcionar, prueba con otro modelo en Ajustes.

## Licencia

[MIT](LICENSE): software libre, puedes usarlo, copiarlo y modificarlo libremente.
