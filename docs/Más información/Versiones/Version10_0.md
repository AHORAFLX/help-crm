# Versión 10.0

La actualización renueva la interfaz de AHORA CRM y mejora la seguridad y el rendimiento.

## Novedades

### Interfaz

- **AHORA CRM se actualiza a Flexygo 10 y .NET 9, con una nueva interfaz y mejoras de seguridad y rendimiento.** La actualización incluye el actualizador de Flexygo 10. La nueva interfaz facilita la consulta de tarjetas y contadores del área de administración y mejora la visibilidad de los campos en la skin crm2024.

### Administración

- **Puedes desplegar AHORA CRM en Docker y usar el ERP de AHORA como base de datos externa.** Así, los datos del ERP se mantienen en una base de datos externa al CRM.

### API MCP

- **AHORA CRM incorpora una API MCP para facilitar la integración con aplicaciones que utilizan este protocolo.** Los desarrolladores pueden conectar sus aplicaciones con el CRM mediante MCP. Así, pueden integrar aplicaciones compatibles con este protocolo.

### Ayuda

- **Consulta la ayuda del CRM para resolver dudas sobre sus funciones con guías y recursos visuales.** Incluye guías sobre análisis, notificaciones, uso offline, calendario, gastos, contactos e integración con 3CX, entre otros temas. También incorpora imágenes en contenidos sobre 3CX, gastos, ofertas y uso online y offline.

### Informes

- **Dispones de informes para actividades de cobro, facturas, gastos, justificantes de cobro y ofertas.** El CRM incorpora plantillas de informe para consultar o imprimir estos documentos.

## Mejoras

### Calendario

- **Se ajusta el color de fondo del calendario.**

### Clientes

- **Al crear clientes sin conexión o mediante IA, puedes incluir también su web y su NIF.** En el alta sin conexión, añádelos durante el proceso; si utilizas IA, inclúyelos entre los datos del alta.

### Importación de clientes

- **Al importar clientes, se completan la población, la provincia y el país a partir del nombre de la población.** Así se rellenan los datos geográficos del cliente durante la importación. Basta con incluir el nombre de la población para que se completen esos campos.

### Ofertas

- **Las líneas de las ofertas incluyen la información de los descuentos de cabecera y de pronto pago.** La información aparece junto a los datos de cada línea. Así puedes tener en cuenta ambos descuentos al revisar una oferta.
- **Puedes consultar el seguimiento de firma de las ofertas desde la ficha, la lista y los presets.** La información está disponible en esos tres contextos. Así puedes revisar las ofertas desde el lugar que te resulte más cómodo.

### WhatsApp

- **El complemento de WhatsApp presenta estilos mejorados.** El cambio actualiza la apariencia del complemento en el CRM.

## Correcciones

### Artículos

- **El detalle de artículo ya no aparece cuando no tiene un registro relacionado.** Así, el módulo solo se muestra cuando hay información asociada que consultar.

### Gastos

- **El envío de gastos al ERP funciona aunque sus líneas tengan documentos adjuntos.** Los documentos adjuntos ya no impiden completar el envío de los gastos.

### Importación de clientes

- **La importación de clientes procesa correctamente el nombre del contacto y el número de empleados.** Estos datos se incluyen al cargar los clientes mediante la importación. Así, el nombre del contacto y el número de empleados quedan recogidos correctamente en los registros importados.

### Procesos personalizados

- **Las funciones personalizadas de los script jobs funcionan correctamente en Lite.** El cambio evita el problema al usar estas funciones en instalaciones Lite.
