## Antes de iniciar

### Instalación y configuración de módulo de KueskiPay
Los siguientes pasos a seguir son necesarios para instalar el módulo de _KueskiPay_ en tu plataforma de PrestaShop y poder hacer uso de su método de pago. 

1. Descargar el módulo de KueskiPay en la [página de PrestaShop](https://addons.prestashop.com/es/pago-tarjeta-carteras-digitales/51986-kueski-pay-compra-a-plazos-y-sin-tarjeta.html). 

2. Dar click al botón **Descargar**.

3. Iniciar sesión en PrestaShop Marketplace. 

4. En el menú del lado izquierdo, seguir el siguiente flujo: **MEJORAS** -> **Módulos** -> **Módulos y Servicios**. 

5. Dar click al botón **Subir un módulo**. <br>
Se abrirá un modal para subir el módulo. 

6. Seleccionar el archivo **v1.0.7-kueski.zip** <br>
La instalación iniciará automáticamente. 

7. Dar click al botón **Configurar**.

8. Llenar los campos con la siguiente información:
   * **API KEY:** {{API KEY}} <br>
   * **API SECRET:** {{API SECRET}} <br>
   * **Mostrar widget en la ficha del producto:** Sí <br>
   * **Mostrar widget en resumen de compra:** Sí <br>
   * **Activar Sandbox:** No <br>
   * **Estado de una Orden Aceptada:** Pago aceptado <br>
   * **Estado de una Orden con Error o Pago Inválido:** Error en pago <br>
   * **Ventana Modal (El cliente no saldrá de tu página):** No <br>

> :page_facing_up: **NOTA:**  
> Esta configuración te abre otra ventana en forma de modal, por lo tanto, si tu navegador está configurado para no permitirlos, no se verá el método de pago de KueskiPay.

   * **Activar Log:** Sí

9. Dar click al botón **Guardar cambios**.

10. Mandar el URL del campo **Notificaciones** al personal de Kueski que proporcionó la guía de instalación. 

**El método de pago y widget de KueskiPay se encuentran instalados.**