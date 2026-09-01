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

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente):
- H1 repetía la plantilla "X. Aquí Y." usada en varios repos ("Tu
  Taurus Mycook ya no cocina. Aquí lo reparamos rápido."). Reescrito
  en formato imperativo, incluye la marca: "Repara tu Taurus Mycook
  con diagnóstico incluido." (7 palabras).
- BUG REAL — texto decorativo gigante ".care-art:before" ("COCINA",
  105px) sin ninguna reducción de tamaño en tablet/móvil. Añadida
  (64px tablet, 44px móvil). El badge legible ".care-art:after"
  ("CALENTAMIENTO · CUCHILLAS · BÁSCULA · PANTALLA") no es un
  watermark, no se ha tocado.
- BUG REAL — el botón CTA de teléfono no tenía icono, a diferencia del
  de WhatsApp. Añadido (verificado con cuidado el cierre de las
  etiquetas </a>: 20 aperturas / 20 cierres).
- BUG REAL — la casilla de política de privacidad existía pero el
  texto no enlazaba a ningún sitio. Añadido el enlace estándar de la
  familia a https://kelatos.com/privacy-policy/, resaltado en azul.
- Añadida franja de aviso de servicio técnico independiente debajo del
  menú (no existía). Verificado antes que .header no usa
  display:flex directamente.
- Añadido "Sábados, domingos y días festivos estamos cerrados" debajo
  del horario.
- Verificado sin bugs: .hero-shape es un círculo decorativo sin texto
  (no hay ninguna etiqueta rotada tipo hero-chip en este repo); el
  ticker ".hero:after" ya se ocultaba correctamente en móvil; Cal.com
  ya estaba presente; schema.org ya usaba correctamente el único
  teléfono de este repo; formulario correctamente conectado a
  /api/contacto.

REDIRECCIÓN DE URLS ANTIGUAS:
Este sitio era antes multipágina (tenía /servicios/... y /modelos/...,
eliminados en commits anteriores al pasar a one-page). Añadido
middleware.mjs: cualquier URL que no sea "/" redirige (301) a la home.
Añadida la dependencia "@vercel/functions" en package.json.

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente — repo 23/48):
- BUG REAL — enlace de Cal.com desactualizado. Actualizado a
  https://cal.com/kelatos/30min?embed=true&theme=light&attendeePhoneNumber=%2B34&overlayCalendar=true.
- Verificado: el correo soporte@kelatos.com no aparece visible.
- BUG REAL — el mensaje prellenado de WhatsApp decía "¡Hola Kelatos!".
  Corregido a "¡Hola Taurusmycooktech!".
- Verificado: el menú móvil ya se cerraba correctamente al pulsar un
  enlace.
- Verificado: sin iconos ni imágenes con proporciones fijas
  incorrectas.
- BUG REAL — el H1 en móvil estaba en 40px. Corregido a 48px.
- BUG REAL — botones del hero (.cta) con border-radius de 16px y sin
  estado hover. Aumentado a border-radius:999px; añadido
  filter:brightness(.88) en wa/pickup (colores sólidos) y relleno
  sólido con var(--navy) + texto blanco en el botón de teléfono
  (estilo contorno) al pasar el ratón.
- Verificado: este repo no usa el patrón de franja de insignias bajo
  el H1 (familia Dyson); no aplica la reubicación.
