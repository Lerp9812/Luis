# Errores de Conciliación

Un error de conciliación ocurre cuando Kueski hace un request y el merchant tiene problemas para regresar el response con el estatus requerido por Kueski. Esto ocasiona que el préstamo no se pueda llevar a cabo. <br>
Los known issues de conciliación fueron identificados en las siguientes plataformas:
- WooCommerce
- Prestashop
- Magento 
- Tienda Nube
- API

## WooCommerce
Los siguientes errores fueron identificados en la plataforma de WooCommerce. 

### Inconsistencia en el método de autenticación: 
Error que se genera por elegir el método de autenticación incorrecto. El método de autenticación depende de la versión del plugin de KueskiPay que se vaya a instalar en WooCommerce. 
Elegir mal el método de autenticación puede lanzar los siguientes errores:
`invalid api_secret provided` o `invalid JWT provided`<br>

**Solución:** Elegir el método de autenticación de acuerdo a la siguiente tabla:
| Auth method               | Plain                         | JWT                   |
| ------------------------- | ----------------------------- |-----------------------|
| Versión plugin Kueski Pay | 1.0.4 y anteriores            | 1.0.5 y 1.0.6         |
| Error message             | `invalid api_secret provided` | `invalid JWT provided`|


### Plugin de Firewall instalado: 
Error generado porque el comercio tiene instalado un plugin anti firewall. Los firewalls identificados hasta el momento son:
- Jet Pack
- Cloudflare

**Solución:** Pedirle al merchant que su proveedor agregue las siguientes IPs a la lista blanca:

| Sandbox        | Production   | 
| -------------- | ------------ |
| 34.228.88.107  | 54.83.122.50 <br> 34.201.31.235 <br> 34.205.87.241 <br> 54.145.36.91 <br> 54.162.85.69 | 


### Widget KueskiPay version 1.0.6 incompatible con servidor Apache:
Error que se genera cuando se intenta instalar el plugin versión 1.0.6 en una plataforma montada en un servidor Apache. El servidor Apache bloquea el envío de las llaves secretas a Kueski y no permite terminar el proceso de solicitud de préstamo. 

**Solución:** Bajar de versión del plugin instalado en la plataforma. Es necesario instalar el plugin versión 1.0.4 en lugar de la versión 1.0.6