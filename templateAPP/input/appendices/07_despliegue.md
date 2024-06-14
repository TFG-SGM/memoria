# Despliegue de DynaViz

En este anexo se presenta un detallado proceso para desplegar la aplicación *DynaViz* en un entorno real junto con la estimación del coste final del despliegue. Para implementar una aplicación Web de manera efectiva se requiere configurar un dominio y desplegar tanto el lado del cliente como el servidor, además de la base de datos correspondiente. A continuación, se presenta una descripción detallada de cada uno de estos elementos.

## Proveedor de Dominio

Un proveedor de dominio, como lo describe Balkhi @domain-providers, es una empresa que facilita la compra y registro de nombres de dominio. Esto permite acceder a las páginas Web utilizando palabras fáciles de recordar en lugar de direcciones IP.

Los precios de los dominios varían según los servicios ofrecidos y la extensión del dominio. La Figura \ref{anexo7:domain-providers} muestra algunos de los proveedores de dominios más populares junto con sus precios, como se detalla en *domcomp* @domain-pricing.

Para *DynaViz*, una opción recomendada es utilizar *NameCheap*, ya que ofrece precios competitivos y es ampliamente reconocido en la actualidad.

Una vez seleccionado el proveedor de dominios, en el siguiente punto se procede a analizar el proveedor de hosting.

| **Servicio**         | **Nuevo dominio** | **Renovación anual** |
| -------------------- | ----------------- | -------------------- |
| z.com @zcom          | $5.90             | $10.18               |
| namecheap @namecheap | $5.98             | $11.88               |
| spaceship @spaceship | $8.06             | $8.06                |
| dynadot @dynadot     | $10.19            | $10.19               |

: Comparativa de precios de prooveedores de dominio\label{anexo7:domain-providers}

## Proveedor de Hosting

En cuanto al hosting, una opción viable para *DynaViz* es continuar utilizando *Render*, donde los pagos se ajustan según el uso de la aplicación Web.

*Render* ofrece planes mensuales con diversos beneficios, así como opciones basadas en el uso, como se detalla en su página oficial @render-pricing. Los planes mensuales disponibles se presentan en la Figura \ref{anexo7:render-plans}. Además, para *DynaViz* se requieren dos componentes: un "sitio estático" para el lado del cliente y un "servicio Web" para el lado del servidor.

| **Caracteristicas**        | **Individual** | **Team**        | **Organization** | **Enterprise** |
| ------------------------ | --------- | ---------------- | ----------------- | ------- |
| **Precio**                 | Gratis     | $19/usuario-mes | $29/usuario-mes | Custom     |
| **Minutos de pipeline gratis** | 500/mes    | 500/usuario-mes | 500/usuario-mes | Custom     |
| **Ancho de banda gratis**  | 100 GB     | 500 GB          | 1 TB            | Custom     |
| **Autoescalado**           | No         | Si              | Si              | Si         |

: Planes mensuales de *Render*\label{anexo7:render-plans}

