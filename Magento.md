# Antes de iniciar
Los requisitos para instalar el método de pago Kueski Pay en Magento son los siguientes:

* Versión Magento: `>= 2.3.0 || 2.4.3 <=`
* Versión PHP: `>= 7.3 || 8.0 <`
* Versión Composer: `composer V1.X || composer V2.X`
* Composer Stability: `stable`

> :warning: :heavy_exclamation_mark: **IMPORTANTE:**  
> Estos requisitos son para la versión actual del plugin marcada como paquete _stable_. 

# Instalar plugin de Kueski Pay
Los siguientes pasos a seguir son necesarios para instalar el plugin de _Kueski Pay_ en tu plataforma de Magento y poder hacer uso de su método de pago. 

1. Abre la terminal.
2. Ve a la carpeta raíz del proyecto de Magento. _(Esta carpeta puede variar de un proyecto a otro)._
3. Escribe en la terminal los siguientes comandos: <br>
```
composer require kueski/magento2-payment
php bin/magento module:enable Kueski_Payment
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento cache:clean
php bin/magento cache:flush
```




