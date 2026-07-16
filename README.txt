M3 WORKSHOP — cómo publicar y gestionar tu web
==============================================

CONTENIDO DE ESTA CARPETA
  index.html          → tu web
  admin/              → el panel de administración (no tocar)
  content/works.json  → los datos de obras y tienda (los edita el panel)
  images/             → aquí se guardan las fotos que subas
  DarkMother.woff2    → (opcional) pon aquí tu fuente Dark Mother


PUESTA EN MARCHA — SE HACE UNA SOLA VEZ
---------------------------------------

1) SUBIR A GITHUB
   - Crea una cuenta en github.com
   - New repository → nombre: m3workshop → Public → Create
   - En la página del repo: "uploading an existing file"
   - Arrastra TODO el contenido de esta carpeta → Commit changes

2) CONECTAR NETLIFY
   - Entra en netlify.com con tu cuenta de GitHub
   - Add new site → Import an existing project → GitHub → elige m3workshop
   - Deja todo vacío → Deploy
   - Ya tienes la web online en una dirección .netlify.app

3) ACTIVAR EL PANEL (Identity)
   En Netlify, dentro de tu sitio:
   - Site configuration → Identity → Enable Identity
   - Identity → Registration → ponlo en "Invite only"
     (importante: si no, cualquiera podría registrarse)
   - Identity → Services → Git Gateway → Enable Git Gateway
   - Identity → Invite users → invítate con tu email
   - Te llega un email → aceptas → creas tu contraseña

4) CONECTAR TU DOMINIO
   - Domain management → Add a domain → m3workshop.art
   - Netlify te dará unos registros DNS
   - Entra en Porkbun → tu dominio → DNS → añade esos registros
   - Espera de 10 min a un par de horas. El HTTPS se activa solo.


USO DIARIO
----------
Entra en:  m3workshop.art/admin

Desde ahí puedes, sin tocar código:
  - Añadir una obra nueva (botón "Add Obra")
  - Subir la foto del cuadro
  - Escribir título, técnica, medidas, año, precio
  - Marcar una obra como VENDIDA (aparece el sello "Collected")
  - Reordenar las obras arrastrándolas
  - Editar los productos de la tienda

Pulsa "Publish" y en 1-2 minutos está online.
Funciona también desde el móvil.


LA FUENTE DARK MOTHER
---------------------
Si tienes el archivo de la fuente:
  1. Renómbralo a  DarkMother.woff2
  2. Súbelo a la raíz del repositorio (junto a index.html)
  3. Listo, la web la usa sola.
Mientras tanto usa Grenze Gotisch, que es muy parecida.
Ojo: asegúrate de tener licencia WEB de la fuente antes de usarla en un sitio público.


COBRAR LOS CUADROS
------------------
En el panel, cada producto tiene un campo "Enlace de pago".
  - Crea una cuenta en Mollie (va muy bien en NL, acepta iDEAL) o Stripe
  - Genera un payment link para cada obra
  - Pega el link en ese campo
Si lo dejas vacío, el botón "Acquire" abre un email a hello@m3workshop.art
