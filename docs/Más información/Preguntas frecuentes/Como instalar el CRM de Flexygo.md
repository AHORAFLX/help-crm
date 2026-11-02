# Como instalar el CRM de Flexygo

Ahora CRM by Flexygo es la herramienta completa y definitiva para tu equipo de ventas. Es una aplicación creada y diseñada para facilitar y acelerar la venta de los equipos comerciales. Concentre en una sola aplicación Web toda la actividad comercial, sus agendas, sus empleados y la gestión de reserva de recursos. Analice cómodamente la previsión de ventas de su departamento comercial mediante los cuadros de mando que integra de forma estándar.

Ahora CRM está pensada para funcionar tanto con el modelo de datos de [Ahora ERP](http://www.ahora.es/), como con el propio modelo de datos de CRM.

## REQUISITOS PREVIOS

El servidor donde se realiza la instalación de CRM debe tener:

- **Internet Information Services (IIS)**, con la característica **WebSocket** habilitada. Si no está instalado, el instalador puede instalarlo.
- **SQL Server 2017 o superior**. A partir de la versión 10, las bases de datos de la aplicación deben estar en un servidor SQL Server 2017 o posterior. El instalador puede instalar SQL Server Developer Edition para entornos de pruebas.
- **.NET Hosting Bundle**. El instalador lo instala automáticamente si no lo encuentra.
- Permisos de administrador en el equipo.

Si trabaja con AHORA ERP, mantenga su base de datos actualizada para garantizar el correcto funcionamiento de las nuevas versiones de CRM.

Puede consultar todos los requisitos en la [ayuda de Flexygo: Requisitos del sistema](https://ayuda.ahora.es/Flexygo/latest/1Deployment/SystemRequirements/).

## INSTALADOR

El CRM se instala con el instalador de Flexygo. Puede descargarlo desde la [ayuda de Flexygo](https://ayuda.ahora.es/Flexygo/latest/) o directamente en la siguiente dirección: <https://ayuda.ahora.es/Flexygo/files/flexygoinstallercore.zip>

1. Descomprima el archivo `.zip` y ejecute el instalador como administrador.
2. Elija el modo **Despliegue** y seleccione el producto **CRM** en la lista de productos.
3. Elija el modo de instalación:
    - **IIS Básico:** instala el Frontend y el Backend en el mismo servidor y sitio IIS. Indique el nombre del proyecto, el sitio web, el path virtual y el directorio físico.
    - **IIS Avanzado:** permite instalar el Frontend y el Backend en servidores o sitios distintos, instalar IIS o SQL Server si faltan, o instalar una versión concreta del producto.
    - **Docker:** despliega la aplicación en Docker Desktop, para demos, pruebas o desarrollo local.
4. Al terminar, el instalador muestra un resumen y ofrece abrir la aplicación en el navegador.

Tiene el detalle de cada pantalla en la [ayuda de Flexygo: Instalador, modo Despliegue](https://ayuda.ahora.es/Flexygo/latest/1Deployment/1Installer/Deployment/).

## ASISTENTE DE CONFIGURACIÓN

La primera vez que se accede a la aplicación se abre el asistente de configuración, que guía en cinco pasos:

1. **Conexión con el backend:** la dirección del frontend y la del backend.
2. **Base de datos de configuración:** el servidor SQL Server, el usuario, la contraseña y el nombre de la base de datos. Si no existe, el asistente la crea; si es de una versión anterior, la actualiza.
3. **Proyecto y administrador:** el nombre del proyecto y la contraseña del usuario `admin`.
4. **Bases de datos de datos:** la base de datos con la que trabaja el CRM.
    - Si trabaja con **AHORA ERP**, indique su base de datos. Debe existir: el asistente no crea bases de datos del ERP.
    - Si usa el **modelo de datos propio del CRM**, indique el nombre de su base de datos.
5. **Correo saliente:** la cuenta para recuperar contraseñas y enviar notificaciones. Es opcional y puede configurarse más tarde.

Al terminar, entre en la aplicación con el usuario `admin` y la contraseña indicada. Tiene el detalle de cada paso en la [ayuda de Flexygo: Asistente de configuración](https://ayuda.ahora.es/Flexygo/latest/1Deployment/2ConfigWizard/Configuration/).

## ACTUALIZACIONES

Mantenga el producto CRM actualizado. Puede consultar cómo se actualiza la aplicación en la [ayuda de Flexygo: Flujo de actualización](https://ayuda.ahora.es/Flexygo/latest/1Deployment/3Updater/UpdateFlow/).

!!! note "Nota"
    CRM no reemplaza ni actualiza CRMExpress. Es un nuevo producto, con una nueva tecnología, y se instala como una aplicación independiente.
