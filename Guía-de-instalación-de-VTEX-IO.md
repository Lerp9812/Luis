# Antes de iniciar
Los requisitos para instalar el método de pago KueskiPay son los siguientes:
* Versión de VTEX **IO**.
* La llave **KueskiPay Producción API Key** provista por el equipo de Kueski antes de la integración.

> :bulb: **TIP:**  
> Tener a la mano la llave **KueskiPay Producción API Key** proporcionada por el equipo de Kueski, ya que será solicitada durante la integración.

# Generar credenciales VTEX IO
Los siguientes pasos a seguir son necesarios para generar las credenciales que serán asignadas a los roles y usuarios creados para el método de pago _KueskiPay_.

## Generar Access Key y Secret
En los siguientes pasos se generan y activan las llaves **Access Key** y **Secret**, que serán necesarias para la creación de roles y usuarios de _KueskiPay_. 
1. Acceder a tu cuenta de VTEX con permisos de _Admin_.
2. En el menú del lado izquierdo, seguir el siguiente flujo **ACCOUNT SETTINGS** -> **Account management** -> **Account**.
3. En la sección **Security** dar click al botón **Generate access key and secret.** <br>
Se abrirá un modal con título **New access key and secret**
4. En el campo **Choose a name for the new access key and secret pair** escribir `Kueskipay-secret`.
5. Dar click al botón **Generate new secret**.
6. Guardar el _secret_ que se acaba de generar en un lugar seguro, ya que será usado mas adelante.

> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> No se podrá acceder al _secret_ una vez cerrada la ventana. En caso de no haberlo guardado, será necesario repetir la sección **Generar las Credenciales VTEX**.

7. Dar click al botón **Close**.
8. En la sección **Security** verificar que la llave de **Kueskipay-secret** tenga su **Token Status** como _Active_.
9. Copiar y Guardar la llave **Access Key** en un lugar seguro, ya que será usado mas adelante. 

## Creación de roles
Los siguientes pasos a seguir son para crear los roles de _KueskiPay_ y otorgarles los permisos necesarios para el buen funcionamiento del método de pago.

1. En el menú del lado izquierdo, seguir el siguiente flujo **ACCOUNT SETTINGS** -> **Account management** -> **Roles**.
2. Dar click al botón **New Role**. <br>
Se abrirá una página para crear el nuevo rol. 
3. En el campo **Choose role** elegir la opción **Custom**.
4. En el campo **Role name** escribir `KueskiPay`.
5. En la sección **Products and Resources** activar los siguientes permisos:

![Screen Shot 2022-04-13 at 17 59 56](https://user-images.githubusercontent.com/101224062/163288671-47c93d24-fb72-4411-9225-567fc766370f.png)

> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> Marcar solo las casillas mostradas en la **Tabla 1**, ya que de haber una configuración diferente, puede causar errores en el funcionamiento de KueskiPay.

6. Dar click al botón **Save**.<br>
Los permisos están configurados. 

## Asignación de permisos a Application Keys
Los siguientes pasos a seguir son para asignarle permisos del rol _KueskiPay_ a los Application Keys.

1. En el menú del lado izquierdo, seguir el siguiente flujo: **Account Settings** -> **Account management** -> **Application keys**.
2. Dar click al botón **+ ADD** (
![Screen Shot 2022-04-13 at 18 04 08](https://user-images.githubusercontent.com/101224062/163289027-98c15ccc-6d4d-4ce8-8695-47304d45f687.png)
)
3. En el campo **Key** escribir el _Access key_ guardada en la sección **Generar credenciales VTEX IO** en el paso 11.
4. Dar click al botón **+ ADD Roles** (
![Screen Shot 2022-04-14 at 11 20 44](https://user-images.githubusercontent.com/101224062/163440842-97871f0d-8bd3-496a-8fcb-f31a420767da.png)
).
5. Seleccionar el rol de **KueskiPay**.
6. Dar click al botón **ADD ROLES** (
![Screen Shot 2022-04-14 at 11 21 40](https://user-images.githubusercontent.com/101224062/163441008-70c62b8b-2dea-41ad-883d-9d5415192f1d.png)
). <br>
El rol _KueskiPay_ debe de verse en la tabla **Add roles**.
7. Dar click al botón **SAVE**. <br>
La llave _Access Key_ debe de estar Activa. 

![Screen Shot 2022-04-14 at 11 22 48](https://user-images.githubusercontent.com/101224062/163441153-5842bbde-cfa7-4581-bd61-5a5349ef08a4.png)

