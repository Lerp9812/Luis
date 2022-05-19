# Errores de Conciliación

Known issues de conciliación identificados en las siguientes plataformas:
- Shopify
- WooCommerce
- Prestashop
- VTEX
- API


### WooCommerce
Los siguientes errores fueron identificados en la plataforma de WooCommerce en las integraciones. 

**Inconsistencia en el método de autenticación:**  
Error que se genera por elegir el método de autenticación incorrecto. El método de autenticación depende de la versión del plugin de KueskiPay que se vaya a instalar en WooCommerce. 
Elegir mal el método de autenticación puede lanzar los siguientes errores:
`invalid api_secret provided` o `invalid JWT provided`<br>

**Solución:** Elegir el método de autenticación de acuerdo a la siguiente tabla:
| Auth method               | Plain                         | JWT                   |
| ------------------------- | ----------------------------- |-----------------------|
| Versión plugin Kueski Pay | 1.0.4 y anteriores            | 1.0.5 y 1.0.6         |
| Error message             | `invalid api_secret provided` | `invalid JWT provided`|


**Plugin de Firewall instalado:** <br>
Error generado porque el comercio tiene instalado un plugin anti firewall. Los firewalls identificados hasta el momento son:
- Jet Pack
- Cloudflare

**Solución:** Pedirle al merchant que su proveedor agregue las siguientes IPs a la lista blanca:
> **Sandbox** <br>
34.228.88.107 <br>
**Production** <br>
54.83.122.50 <br>
34.201.31.235 <br>
34.205.87.241 <br>
54.145.36.91 <br>
54.162.85.69 <br>


