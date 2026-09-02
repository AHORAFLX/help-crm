# Google Integration Console

Para configurar su App en Google Cloud, previa a la [integración con Google](Integraci%C3%B3n%20con%20Google.md), debe seguir los siguientes pasos.

## Crear un proyecto nuevo

- Al ingresar por primera vez hay que aceptar los Términos y Servicios.
- Seleccionar / Crear proyecto.

![](../docs_assets/images/Ayuda/Google/SeleccionarProyecto.png)
*Fig.1 - Seleccionar proyecto.*

![](../docs_assets/images/Ayuda/Google/CrearProyecto.png)
*Fig.2 - Crear proyecto.*

## Configurar consentimiento

- Configurar las credenciales desde el apartado **APIs Services** - **Pantalla de consentimiento**.
- Seleccionar el tipo Externo y crear.

![](../docs_assets/images/Ayuda/Google/CrearConsentimiento.png)
*Fig.3 - Crear consentimiento.*

- En la siguiente pantalla, rellenar los campos requeridos. Si se rellena el campo logo, deberá verificar la aplicación siguiendo los criterios de verificación de Google.

![](../docs_assets/images/Ayuda/Google/CrearConsentimiento_2.png)
*Fig.4 - Información de App.*

- La siguiente pantalla la dejamos como está.
- En esta pantalla incluir el correo de los usuarios que van a usar la integración; los usuarios que no estén incluidos no tendrán acceso (solo mientras la publicación esté en modo Prueba).

![](../docs_assets/images/Ayuda/Google/CrearConsentimiento_3.png)
*Fig.5 - Incluir usuarios.*

- En la última pantalla tendremos un resumen de la configuración; si está todo correcto, pulsamos **Volver**.

![](../docs_assets/images/Ayuda/Google/CrearConsentimiento_4.png)
*Fig.6 - Resumen consentimiento.*

## Publicar

Para que cualquier usuario pueda usar la integración hay que publicarla, por lo que el apartado de usuarios de prueba ya no hace falta mantenerlo.

![](../docs_assets/images/Ayuda/Google/PublicarApp.png)
*Fig.7 - Publicar.*

![](../docs_assets/images/Ayuda/Google/ConfirmarPublicacion.png)
*Fig.8 - Confirmar publicación.*

## Configurar credenciales

- Para poder usar los servicios de Google hay que configurar las credenciales del tipo *OAuth client ID* desde el apartado **APIs Services** - **Credentials**.
- Rellenar los campos correspondientes; en el apartado de URIs, sustituir el texto seleccionado por la URL de su aplicación.

![](../docs_assets/images/Ayuda/Google/CrearCredenciales.png)
*Fig.9 - Crear credenciales.*

Una vez creado, obtendremos unas claves las cuales debemos copiar en los settings de Flexygo:

<flx-navbutton type="execprocess" processname="sysEditSettings" objectname="sysSettings" objectwhere="(Settings.[SettingName] IN ('GoogleClient', 'GoogleSecret'))" targetid="popup" excludehist="false" showprogress="false">
    <span class="clickable txt-outstanding hover-underline">Settings de Flexygo</span>
</flx-navbutton>

![](../docs_assets/images/Ayuda/Google/InfoOAuth.png)
*Fig.10 - Info OAuth.*

## Habilitar API para Contactos y Calendario

Por último, habilitar la API de Contactos y Calendario desde el apartado de Biblioteca.

![](../docs_assets/images/Ayuda/Google/IrBiblioteca.png)
*Fig.11 - Biblioteca.*

![](../docs_assets/images/Ayuda/Google/EnabledContactAPI.png)
*Fig.12 - Habilitar API Contactos.*

![](../docs_assets/images/Ayuda/Google/EnabledCalendarAPI.png)
*Fig.13 - Habilitar API Calendario.*