El "sitio estático" ofrece ventajas como un [CDN](#CDN) ultrarrápido, implementaciones automáticas continuas desde Git, invalidación instantánea de caché y dominios personalizados con [TLS](#TLS) completamente administrado, todo ello de forma gratuita.

El coste del "servicio Web" depende de la instancia seleccionada, como se muestra en la Figura \ref{anexo7:render-web-services}. Estas instancias se pueden adaptar según las necesidades de la aplicación.

Una vez elegido el proveedor de hosting, el siguiente paso es analizar la opción más adecuada para la base de datos.

| **Tipo de Instancia** | **Precio** | **RAM** | **CPU** |
| --------------------- | ---------- | ------- | ------- |
| Free                  | $0/mes     | 512 MB  | 0.1     |
| Starter               | $7/mes     | 512 MB  | 0.5     |
| Standard              | $25/mes    | 2 GB    | 1       |
| Pro                   | $85/mes    | 4 GB    | 2       |
| Pro Plus              | $175/mes   | 8 GB    | 4       |
| Pro Max               | $225/mes   | 16 GB   | 4       |
| Pro Ultra             | $450/mes   | 32 GB   | 8       |
| Custom                | Contacto   | +512 GB | +64     |

: Instancias de servicios Web de *Render* @render-pricing\label{anexo7:render-web-services}

## Proveedor de Base de Datos

Para la base de datos, al igual que con el hosting, *MongoDB Atlas* sigue siendo una opción sólida. Este servicio ofrece tres planes distintos, como se detalla en su página oficial @mongodb-pricing:

- **Compartido:** es el plan más económico y el que actualmente se utiliza. Los diferentes precios de este plan se muestran en la Figura \ref{anexo7:mongodb-shared}.
- **Dedicado:** ofrece características mejoradas a cambio de un coste mayor. Los precios de este plan se muestran en la Figura \ref{anexo7:mongodb-dedicated}.
- **Serverless:** este plan ofrece un servicio de pago según el uso. Las características y los precios de este plan se detallan en la Figura \ref{anexo7:mongodb-serverless}.

Para *DynaViz*, una opción recomendada es utilizar el plan *Serverless*. De esta manera, la base de datos puede escalar junto con la aplicación Web conforme se le vaya dando uso con el tiempo.

| **Almacenamiento** | **RAM**    | **vCPUs**  | **Precio** |
| ------------------ | ---------- | ---------- | ---------- |
| 512 MB             | Compartido | Compartido | Gratis     |
| 2 GB               | Compartido | Compartido | $9/mes     |
| 5 GB               | Compartido | Compartido | $25/mes    |

: Plan compartido de *MongoDB Atlas*\label{anexo7:mongodb-shared}

| **Almacenamiento** | **RAM** | **vCPUs** | **Precio**  |
| ------------------ | ------- | --------- | ----------- |
| 10 GB              | 2 GB    | 2         | $0.08/hora  |
| 1000 GB            | 192 GB  | 48        | $10.99/hora |
| 4000 GB            | 768 GB  | 96        | $33.26/hora |

: Plan dedicado de *MongoDB Atlas*\label{anexo7:mongodb-dedicated}

| **Item**               | **Descripción**                    | **Precio**                                     |
| ------------------------- | ---------------------------------- | ----------------- |
| RPU            | Número de operaciones de lectura   | $0.10/millón [^anexo7:rpu]                     |
| WPU            | Número de operaciones de escritura | $1.00/millón                                   |
| Almacenamiento         | Datos guardados                    | $0.25 / GB-mes                                 |
| Transferencia de datos | Datos entrantes y salientes        | $0.01 - $0.20/GB [^anexo7:transferencia-datos] |

: Plan serverless de *MongoDB Atlas*\label{anexo7:mongodb-serverless}

## Conclusiones

En conclusión, con un proveedor de dominios, un proveedor de hosting como *Render* y un proveedor de bases de datos como *MongoDB Atlas* se conseguirá desplegar la aplicación *DynaViz* de manera que el coste dependerá del uso que se le dé.

A modo de ilustración, en la Tabla \ref{anexo7:suposiciones-mongodb} se realiza una estimación basada en un uso promedio de la aplicación Web en relación con la base de datos, dando como resultado un precio final de $40 al mes. Además, en la Tabla \ref{anexo7:suposiciones-servicios} se opta por utilizar *Namecheap* para el dominio, el plan *Individual* de *Render* y la instancia *Standard* del servicio Web proporcionado por *Render*.

Con base en lo anterior, se llega a las conclusiones presentadas en la Tabla \ref{anexo7:precios-finales}. El primer mes implicaría un coste de $70.98 debido al pago inicial de *Namecheap*. Posteriormente, cada mes tendría un coste de $65 y cada primer mes del año requeriría $76.88 para renovar el dominio en *Namecheap*.

| **Item**               | **Suposición de uso**                         | **Precio** |
| ---------------------- | --------------------------------------------- | ---------- |
| RPU                    | 25 millones                                   | $2.50      |
| WPU                    | 5 millones                                    | $5.00      |
| Almacenamiento         | 100 GB                                        | $25        |
| Transferencia de datos | 150 GB (a un precio promedio de $0.05 por GB) | $7.50      |

: Suposiciones de uso de *MongoDB Atlas*\label{anexo7:suposiciones-mongodb}

| **Servicios**                   | **Elección**  | **Precio** | **Renovación anual** |
| ------------------------------- | ------------------ | ---------- | -------------------- |
| Proveedor de dominios           | Namecheap     | $5.98      | $11.88               |
| Render - Plan mensual           | Individual    | $0         | -                    |
| Render - Instancia Servicio Web | Standard      | $25/mes    | -                    |
| Base de datos                   | MongoDB Atlas | $40/mes    | -                    |

: Suposiciones de uso de servicios\label{anexo7:suposiciones-servicios}

| **Concepto**        | **Coste** |
| ------------------- | --------- |
| Primer mes          | $70.98    |
| Meses subsiguientes | $65       |
| Renovación anual    | $76.88    |

: Precios finales según suposiciones\label{anexo7:precios-finales}

[^anexo7:rpu]: Para los primeros 50 millones por día
[^anexo7:transferencia-datos]: Dependiendo del tráfico de la fuente y del destino
