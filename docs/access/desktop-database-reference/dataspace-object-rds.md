---
title: DataSpace (objeto) (RDS)
TOCTitle: DataSpace object (RDS)
ms:assetid: 7db181d5-422b-49fe-b6af-a20f5da520ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249527(v=office.15)
ms:contentKeyID: 48545862
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f77617d4ddfb0160b8a418f55582a380067fde70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294466"
---
# <a name="dataspace-object-rds"></a>DataSpace (objeto) (RDS)

**Se aplica a:** Access 2013, Office 2013

Crea proxies de cliente a objetos de negocio personalizados ubicados en el nivel medio.

## <a name="remarks"></a>Comentarios

El servicio de datos remotos necesita servidores proxy de objetos de negocio para que un componente de cliente pueda establecer comunicación con objetos de negocio ubicados en el nivel medio. Los servidores proxy facilitan el empaquetado, desempaquetado y transporte (cálculo de referencias) de los datos [Recordset](recordset-object-ado.md) de la aplicación mediante límites de procesos o de equipo.

El servicio de datos remotos utiliza el método **CreateObject** del objeto [RDS.DataSpace](createobject-method-rds.md) para crear servidores proxy de objetos de negocio. El proxy de objetos de negocio se crea dinámicamente cada vez que se crea una instancia de su equivalente objeto de negocio de nivel medio. Además, admite los protocolos siguientes: HTTP, HTTPS (HTTP Secure Sockets), DCOM y en proceso (los componentes de cliente y el objeto de negocio residen en el mismo equipo).

> [!NOTE]
> [!NOTA] El servicio de datos remotos (RDS) se comporta de forma "independiente" cuando el objeto **RDS.DataSpace** utiliza los protocolos HTTP o HTTPS. Es decir, se descarta la información interna sobre una solicitud de cliente después de que el servidor devuelva una respuesta.

Aunque parezca que el objeto de negocio existe durante la vida útil del proxy de objetos de negocio, sólo existe realmente hasta que se envía una respuesta a una solicitud. Cuando se emite una solicitud (es decir, se llama a un método en el objeto de negocio), el proxy abre una nueva conexión con el servidor y el servidor crea una nueva instancia del objeto de negocio. Una vez que el objeto de negocio responde a la solicitud, el servidor lo destruye y cierra la conexión.

Este comportamiento significa que no se pueden pasar datos de una solicitud a otra mediante el uso de una variable o una propiedad de objeto de negocio. Se debe utilizar otro mecanismo, como un archivo o un argumento de método, para conservar los datos de estado.

El identificador de clase para el objeto **RDS.DataSpace** es BD96C556-65A3-11D0-983A-00C04FC29E36.

