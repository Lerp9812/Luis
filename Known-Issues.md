# Errores de Conciliación

Un error de conciliación ocurre cuando Kueski hace un request y el merchant tiene problemas para regresar el response con el estatus requerido por Kueski. Esto ocasiona que el préstamo no se pueda llevar a cabo y la compra no se efectúe. <br>
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
| Auth method   | Versión plugin Kueski Pay     | Error message                 |
| ------------- | ----------------------------- |------------------------------ |
| Plain         | 1.0.5 y anteriores            | `invalid api_secret provided` |
| JWT           | 1.0.6 y 1.0.7                 | `invalid JWT provided`        |

### Plugin de Firewall instalado: 
Error generado porque el comercio tiene instalado un plugin anti firewall. Los firewalls identificados hasta el momento son:
- Jet Pack
- Cloudflare

**Solución:** Pedirle al merchant que su proveedor agregue las siguientes IPs a la lista blanca:

| Sandbox        | Production   | 
| -------------- | ------------ |
| 34.228.88.107  | 107.22.173.170 <br> 34.227.141.157 <br> 54.162.241.13 <br> 34.239.83.96 <br> 44.206.91.122 <br> 3.229.238.39 | 


### KueskiPay widget version 1.0.6 incompatible con servidor Apache:
Error que se genera cuando se intenta instalar el plugin versión 1.0.6 en una plataforma montada en un servidor Apache. El servidor Apache bloquea el envío de las llaves secretas a Kueski y no permite terminar el proceso de solicitud de préstamo. 

**Solución:** Bajar de versión del plugin instalado en la plataforma. Es necesario instalar el plugin versión 1.0.4 en lugar de la versión 1.0.6

## PrestaShop
Los siguientes errores fueron identificados en la plataforma de PrestaShop.

### Inconsistencia en el método de autenticación: 
Error que se genera por elegir el método de autenticación incorrecto. El método de autenticación depende de la versión del plugin de KueskiPay que se vaya a instalar en PrestaShop. 
Elegir mal el método de autenticación puede lanzar los siguientes errores:
`invalid api_secret provided` o `invalid JWT provided`<br>

**Solución:** Elegir el método de autenticación de acuerdo a la siguiente tabla:
| Auth method   | Versión plugin Kueski Pay     | Error message                 |
| ------------- | ----------------------------- |------------------------------ |
| Plain         | 1.0.5 y anteriores            | `invalid api_secret provided` |
| JWT           | 1.0.6 y 1.0.7                 | `invalid JWT provided`        |

### Plugin de Firewall instalado: 
Error generado porque el comercio tiene instalado un plugin anti firewall. Los firewalls identificados hasta el momento son:
- Jet Pack
- Cloudflare

**Solución:** Pedirle al merchant que su proveedor agregue las siguientes IPs a la lista blanca:

| Sandbox        | Production   | 
| -------------- | ------------ |
| 34.228.88.107  | 107.22.173.170 <br> 34.227.141.157 <br> 54.162.241.13 <br> 34.239.83.96 <br> 44.206.91.122 <br> 3.229.238.39 | 

### KueskiPay widget version 1.0.6 incompatible con servidor Apache:
Error que se genera cuando se intenta instalar el plugin versión 1.0.6 en una plataforma montada en un servidor Apache. El servidor Apache bloquea el envío de las llaves secretas a Kueski y no permite terminar el proceso de solicitud de préstamo. 

**Solución:** Bajar de versión del plugin instalado en la plataforma. Es necesario instalar el plugin versión 1.0.4 en lugar de la versión 1.0.6

## Magento
Los siguientes errores fueron identificados en la plataforma de Magento.
### Plugin de Firewall instalado: 
Error generado porque el comercio tiene instalado un plugin anti firewall. Los firewalls identificados hasta el momento son:
- Jet Pack
- Cloudflare

**Solución:** Pedirle al merchant que su proveedor agregue las siguientes IPs a la lista blanca:

| Sandbox        | Production   | 
| -------------- | ------------ |
| 34.228.88.107  | 107.22.173.170 <br> 34.227.141.157 <br> 54.162.241.13 <br> 34.239.83.96 <br> 44.206.91.122 <br> 3.229.238.39 | 

## Tienda Nube
Los siguientes errores fueron identificados en la plataforma de Tienda Nube.

### Servidor de Conexa deja de funcionar:
Error generado porque el servidor de Conexa se cae constantemente y no puede completar la conciliación. 

**Solución:** No hay una por el momento. 
