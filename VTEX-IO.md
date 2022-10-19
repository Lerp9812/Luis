# Generar credenciales VTEX IO
Los siguientes pasos a seguir son necesarios para generar las credenciales que serán asignadas a los roles y usuarios creados para el método de pago _Kueski Pay_.

## Antes de iniciar
Los requisitos para instalar el método de pago Kueski Pay son los siguientes:
* Versión de VTEX **IO**.
* La llave **Kueski Pay Producción API Key** provista por el equipo de Kueski antes de la integración.

> :bulb: **TIP:**  
> Ten a la mano la llave **Kueski Pay Producción API Key** proporcionada por el equipo de Kueski, ya que será solicitada durante la integración.

## Generar Access Key y Secret
En los siguientes pasos se generan y activan las llaves **Access Key** y **Secret**, que serán necesarias para la creación de roles y usuarios de _Kueski Pay_. 
1. Accede a tu cuenta de VTEX con permisos de _Admin_.
2. En el menú del lado izquierdo, sigue el siguiente flujo **ACCOUNT SETTINGS** -> **Account management** -> **Account**.
3. En la sección **Security** haz clic en el botón **Generate access key and secret.** <br>
Se abrirá un modal con título **New access key and secret**
![Screen Shot 2022-05-04 at 15 56 14](https://user-images.githubusercontent.com/101224062/166832288-d6bd46a7-9ee1-4cf1-ab14-2536ecff98f9.png)

4. En el campo **Choose a name for the new access key and secret pair** escribe `KueskiPay-secret`.
5. Haz clic en el botón **Generate new secret**.
6. Guarda el _secret_ que se acaba de generar en un lugar seguro, ya que será usado más adelante.
![Screen Shot 2022-05-04 at 15 58 03](https://user-images.githubusercontent.com/101224062/166832471-93ee4fbb-01bd-429a-8bf3-b87aab504199.png)

> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> No se podrá acceder al _secret_ una vez cerrada la ventana. En caso de no haberlo guardado, será necesario repetir la sección **Generar las Credenciales VTEX**.

7. Haz clic en el botón **Close**.
8. En la sección **Security** verifica que la llave de **Kueskipay-secret** tenga su **Token Status** como _Active_.
9. Copia y Guarda la llave **Access Key** en un lugar seguro, ya que será usado más adelante. 
![Screen Shot 2022-05-14 at 16 01 48](https://user-images.githubusercontent.com/101224062/166832919-f1e7f0b8-f955-4a47-966d-71b18a145936.png)

## Creación de roles
Los siguientes pasos a seguir son para crear los roles de _Kueski Pay_ y otorgarles los permisos necesarios para el buen funcionamiento del método de pago.

1. En el menú del lado izquierdo, sigue el siguiente flujo **ACCOUNT SETTINGS** -> **Account management** -> **Roles**.
2. Haz clic en el botón **New Role**. <br>
Se abrirá una página para crear el nuevo rol. 
3. En el campo **Choose role** elige la opción **Custom**.
4. En el campo **Role name** escribe `KueskiPay`.
5. En la sección **Products and Resources** activa los siguientes permisos:

![Screen Shot 2022-04-13 at 17 59 56](https://user-images.githubusercontent.com/101224062/163288671-47c93d24-fb72-4411-9225-567fc766370f.png)

> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> Marca solo las casillas mostradas en la **Tabla 1**, ya que de haber una configuración diferente, puede causar errores en el funcionamiento de Kueski Pay.

6. haz clic en el botón **Save**.<br>
Los permisos están configurados. 

## Asignación de permisos a Application Keys
Los siguientes pasos a seguir son para asignarle permisos del rol _Kueski Pay_ a los Application Keys.

1. En el menú del lado izquierdo, sigue el siguiente flujo: **Account Settings** -> **Account management** -> **Application keys**.
2. Haz clic en el botón **+ ADD** 
![Screen Shot 2022-04-13 at 18 04 08](https://user-images.githubusercontent.com/101224062/163289027-98c15ccc-6d4d-4ce8-8695-47304d45f687.png)

3. En el campo **Key** escribe el _Access key_ guardada en la sección **Generar credenciales VTEX IO** en el paso 11.
![Screen Shot 2022-05-04 at 16 03 58](https://user-images.githubusercontent.com/101224062/166833193-212123d6-5517-4a7e-9665-edc8ed43ff51.png)

4. Haz clic en el botón **+ ADD Roles** 
![Screen Shot 2022-04-14 at 11 20 44](https://user-images.githubusercontent.com/101224062/163440842-97871f0d-8bd3-496a-8fcb-f31a420767da.png)
.
5. Selecciona el rol de **Kueski Pay**.
6. Haz clic en el botón **ADD ROLES** 
![Screen Shot 2022-04-14 at 11 21 40](https://user-images.githubusercontent.com/101224062/163441008-70c62b8b-2dea-41ad-883d-9d5415192f1d.png)
. <br>
El rol _Kueski Pay_ debe de verse en la tabla **Add roles**.
7. Haz clic en el botón **SAVE**. <br>
La llave _Access Key_ debe de estar Activa. 

![Screen Shot 2022-04-14 at 11 22 48](https://user-images.githubusercontent.com/101224062/163441153-5842bbde-cfa7-4581-bd61-5a5349ef08a4.png)

# Configura Payment Gateway de Kueski Pay
Los siguientes pasos a seguir son para configurar y personalizar el método de pago de _Kueski Pay_ en VTEX, creando una afiliación entre su comercio y _Kueski Pay_.<br>
En esta sección también se definen las condiciones del método de pago con el que se van a realizar las compras.  

## Antes de iniciar
Para iniciar la configuración del Payment Gateway de _Kueski Pay_ es necesario tener lo siguiente:
* La llave **Access Key** guardada en la sección **Generar Credenciales VTEX** en el paso 11. 
* El _secret_ guardado en la sección **Generar Credenciales VTEX** en el paso 6.
* La llave **Kueski Pay Producción API Key** provista por el equipo de Kueski antes de la instalación.

> :bulb: **TIP:**  
> Ten a la mano la llave **Kueski Pay Producción API Key** proporcionada por el equipo de Kueski, ya que será solicitada durante la integración.

## Habilitar la afiliación de Kueski Pay
En esta sección es necesario otorgar los permisos para habilitar y configurar la afiliación de KueskiPay en su comercio mediante las llaves proporcionadas por Kueski.

1. En el menú del lado izquierdo, sigue el siguiente flujo: **TRANSACTIONS** -> **Payments** -> **Settings**.
2. Haz clic en la pestaña **Gateway Affilliations**.
![Screen Shot 2022-05-04 at 16 19 58](https://user-images.githubusercontent.com/101224062/166835024-24ec38e8-475a-416d-b7b1-0fb0ccc93d47.png)

3. Haz clic en el botón **Agregar** (
![Screen Shot 2022-04-14 at 12 30 05](https://user-images.githubusercontent.com/101224062/163454180-7ab24802-1a80-4ab0-a8b5-33eaf2b8257e.png)
) para agregar una afiliación. <br>
4. En la sección **OTHERS**, dar click al conector **Kueski Pay** ( 
![Screen Shot 2022-04-14 at 12 31 22](https://user-images.githubusercontent.com/101224062/163454340-3329d4d3-f063-492c-9b52-897c3725b1ac.png)
).<br> 
Se abrirá un formulario para configurar la afiliación de Kueski Pay. 
5. Llena los campos con la siguiente información:
   * **Affiliation name:** `Kueski Pay - New configuration`.
   * **Application Key:**
      * **Ambiente de producción:** `prod_{{Access Key}}_{{Kueski Pay Producción API Key}}` <br>
   Ejemplo: `prod_vtexappkey-kueski-HGWRPJ_3b7442b-3j2c-12c4-3f68`
      * **Ambiente de sandbox:** `sandbox_{{Access Key}}_{{Kueski Pay Sandbox API Key}}` <br>
   Ejemplo: `sandbox_vtexappkey-kueski-HGWRPJ_3b7442b-3j2c-12c4-3f68`
![Screen Shot 2022-05-04 at 16 15 21](https://user-images.githubusercontent.com/101224062/166834416-b2194562-c31a-4330-a678-3ca7aa5d4f15.png)

   * **Application Token:** _secret_.
![Screen Shot 2022-05-04 at 16 18 00](https://user-images.githubusercontent.com/101224062/166834699-102b3565-e408-4195-a16a-c952b21ee9d4.png)

6. Haz clic en el botón **Save**. <br>
La afiliación ya está dada de alta. 

## Configura pago personalizado Kueski Pay
En esta sección se personaliza el método de pago _Kueski Pay_, esta configuración es definida por Kueski y se tienen que seguir los siguientes pasos:
1. En el menú del lado izquierdo, sigue el siguiente flujo: **TRANSACTIONS** -> **Payments** -> **Settings**.
2. Haz clic en la pestaña **Custom payments**.
![Screen Shot 2022-05-04 at 16 19 03](https://user-images.githubusercontent.com/101224062/166834884-2242d99f-088a-4761-9628-f8f96030917e.png)

3. En la sección **Notes Payables** haz clic en el primer cuadro que diga **Config**. <br>
Se abrirá un formulario para configurar el _custom payment_.
![Screen Shot 2022-05-04 at 16 25 02](https://user-images.githubusercontent.com/101224062/166835447-898fd479-f16b-4640-ac33-aee9edce95be.png)

4. Llena los campos de _custom payment_ con la siguiente información:
   * **Name:** `KUESKI`
   * **Description:** `Método de pago con Kueski Pay`
   * **Notes payables expiration date:** `3`
   * **Automatic authorization:** `No`
   * **Change margin range:** `0`
   * **Split payment:** `No`
   * **Automatic invoicing:** `15`

> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> El campo **Name** debe de ser **KUESKI**, si se pone otro nombre se generará un error. <br>
> En caso de necesitar algún cambio en otro campo de la configuración, es necesario confirmar con el equipo de Kueski Pay y VTEX, ya que podrían verse afectados los procesos de Kueski Pay en su comercio. 

5. Haz clic en el botón **Save**. <br>
Se abrirá la página de Payment conditions.
6. Llena los campos de **Payment conditions** de la siguiente manera:
   * **Rule name:** `Kueski Pay`
![Screen Shot 2022-05-04 at 13 59 33](https://user-images.githubusercontent.com/101224062/166816294-5dfda646-9e22-42a6-a3f4-b34a27e1636c.png)

   * **Status:** Active 
![Screen Shot 2022-04-14 at 13 12 44](https://user-images.githubusercontent.com/101224062/163460238-2a48fa1f-6df3-4b04-925c-938ab2d21d7c.png)

   * **Process with affiliation:** `Kueski Pay - New configuration`
7. Haz clic en el botón **Save**. <br>
Saldrá el método de pago _KUESKI_ en **Payment Conditions**.

![Screen Shot 2022-04-04 at 15 47 12](https://user-images.githubusercontent.com/101224062/166831489-046b3420-d056-4c77-8570-4dd889a60dd5.png)

8. Guarda el _ID_ de **Payment Conditions**, ya que será requerido más adelante.

![Screen Shot 2022-04-04 at 15 35 21](https://user-images.githubusercontent.com/101224062/166831611-c2e9a808-6522-4905-9660-83186f3cfb69.png)

> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> La configuración hecha en _Payment conditions_ puede tardar hasta 10 minutos en verse reflejado en el checkout.

# Configura KueskiPay en el checkout con Google Tag Manager

Los siguientes pasos a seguir son para configurar Google Tag Manager en el checkout.

> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> Google Tag Manager solo esta disponible con las credenciales de **sandbox**, por esta razón es importante no cambiar a las llaves de producción.

## Antes de iniciar
Para iniciar la configuración de Google Tag Manager es necesario tener lo siguiente:
* Tener una cuenta de Google con acceso a _Google Tag Manager_.

## Configurar Google Tag Manager
1. Entra a tu cuenta de [Google Tag Manager](http://www.google.com/tagmanager/)
2. Haz clic en el botón de configuración (<img width="60" alt="Screen Shot 2022-04-14 at 14 10 00" src="https://user-images.githubusercontent.com/101224062/163467902-f72154a7-af78-4f9e-9244-7d00804a8eac.png">
). <br>
Aparecerá un menú.
3. Haz clic en la pestaña **Espacio de trabajo**.
<img width="185" alt="Screen Shot 2022-04-14 at 14 11 29" src="https://user-images.githubusercontent.com/101224062/163468071-e1db863a-b474-4b1c-98e1-856296c9baa4.png">

4. Haz clic en el botón **Añadir nueva etiqueta**.<br>
Se desplegará una página para configurar la etiqueta. 
![Captura de Pantalla 2022-04-05 a la(s) 11 17 06](https://user-images.githubusercontent.com/101224062/163468120-cfcd9f96-2066-47d0-82ec-a3cbc3a6694c.png) <br>
> Imagen 1. Botón para añadir etiquetas

5. En el campo **Etiqueta sin título** escribe `Kueski Pay`.
6. Haz clic en el botón editar (
![Screen Shot 2022-04-14 at 13 23 14](https://user-images.githubusercontent.com/101224062/163461638-99a70468-5b3d-40cd-8221-0fae3a23a512.png)
) del cuadro **Configuración de la etiqueta**, el cual será visible al pasar el cursor sobre él.
7. En la sección **Personalizado**, haz clic en **HTML personalizado**. <br>
Se abrirá un modal para agregar el HTML. 
![Captura de Pantalla 2022-04-05 a la(s) 11 34 05](https://user-images.githubusercontent.com/101224062/163468158-daf5b4ed-0692-463d-95ce-62f2989fb0b3.png)
> Imagen 2. Botón para personalizar el HTML

8. Pega el siguiente código HTML en el campo **HTML**.
Este código realiza el llamado a _Kueski Pay_. 
```html
<script type="text/javascript" id='kpay-advertising-script' src="https://cdn.kueskipay.com/widgets.js?authorization=API-KEY&sandbox=true&integration=vtex"></script>
<script type="text/javascript">
  new KueskipayAdvertising({
    paymentConditionsId: 201,
  }).init();
</script>
```
![Screen Shot 2022-04-14 at 13 26 43](https://user-images.githubusercontent.com/101224062/163462134-26a0c336-1765-4d05-957b-ce2d87a965c4.png)

9. Haz clic en el botón editar (
![Screen Shot 2022-04-14 at 13 27 30](https://user-images.githubusercontent.com/101224062/163462250-89478f3c-9e5e-4437-b795-f45454f4fc6e.png)
), el cual será visible al pasar el cursor sobre el cuadro de **Activación**.
![Captura de Pantalla 2022-04-05 a la(s) 11 31 19](https://user-images.githubusercontent.com/101224062/163468253-05a60722-b453-40bf-9319-643ce0e7370c.png)
> Imagen 3. Botón para editar activación

10. Haz clic en el botón **+** (
![Screen Shot 2022-04-14 at 13 27 58](https://user-images.githubusercontent.com/101224062/163462317-4e18caba-34ec-432c-a14b-ae5696c0001e.png)
).
11. En el campo **Activador sin título** escribe `Activador Kueski Pay`.
12. Haz clic en el botón editar (![Screen Shot 2022-04-14 at 13 27 30](https://user-images.githubusercontent.com/101224062/163462250-89478f3c-9e5e-4437-b795-f45454f4fc6e.png) ), el cual será visible al pasar el cursor sobre el cuadro de Configuración del activador.
13. En la sección **Otros** haz clic en **Evento personalizado**.
Se desplegará una página para configurar el activador.
![Captura de Pantalla 2022-04-05 a la(s) 11 35 07](https://user-images.githubusercontent.com/101224062/163468286-cf288c72-57ce-46cd-8b7c-362ff4ae73ec.png)
> Imagen 4. Botón para configurar un evento personalizado

14. Configura un activador con referencia a la etiqueta de código _HTML_ previamente creada en el paso 7, de la siguiente manera:

    * **Tipo de activador:** `Evento personalizado` <br> ![Screen Shot 2022-04-14 at 13 33 42](https://user-images.githubusercontent.com/101224062/163463068-7c7834af-a54b-4afa-9e63-fd75b0935209.png)
    * **Nombre del evento:** `.*` <br> ![Screen Shot 2022-04-14 at 13 33 58](https://user-images.githubusercontent.com/101224062/163463107-0e751384-2daf-45f7-bfa5-2f0d69ef5492.png)
    * **Este activador se activa en:** `Algunos eventos personalizados` <br> ![Screen Shot 2022-04-14 at 13 34 09](https://user-images.githubusercontent.com/101224062/163463127-3ec4ec0d-618c-427e-ad7a-8dd2782da14f.png)
    * **Ejecute este activador cuando tenga lugar un evento y se cumplan todas las condiciones:** <br> ![Screen Shot 2022-04-14 at 13 33 23](https://user-images.githubusercontent.com/101224062/163463021-27ab3012-65b2-444d-8a0b-0210cb4ba7a9.png)

15. Haz clic en el botón **Guardar**. <br>
El activador está configurado. 
![Captura de Pantalla 2022-04-05 a la(s) 11 22 31](https://user-images.githubusercontent.com/101224062/163463270-4e256f23-24ff-4d69-9484-7ec54de357e0.png)
> Imagen 5. Activador configurado


16. Haz clic en el botón **Guardar**. <br>
El activador quedó referenciado al HTML recién creado. 
![Captura de Pantalla 2022-04-05 a la(s) 11 27 59](https://user-images.githubusercontent.com/101224062/163467550-fa24c0bf-9827-4c1c-9bfb-9fc0e7db4e5c.png)
> Imagen 6. Activador referenciado a HTML personalizado

17. Haz clic en el botón **Enviar** para publicar los cambios del _Espacio de trabajo de Google Tag Manager_ para que se visualice la forma de pago dentro del checkout de _VTEX_.

![Captura de Pantalla 2022-04-05 a la(s) 11 36 13](https://user-images.githubusercontent.com/101224062/163467691-62f61058-8cad-4c37-a6a0-990ac7150dac.png)
> Imagen 7. Botón para desplegar configuraciones
 