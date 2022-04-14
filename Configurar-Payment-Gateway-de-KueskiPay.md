Los siguientes pasos a seguir son para configurar y personalizar el método de pago de _KueskiPay_ en VTEX, creando una afiliación entre su comercio y _KueskiPay_.<br>
En esta sección también se definen las condiciones del método de pago con el que se van a realizar las compras.  

### Antes de iniciar
Para iniciar la configuración del Payment Gateway de _KueskiPay_ es necesario tener lo siguiente:
* La llave **Access Key** guardada en la sección **Generar Credenciales VTEX** en el paso 11. 
* El _secret_ guardado en la sección **Generar Credenciales VTEX** en el paso 6.
* La llave **KueskiPay Producción API Key** provista por el equipo de Kueski antes de la instalación.

![Screen Shot 2022-04-14 at 11 26 58](https://user-images.githubusercontent.com/101224062/163441808-e0954b0c-0d42-4283-a222-8e23c7ebc75f.png)

## Habilitar la afiliación de KueskiPay
En esta sección es necesario otorgar los permisos para habilitar y configurar la afiliación de KueskiPay en su comercio mediante las llaves proporcionadas por Kueski.

1. En el menú del lado izquierdo, seguir el siguiente flujo: **TRANSACTIONS** -> **Payments** -> **Settings**.
2. Dar click a la pestaña **Gateway Affilliations**.
3. Dar click al botón **Agregar** (
![Screen Shot 2022-04-14 at 12 30 05](https://user-images.githubusercontent.com/101224062/163454180-7ab24802-1a80-4ab0-a8b5-33eaf2b8257e.png)
) para agregar una afiliación. <br>
Se abrirá la siguiente página. 
4. En la sección **OTHERS**, dar click al conector **KueskiPay** ( 
![Screen Shot 2022-04-14 at 12 31 22](https://user-images.githubusercontent.com/101224062/163454340-3329d4d3-f063-492c-9b52-897c3725b1ac.png)
).<br> 
Se abrirá un formulario para configurar la afiliación de KueskiPay. 
5. Llenar los campos con la siguiente información:
   * **Affiliation name:** `KueskiPay - New configuration`.
   * **Application Key:** `prod_{{Access Key}}_{{Kueskipay Producción API Key}}` <br>
   Ejemplo: `prod_vtexappkey-kueski-HHWTPJ_2b7642b-3j9c-12c4-3c68`
   * **Application Token:** _secret_.
6. Dar click al botón **Save**.
La afiliación ya está dada de alta. 

## Configurar pago personalizado KueskiPay
En esta sección se personaliza el método de pago _KueskiPay_, esta configuración es definida por Kueski y se tienen que seguir los siguientes pasos:
1. En el menú del lado izquierdo, seguir el siguiente flujo: **TRANSACTIONS** -> **Payments** -> **Settings**.
2. Dar click a la pestaña **Custom payments**.
3. En la sección **Notes Payables** dar click al primer cuadro que diga **Config**. Se abrirá un formulario para configurar el _custom payment_.
4. Llenar los campos de _custom payment_ con la siguiente información:
   * **Name:** `KUESKI`
   * **Description:** `Método de pago con KueskiPay`
   * **Notes payables expiration date:** `3`
   * **Automatic authorization:** `No`
   * **Change margin range:** `0`
   * **Split payment:** `No`
   * **Automatic invoicing:** `15`

![Screen Shot 2022-04-14 at 13 11 13](https://user-images.githubusercontent.com/101224062/163460041-f81ce54e-9068-4440-9e16-ecc36a607a81.png)

5. Dar click al botón **Save**. <br>
Se abrirá la página de Payment conditions.
6. Llenar los campos de **Payment conditions** de la siguiente manera:
   * **Rule name:** `KueskiPay`
   * **Status:** Active (
![Screen Shot 2022-04-14 at 13 12 44](https://user-images.githubusercontent.com/101224062/163460238-2a48fa1f-6df3-4b04-925c-938ab2d21d7c.png)
)
   * **Process with affiliation:** `KueskiPay - New configuration`
7. Dar click al botón **Save**. <br>
Saldrá el método de pago _KUESKI_ en **Payment Conditions**.
8. Guardar el _ID_ de **Payment Conditions**, ya que será requerido más adelante.

![Screen Shot 2022-04-14 at 13 15 20](https://user-images.githubusercontent.com/101224062/163460597-3221ee21-7c02-4637-8033-73b3e595c240.png)
 
