# Instalar método de pago KueskiPay
Los siguientes pasos a seguir son necesarios para instalar el método de pago KueskiPay en la plataforma _Shopify_

1. En la parte inferior izquierda, dar click a **configuración**.
2. En el menú de la izquierda, dar click a **Pagos**.
3. En la sección **Formas de pago admitidas**, dar click al botón **Agregar formas de pago**.
4. En el campo **Buscar por formas de pago** escribir `Kueski`. <br>
Te saldrá la opción de Kueski Pay.
5. Dar click a Kueski Pay.
<img width="692" alt="Screen Shot 2022-04-28 at 14 54 13" src="https://user-images.githubusercontent.com/101224062/167010043-460876c3-7333-4e39-b07e-ab9dd91ea395.png">

> **Imagen 1. Método de pago Kueski Pay**

6. Dar click al botón **Activar**.
<img width="674" alt="Screen Shot 2022-04-28 at 17 14 15" src="https://user-images.githubusercontent.com/101224062/167010449-b2450c33-2234-469d-8f61-44c95b590a8d.png">

> **Imagen 2. Botón para activar el método de pago Kueski Pay**

7. Dar click al botón **Conectar**.
<img width="670" alt="Screen Shot 2022-05-02 at 17 22 38" src="https://user-images.githubusercontent.com/101224062/167010602-5cbd4c32-8b0e-49a3-8b1e-8374c7ebd704.png">

> **Imagen 3. Botón para conectar con Kueski Pay**

8. Cerrar la página del formulario.
9. Notificar a Kueski mediante un correo, que el formulario ya se completó. 
10. Esperar el correo por parte de Kueski notificando que el comercio se encuentra activo en la plataforma de Kueski.
> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> Es necesario que Kueski active el comercio en su plataforma antes de seguir con la guía, para que se active el botón del siguiente paso. 

