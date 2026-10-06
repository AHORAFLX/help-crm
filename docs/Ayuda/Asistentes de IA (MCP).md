# Asistentes de IA conectados al CRM (MCP)

Puedes conectar al CRM tu propio asistente de IA (Claude, ChatGPT, Gemini o cualquier otro compatible con **MCP**, el *Model Context Protocol*) y preguntarle por tus datos en lenguaje normal: «¿qué tengo pendiente hoy?», «¿cómo va el embudo de ventas?», «resúmeme la cuenta García», «registra una llamada a Acme para mañana».

El asistente entra **con tu usuario del CRM** y ve y hace exactamente lo mismo que tú en la aplicación, nada más.

!!! note "No es el asistente integrado"
    El CRM también trae asistentes propios dentro de la aplicación, que usan OpenAI: ver [Inteligencia artificial](Inteligencia%20artificial.md). Esta página trata de lo contrario: tu asistente de siempre, fuera del CRM, trabajando con los datos del CRM.

## Qué le puedes pedir

El asistente conoce el CRM: sabe qué son las cuentas, los potenciales, las actuaciones, las oportunidades con sus fases, las ofertas, los gastos y las reservas, porque el CRM le da una descripción de cada cosa. Algunos ejemplos:

| Le pides | Qué hace |
|---|---|
| «¿Qué actuaciones tengo pendientes esta semana?» | Lista tus llamadas, visitas, reuniones y tareas pendientes |
| «¿Cómo va el embudo de ventas?» | Número e importe de las oportunidades por fase |
| «Resúmeme la cuenta García» | Busca la cuenta y te cuenta sus contactos, la última actividad, las oportunidades abiertas y las ofertas |
| «¿Qué oportunidades cierran este mes?» | Las oportunidades abiertas con fecha prevista de cierre en el mes |
| «¿Qué tiene pendiente de cobro Acme?» | Los cobros pendientes de la cuenta |
| «Registra una visita a Acme el jueves a las 10» | Crea la actuación (si tienes permiso de modificar) |
| «Hazme un tablero de mis oportunidades» | Cifras, desgloses y tablas; en Claude web o escritorio, como un tablero interactivo |

Además, el CRM ofrece al asistente unas **tareas típicas**, que la mayoría de asistentes muestran como atajos:

- Agenda de hoy
- Embudo de ventas
- Oportunidades que cierran pronto
- Resumen de una cuenta
- Cobros pendientes de una cuenta
- Registrar una llamada o visita
- Dar de alta una cuenta

## Activarlo (administrador)

Lo hace un administrador en **Work Area › Admin Work Area › Security › WebAPI**, la misma pantalla que la [Web API](Web%20API.md):

![](../docs_assets/images/Ayuda/WebAPI/configuracion-webapi.png)
*Fig.1 - Habilitar MCP y el permiso de asistentes (columna del robot).*

1. Enciende **Enable WebAPI** y **Habilitar MCP**. Los dos vienen apagados: conectar asistentes de IA es una decisión de cada empresa.
2. En **Personas autorizadas**, marca la columna del **robot** en los roles (pestaña **Papeles autorizados**) o en los usuarios (pestaña **Usuarios autorizados**) que pueden conectar un asistente. Es un permiso aparte del de la API (el ojo). **De serie, ningún rol lo tiene**: solo el usuario administrador.

No hay que preparar nada más: el CRM ya trae publicados sus objetos, vistas y procesos, con sus descripciones y las tareas típicas.

## Conectar tu asistente

1. En la aplicación, abre tu menú de perfil y elige **Conectar un asistente**. Copia la dirección que aparece: es la de la aplicación terminada en `/mcp`, por ejemplo `https://crm.miempresa.com/mcp`.
2. Añade esa dirección en tu asistente:
    - **Claude (web o escritorio):** *Ajustes › Conectores › Añadir conector personalizado*.
    - **ChatGPT, Gemini y otros:** en su apartado de conectores o aplicaciones, con la misma dirección.
    - **Claude Code:** `claude mcp add --transport http crm https://crm.miempresa.com/mcp`.

    Los asistentes en la nube (Claude web, ChatGPT…) se conectan desde internet: la aplicación tiene que estar publicada con HTTPS y accesible desde fuera.

3. El asistente abre el navegador: entra con **tu usuario del CRM** y verás la página de consentimiento, con quién pide acceso y qué se le concede. Pulsa **Permitir**. Si desmarcas **Modificar datos**, el asistente solo podrá consultar.

## Qué ve el asistente

Lo mismo que tú, con las mismas reglas que la aplicación y la [Web API](Web%20API.md#la-seguridad-es-la-misma-que-en-la-aplicacion):

- Con el rol **Comercial Restringido**, solo las cuentas de tu cartera y lo que cuelga de ellas. Si preguntas por una cuenta de otra cartera, el asistente no la encuentra o te dice que no tienes permiso.
- Con los roles **Comercial Restringido** y **Users**, solo tus gastos, y solo puede modificar tus actuaciones.
- Si le pides algo que tu usuario no puede hacer (por ejemplo, rechazar una oferta de otra cartera), te dice que no tienes permiso y no cambia nada.

## Revisar y cortar la conexión

- **Tus asistentes:** menú de perfil › **Asistentes conectados**. Con **Revocar** se corta la conexión al momento; para volver a usarlo, conéctalo de nuevo.
- **El administrador**, en el panel de control, puede ver el **Uso del MCP** (llamadas por día, por herramienta y por persona, y las rechazadas) y las **Sesiones MCP** abiertas.
- Si se apaga **Habilitar MCP**, ningún asistente puede conectarse, desde ese momento.

## CRM sin AHORA ERP (CRM Lite)

Funciona igual, salvo lo que depende del ERP: no hay facturas, ni cobros pendientes, ni resúmenes de ventas. La tarea «Cobros pendientes de una cuenta» no tendrá datos que mostrar.

## Si algo no sale

| Lo que ves | Por qué | Qué hacer |
|---|---|---|
| El asistente no conecta y la dirección da error 404 | **Habilitar MCP** o **Enable WebAPI** están apagados | Pide al administrador que los encienda |
| **Conectar un asistente** o la página de consentimiento dicen que no tienes permiso | Tu rol o tu usuario no tiene la columna del robot | Pide al administrador el permiso |
| Claude web o ChatGPT no llegan a la aplicación | La aplicación no es accesible desde internet con HTTPS | Consúltalo con quien administra el servidor |
| El asistente se niega a crear o modificar | Desmarcaste **Modificar datos** al conectar, o tu usuario no puede hacerlo en la aplicación | Revoca la conexión y vuelve a conectar marcando **Modificar datos** |

Para todo el detalle (ajustes, límites de llamadas, auditoría), consulta la ayuda de Flexygo, apartado *Ayuda › Asistentes de IA (MCP)*.
