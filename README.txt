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

REVISIÓN ADICIONAL (esta pasada, auditoría a petición del cliente —
sin tocar el diseño del hero):
- H1 no cumplía la regla final de la familia: era largo (21 palabras),
  con planteamiento en forma de pregunta implícita y la palabra
  condicional "si merece la pena". Reescrito, corto y afirmativo:
  "Tu Taurus Mycook ya no cocina. Aquí lo reparamos rápido." No se ha
  tocado el tamaño de fuente ni ningún otro estilo del hero.
- BUG REAL — .navcall (píldora de teléfono del menú) mostraba el texto
  largo "Atención Telefónica 24 horas 365 días" en vez de solo el
  número, igual que el patrón visto en otros repos de la familia
  (RowentaTech/XiaomiTech); aunque heredaba white-space:nowrap y no se
  partía en dos líneas, sí podía ensanchar la píldora y apretar el
  resto del menú. Acortado a solo "+34 914 46 85 03" (mismo href
  tel:, número sin modificar).
- BUG REAL — el chat n8n no tenía borde blanco en el botón flotante
  (#n8n-chat .chat-window-toggle sin la propiedad border), a
  diferencia del resto de la familia. Añadido
  border:1px solid #fff!important.

REDIRECCIÓN DE URLS ANTIGUAS:
Este sitio era antes multipágina (tenía /servicios/... y /modelos/...,
eliminados en commits anteriores al pasar a one-page). Añadido
middleware.mjs: cualquier URL que no sea "/" redirige (301) a la home.
Añadida la dependencia "@vercel/functions" en package.json.