11. Dar click al botón **Activar Kueski Pay: Compra sin tarjeta**. <br>
Saldrá un mensaje con el texto _Kueski Pay: Compra sin tarjeta activado_.
![Captura de Pantalla 2022-04-19 a la(s) 16 06 14 (1)](https://user-images.githubusercontent.com/101224062/167011659-a1f04479-6e24-4819-8d95-95e88461937d.png)

> **Imagen 4. Botón para activar Kueski Pay**

**El método de pago KueskiPay ha quedado instalado y activo en la plataforma Shopify.**

# Instalar Widget de KueskiPay
Los siguientes pasos a seguir son necesarios para instalar el widget _KueskiPay_ en la plataforma de Shopify, para que sea visible desde la página de producto y carrito de compras.

## Antes de iniciar
Los requisitos para instalar el método de pago KueskiPay son los siguientes:

- La llave _API KEY_ provista por el equipo de Kueski antes de la integración. 

> :bulb: **TIP:**  
> Tener a la mano la llave _API KEY_ proporcionada por el equipo de Kueski, ya que serán necesarias durante la integración. 

## Instalación de widget en página de producto
Para instalar el widget de KueskiPay y sea visible en la página de producto es necesario seguir los siguientes pasos: 

1. Dar click al botón cerrar (X) para cerrar la página de configuración. <br>
Se abrirá la página de inicio. 
2. En el menú del lado izquierdo, seguir el siguiente flujo **Canales de venta** -> **Tienda online** -> **Temas**.
3. Dar click al botón **Acciones**. <br>
Se desplegará un menú.
<img width="1783" alt="Screen Shot 2022-04-28 at 17 41 05" src="https://user-images.githubusercontent.com/101224062/167026436-3b821ce9-e1be-4468-86b5-91a5d5bebb99.png">

> **Imagen 5. Menú del botón Acciones

4. Dar click a **Editar código**.
5. En la columna de archivos, dar click a la carpeta **Snippets**.
6. Dar click a **Agregar un nuevo snippet**. <br>
Se abrirá un modal con el titulo **Agregar un nuevo fragmento de código**. 
<img width="624" alt="Screen Shot 2022-04-27 at 14 21 33" src="https://user-images.githubusercontent.com/101224062/167026629-52b4c681-1063-4c31-818d-3ef7cc1e5fe1.png">

> **Imagen 6. Modal para asignar nombre al snippet

7. En el campo **Crea un nuevo fragmento de código llamado** escribir `kp-product-page-snippet`.
8. Dar click al botón **Crear fragmento de código**. <br>
Se creará un archivo .liquid en blanco.
9. Pegar el siguiente código:
```ruby
<!-- Trigger/Open The Modal -->
<kueskipay-widget
     data-kpay-widget-type="product"
     data-kpay-widget-font-size="15"
     data-kpay-widget-text-align="left"
     data-kpay-widget-amount="{{ product.price }}"
     data-kpay-widget-product-name="{{ product.title }}">
</kueskipay-widget>
<script id="kpay-advertising-script"
src="https://cdn.kueskipay.com/widgets.js?authorization={{API-KEY}}&sandbox=false&integration=shopify&version=v1.0">
</script>
<script type="">new KueskipayAdvertising().init()</script>
```

> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> Reemplazar el texto **API-KEY** por la llave _Public API Key_ proporcionada por el equipo de Kueski.
 
<img width="1270" alt="Screen Shot 2022-05-05 at 15 27 07" src="https://user-images.githubusercontent.com/101224062/167028459-2547d8e7-f32d-463f-b284-3ccb3f181495.png">

> **Imagen 6. Ejemplo de snippet con API-KEY en archivo kp-product-page-snippet.liquid**

10. Dar click al botón **Guardar**. <br>
Saldrá un mensaje con el texto _Asset saved_.
11. En la columna de archivos dar click a la carpeta **Sections**. 
12. Abrir el archivo **main-product.liquid**.

> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> En caso de no encontrar tal archivo, tratar con los siguientes: **main-product-footer.liquid** o **product-template.liquid**.<br>
En caso de no existir ninguno de los archivos antes mencionados, contactar directamente a Kueski. 

12. Identificar en el código el siguiente fragmento:<br>
`{%- if shop.taxes_included or shop.shipping_policy.body != blank -%} `

<img width="1257" alt="Screen Shot 2022-05-04 at 16 36 33" src="https://user-images.githubusercontent.com/101224062/167029384-a69e9217-5395-41d4-9689-61a6cee017c3.png">

> **Imagen 7. Herramienta para identificar fragmento de código

> :bulb: **TIP:**  
> Usar buscador para localizar el fragmento de código:<br>
Mac: **cmd** + **f**
Windows: **ctrl** + **f**

13. Posicionar el cursor al inicio del código del paso anterior. 
<img width="1267" alt="Screen Shot 2022-05-04 at 16 38 39" src="https://user-images.githubusercontent.com/101224062/167029728-93e18ccc-b0af-4aa0-b355-806eb9bf2de3.png">

> **Imagen 8. Cursor al inicio de la línea de código**

14. Dar enter. <br>
Quedará una línea en blanco.
<img width="1264" alt="Screen Shot 2022-05-04 at 16 40 45" src="https://user-images.githubusercontent.com/101224062/167029818-8412d1d4-9ae3-4143-b0d3-870ab3ff6864.png">

> **Imagen 9. Línea en blanco antes del fragmento de código**

15. En la línea en blanco, copiar el siguiente fragmento de código: <br>
`{% include 'kp-product-page-snippet' %}`
<img width="1264" alt="Screen Shot 2022-05-04 at 16 42 31" src="https://user-images.githubusercontent.com/101224062/167200952-c574a122-6304-4f73-a429-c4fb5cf8f0c8.png">

> **Imagen 10. Fragmento de código posicionado**

> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> Si al terminar la instalación, se muestra el siguiente error: **Include usage not allowed in this context** será necesario cambiar el fragmento del paso **15** por el siguiente: `{% render 'kp-product-page-snippet' %}`

16. Dar click al botón **Guardar**.

**El widget está instalado y ya es visible en la página de producto.**

## Instalación de widget en página de producto
Para instalar el widget de KueskiPay y sea visible en la página de carrito de compras es necesario seguir los siguientes pasos: 

1. En la columna de archivos, dar click a la carpeta de **Snippets**.
2. Dar click a **Agregar un nuevo snippet**. <br>
Se abrirá un modal con el título **Agregar un nuevo fragmento de código**.
<img width="624" alt="Screen Shot 2022-04-27 at 14 21 33" src="https://user-images.githubusercontent.com/101224062/167201976-a7840e06-9b23-4178-92c5-42aebb29b0eb.png">

> **Imagen 11. Modal para agregar nombre al snippet**

3. En el campo **Crea un nuevo fragmento de código llamado** escribir `kp-cart-page-snippet`
4. Dar click al botón **Crear fragmento de código**. <br>
Se creará un archivo _.liquid_ en blanco.
5. Pegar el siguiente código:

```ruby
<!-- Trigger/Open The Modal -->
<kueskipay-widget
     data-kpay-widget-type="cart"
     data-kpay-widget-font-size="15"
     data-kpay-widget-text-align="right"
     data-kpay-widget-amount="{{ cart.total_price }}">
</kueskipay-widget>
<script id="kpay-advertising-script" 
src="https://cdn.kueskipay.com/widgets.js?authorization={{APIKEY}}&sandbox=false&integration=shopify&version=v1.0">
</script>
<script type="">new KueskipayAdvertising().init()</script>
```

> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> Reemplazar el texto **API-KEY** por la llave _Public API Key_ proporcionada por el equipo de Kueski.
 
<img width="1785" alt="Screen Shot 2022-05-04 at 16 47 53" src="https://user-images.githubusercontent.com/101224062/167202461-de4d9da7-d533-4152-9af4-955e34431e41.png">

> **Imagen 12. Ejemplo de snippet con API-KEY en archivo kp-cart-page-snippet.liquid**

6. Dar click al botón **Guardar**. <br>
Saldrá un mensaje de texto diciendo _Asset saved_.
7. En la carpeta **Sections** buscar el archivo **main-cart-footer.liquid**
8. Identificar en el código el siguiente fragmento: `<small class="tax-note caption-large rte">`

<img width="1267" alt="Screen Shot 2022-05-04 at 16 52 10" src="https://user-images.githubusercontent.com/101224062/167202881-53025d2c-8bf1-448a-adbc-2e92ac24943d.png">

> **Imagen 13. Herramienta para identificar fragmento de código**

> :bulb: **TIP:**  
> Usar buscador para localizar el fragmento de código:<br>
Mac: **cmd** + **f**
Windows: **ctrl** + **f**

9. Posicionar el cursor al inicio del código del paso anterior.
<img width="1261" alt="Screen Shot 2022-05-04 at 16 54 12" src="https://user-images.githubusercontent.com/101224062/167203050-020c9dfd-aa20-4dc3-a3d4-f950c8ea2e57.png">

> **Imagen 14. Cursor al inicio de la línea de código**

10. Dar enter. <br>
Quedará una línea en blanco.
<img width="1263" alt="Screen Shot 2022-05-04 at 16 56 04" src="https://user-images.githubusercontent.com/101224062/167203138-470fd586-04f9-41bf-b95b-80d95d3fbcf8.png">

> **Imagen 15. Línea en blanco antes del fragmento de código**

11. En la línea en blanco, copiar el siguiente fragmento de código: `{% include 'kp-cart-page-snippet' %}`
<img width="1259" alt="Screen Shot 2022-05-04 at 16 58 03" src="https://user-images.githubusercontent.com/101224062/167203302-0d4c39f8-b0e8-4eed-9982-6d8ffdf46bb2.png">

> **Imagen 16. Fragmento de código posicionado**

> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> Si al terminar la instalación, se muestra el siguiente error: **Include usage not allowed in this context** será necesario cambiar el fragmento del paso **15** por el siguiente: `{% render 'kp-cart-page-snippet' %}`

12. Dar click al botón **Guardar**.

**El widget está instalado y ya es visible en la página de carrito de compras.**
