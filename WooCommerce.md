# Instalar plugin de KueskiPay
Los siguientes pasos a seguir son necesarios para instalar el plugin de _KueskiPay_ en tu plataforma de WooCommerce y poder hacer uso de su método de pago. 

1. Ingresar a su cuenta de WooCommerce.
2. En el menú del lado izquierdo, seguir el siguiente flujo **Plugins** -> **Añadir nuevo**. <br>
3. Dar click al botón **Subir plugin**.

<img width="1791" alt="Screen Shot 2022-04-19 at 14 18 27" src="https://user-images.githubusercontent.com/101224062/164089427-f744c2fe-39f5-4bcf-8176-b0b5cc42a257.png">

> Imagen 1. Botón para subir plugin


4. Dar click al botón **Seleccionar archivo**. <br>
Se abrirá un modal para seleccionar el archivo.
<img width="1786" alt="Screen Shot 2022-04-19 at 14 27 20" src="https://user-images.githubusercontent.com/101224062/164090222-a4848a95-aca6-4372-8e47-13e48dd700aa.png">

> Imagen 2. Botón para seleccionar el archivo 

5. Seleccionar el archivo WooCommerce 1.0.6.zip

![Screen Shot 2022-04-19 at 14 30 06](https://user-images.githubusercontent.com/101224062/164090393-4f4d060c-6e8c-4b8a-88a9-d1868d369945.png)

6. Dar click al botón **Instalar ahora**.
<img width="1785" alt="Screen Shot 2022-04-19 at 14 30 52" src="https://user-images.githubusercontent.com/101224062/164090627-7a051c5c-ca43-4906-b8fe-590803a7b3a9.png">

> Imagen 3. Botón para instalar el plugin

7. Dar click al botón **Activar plugin**

<img width="1790" alt="Screen Shot 2022-04-19 at 14 37 09" src="https://user-images.githubusercontent.com/101224062/164091608-ff5db9d4-55fb-42c5-a17c-58cdc3b56cdf.png">

> Imagen 4. Botón para activar el plugin de KueskiPay

![Screen Shot 2022-04-19 at 14 35 07](https://user-images.githubusercontent.com/101224062/164091117-ebe60a8e-c0d1-4bcd-ab36-7d17e484a13e.png)

> ✔️ El plugin de _KueskiPay_ está instalado.

# Configurar plugin KueskiPay

1. Dar click al botón **Configuración** de la casilla **Kueski WooCommerce Plugin**.

<img width="1789" alt="Screen Shot 2022-04-19 at 14 40 40" src="https://user-images.githubusercontent.com/101224062/164091988-601a10b7-330b-426a-899d-3f0de3fb4d87.png">

> Imagen 5. Botón para configurar el plugin de KueskiPay

2. Mandar el _URL_ del campo **Manual de Configuración** al personal de Kueski que proporcionó la guía de instalación.

<img width="1788" alt="Screen Shot 2022-04-19 at 14 43 47" src="https://user-images.githubusercontent.com/101224062/164092487-b021511d-2050-4960-96a9-5d644651c6db.png">

> Imagen 6. URL único

![Screen Shot 2022-04-19 at 14 46 43](https://user-images.githubusercontent.com/101224062/164092802-8d5bb057-464e-4c27-941c-e3ba1972e22e.png)

3. Llenar los campos con la siguiente información:
    * **Activate:** `Active` <br> 
        * Esta casilla es necesario que este seleccionada. Activa el widget de KueskiPay.
        ![Screen Shot 2022-04-19 at 14 44 49](https://user-images.githubusercontent.com/101224062/164104360-bd3b950e-450d-463e-ae73-bb92388b0f3b.png)

    * **Kueski API Key:** `{{API KEY}}` <br> 
        * **Ejemplo:** `8a8b4ce1-a4d0-4205-912c-56b03afbb34f` <br> 
        ![Screen Shot 2022-04-19 at 14 44 53](https://user-images.githubusercontent.com/101224062/164103927-8da93f00-561e-4902-9047-c862250baa74.png)

    * **Kueski Secret Key:** `{{API SECRET}}` <br> 
        * **Ejemplo:** `01409e49-bbe1-4574-be6d-995112990959` <br> 
        ![Screen Shot 2022-04-19 at 14 45 08](https://user-images.githubusercontent.com/101224062/164094754-01d53d8c-c877-4ba5-a27f-3706f3de040c.png)

    * **Leave orders with payment Accepted in Completed:** <br> 
        * Esta casilla se recomienda dejarla vacía, ya que cambiará el estatus de la orden a **Completada** en cuanto se procese el pago, aun si el envío no se ha hecho. <br> ![Screen Shot 2022-04-19 at 14 45 15](https://user-images.githubusercontent.com/101224062/164104769-859c8070-06a6-4aeb-8001-358cc4448ede.png)

    * **Modal:** 
        * Esta casilla se recomienda dejarla vacía, ya que abre un modal al procesar el pago y en caso de tener bloqueadas las ventanas emergentes, causará un error.  <br> ![Screen Shot 2022-04-19 at 14 45 19](https://user-images.githubusercontent.com/101224062/164104865-92e83d58-4164-43da-baca-0af2dbb0a8f9.png)

    * **Show widget on product sheet:** `Active` <br> 
        * Esta casilla es necesario que este seleccionada. Muestra el widget de KueskiPay en la página del producto.
        ![Screen Shot 2022-04-19 at 14 45 23](https://user-images.githubusercontent.com/101224062/164104937-643fa0d8-cd47-4dc4-8dcc-18f919542d24.png)

    * **Show widget on cart summary:** `Active` <br> 
        * Esta casilla es necesario que este seleccionada. Muestra el widget de KueskiPay en el carrito de compras. 
        ![Screen Shot 2022-04-19 at 14 45 26](https://user-images.githubusercontent.com/101224062/164104989-a8f52915-fb9b-4225-930c-99e685cd4c11.png)

    * **Sandbox Mode:** 
        * Esta casilla es para activar el modo de prueba. Si se activa, los pagos no se verán procesados. <br> ![Screen Shot 2022-04-19 at 15 32 32](https://user-images.githubusercontent.com/101224062/164105428-b90291cd-699b-4327-a44f-f28a32bd9719.png)

    * **Debug Mode:** `Active` <br> 
        * Esta casilla es necesario que este seleccionada. Permite ver los logs en caso de haber un error.
        ![Screen Shot 2022-04-19 at 14 45 33](https://user-images.githubusercontent.com/101224062/164105111-df5c5b23-d663-4e81-903a-c6d138436a30.png)

4. Dar click al botón **Guardar los cambios**. <br>
El plugin de _KueskiPay_ ya está configurado y funciona en tu comercio. 
