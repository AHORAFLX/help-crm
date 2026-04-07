# Generar oferta a una delegación de cuenta

Las ofertas del CRM se generan a la misma vez en el sistema de gestión AHORA ERP.

De modo que una ofertas generada en el CRM será visible en AHORA ERP. Por lo tanto, para evitar errores de compatibilidad, deben seguir los mismos criterios de parametrización.

  

A la hora de generar una oferta a una delegación de cuenta, debe tener en cuenta que solamente le será permitida dicha acción, si el parámetroOFERTAS_CLI_SOLO_CLIENTES lo permite.

Dicho parámetro presente en AHORA ERP, si está activo, impide crear ofertas a plantas, situación análoga en el CRM, ya que de lo contrario, daría un error al abrir la misma oferta en el ERP.

  

_Para permitir generar una oferta a una delegación de cuenta, el parámetroOFERTAS_CLI_SOLO_CLIENTES debe estar con el valor OFF._

  

A partir de ese momento, será posible crear una oferta a una delegación de cuenta, como también desde el ERP, crear una oferta a una planta

  

Recuerde: Las delegaciones de cuentas son plantas en el ERP.