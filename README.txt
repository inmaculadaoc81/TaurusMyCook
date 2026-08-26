Taurusmycooktech ONE PAGE

Dominio: https://taurusmycooktech.com.es/
Teléfono caja y botones: +34 914 46 85 03
Diagnóstico: 20 € + IVA

Variables SMTP compartidas en Vercel:
SMTP_HOST=cp7124.webempresa.eu
SMTP_PORT=465
SMTP_SECURE=true
SMTP_USER=soporte@kelatos.com
SMTP_PASS=[configurada únicamente en Vercel]
CONTACT_EMAIL=soporte@kelatos.com

El correo no aparece visible en la web; solo se utiliza en backend.

Google Analytics:
G-ZNGXWC46SX

REVISIÓN (fixes aplicados):
- Ya tenía menú móvil, colisión del chatbot corregida, schema.org y
  sección SEO (de un commit anterior); no se ha tocado nada de eso.
- El botón .navcall ya tenía white-space:nowrap heredado de .links a
  (fix de un commit anterior), así que no tenía el problema de línea
  partida visto en RowentaTech/XiaomiTech.
- Banner de cookies: no existía. Añadido (Aceptar / Rechazar / Política
  de privacidad → https://kelatos.com/privacy-policy/), con diseño
  apilado a ancho completo en móvil.

REDIRECCIÓN DE URLS ANTIGUAS:
Este sitio era antes multipágina (tenía /servicios/... y /modelos/...,
eliminados en commits anteriores al pasar a one-page). Añadido
middleware.mjs: cualquier URL que no sea "/" redirige (301) a la home.
Añadida la dependencia "@vercel/functions" en package.json.
