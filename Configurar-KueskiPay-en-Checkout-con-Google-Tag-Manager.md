Los siguientes pasos a seguir son para configurar Google Tag Manager en el checkout.

## Antes de iniciar
Para iniciar la configuración de Google Tag Manager es necesario tener lo siguiente:
* Tener una cuenta de Google con acceso a _Google Tag Manager_.

## Configurar Google Tag Manager
1. Entrar a su cuenta de [Google Tag Manager](http://www.google.com/tagmanager/)
2. Dar click al botón de configuración (<img width="60" alt="Screen Shot 2022-04-14 at 14 10 00" src="https://user-images.githubusercontent.com/101224062/163467902-f72154a7-af78-4f9e-9244-7d00804a8eac.png">
). <br>
Aparecerá un menú.
3. Dar click a la pestaña **Espacio de trabajo**.
<img width="185" alt="Screen Shot 2022-04-14 at 14 11 29" src="https://user-images.githubusercontent.com/101224062/163468071-e1db863a-b474-4b1c-98e1-856296c9baa4.png">

4. Dar click al botón **Añadir nueva etiqueta**.<br>
Se desplegará una página para configurar la etiqueta. 
![Captura de Pantalla 2022-04-05 a la(s) 11 17 06](https://user-images.githubusercontent.com/101224062/163468120-cfcd9f96-2066-47d0-82ec-a3cbc3a6694c.png)

5. En el campo **Etiqueta sin título** escribir `KueskiPay`.
6. Dar click al botón editar (
![Screen Shot 2022-04-14 at 13 23 14](https://user-images.githubusercontent.com/101224062/163461638-99a70468-5b3d-40cd-8221-0fae3a23a512.png)
) del cuadro **Configuración de la etiqueta**, el cual será visible al pasar el cursor sobre él.
7. En la sección **Personalizado**, dar click a **HTML personalizado**. <br>
Se abrirá un modal para agregar el HTML. 
![Captura de Pantalla 2022-04-05 a la(s) 11 34 05](https://user-images.githubusercontent.com/101224062/163468158-daf5b4ed-0692-463d-95ce-62f2989fb0b3.png)

8. Pegar el siguiente código HTML en el campo **HTML**.
Este código realiza el llamado a _KueskiPay_. 
```html
<script type="text/javascript" id='kpay-advertising-script' src="https://cdn.kueskipay.com/widgets.js?authorization=API-KEY&sandbox=true&integration=vtex"></script>
<script type="text/javascript">
  new KueskipayAdvertising({
    paymentConditionsId: 201,
  }).init();
</script>
```
![Screen Shot 2022-04-14 at 13 26 43](https://user-images.githubusercontent.com/101224062/163462134-26a0c336-1765-4d05-957b-ce2d87a965c4.png)

9. Dar click al botón editar (
![Screen Shot 2022-04-14 at 13 27 30](https://user-images.githubusercontent.com/101224062/163462250-89478f3c-9e5e-4437-b795-f45454f4fc6e.png)
), el cual será visible al pasar el cursor sobre el cuadro de **Activación**.
![Captura de Pantalla 2022-04-05 a la(s) 11 31 19](https://user-images.githubusercontent.com/101224062/163468253-05a60722-b453-40bf-9319-643ce0e7370c.png)

10. Dar click al botón **+** (
![Screen Shot 2022-04-14 at 13 27 58](https://user-images.githubusercontent.com/101224062/163462317-4e18caba-34ec-432c-a14b-ae5696c0001e.png)
).
11. En el campo **Activador sin título** escribir `Activador KueskiPay`.
12. Dar click al botón editar (![Screen Shot 2022-04-14 at 13 27 30](https://user-images.githubusercontent.com/101224062/163462250-89478f3c-9e5e-4437-b795-f45454f4fc6e.png) ), el cual será visible al pasar el cursor sobre el cuadro de Configuración del activador.
13. En la sección **Otros** dar click a **Evento personalizado**.
Se desplegará una página para configurar el activador.
![Captura de Pantalla 2022-04-05 a la(s) 11 35 07](https://user-images.githubusercontent.com/101224062/163468286-cf288c72-57ce-46cd-8b7c-362ff4ae73ec.png)

14. Configurar un activador con referencia a la etiqueta de código _HTML_ previamente creada en el paso 7, de la siguiente manera:

    * **Tipo de activador:** `Evento personalizado` <br> ![Screen Shot 2022-04-14 at 13 33 42](https://user-images.githubusercontent.com/101224062/163463068-7c7834af-a54b-4afa-9e63-fd75b0935209.png)
    * **Nombre del evento:** `.*` <br> ![Screen Shot 2022-04-14 at 13 33 58](https://user-images.githubusercontent.com/101224062/163463107-0e751384-2daf-45f7-bfa5-2f0d69ef5492.png)
    * **Este activador se activa en:** `Algunos eventos personalizados` <br> ![Screen Shot 2022-04-14 at 13 34 09](https://user-images.githubusercontent.com/101224062/163463127-3ec4ec0d-618c-427e-ad7a-8dd2782da14f.png)
    * **Ejecute este activador cuando tenga lugar un evento y se cumplan todas las condiciones:** <br> ![Screen Shot 2022-04-14 at 13 33 23](https://user-images.githubusercontent.com/101224062/163463021-27ab3012-65b2-444d-8a0b-0210cb4ba7a9.png)

15. Dar click al botón **Guardar**. <br>
El activador está configurado. 
![Captura de Pantalla 2022-04-05 a la(s) 11 22 31](https://user-images.githubusercontent.com/101224062/163463270-4e256f23-24ff-4d69-9484-7ec54de357e0.png)



16. Dar click al botón **Guardar**. <br>
El activador ya quedó referenciado al HTML recién creado. 
![Captura de Pantalla 2022-04-05 a la(s) 11 27 59](https://user-images.githubusercontent.com/101224062/163467550-fa24c0bf-9827-4c1c-9bfb-9fc0e7db4e5c.png)
17. Dar click al botón **Enviar** para publicar los cambios del _Espacio de trabajo de Google Tag Manager_ para que se visualice la forma de pago dentro del checkout de _VTEX_.

![Captura de Pantalla 2022-04-05 a la(s) 11 36 13](https://user-images.githubusercontent.com/101224062/163467691-62f61058-8cad-4c37-a6a0-990ac7150dac.png)
 