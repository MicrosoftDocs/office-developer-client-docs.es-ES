---
title: Modelo de programación básico de RDS
TOCTitle: Basic RDS programming model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad7a6d31fa973ffd8d04b4478d73a88312d52073
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944818"
---
# <a name="basic-rds-programming-model"></a>Modelo de programación básico de RDS

**Se aplica a**: Access 2013, Office 2013

RDS se orienta a las aplicaciones que existen en el entorno siguiente: una aplicación de cliente especifica un programa que se ejecutará en un servidor y los parámetros necesarios para que se devuelva la información deseada. El programa invocado en el servidor obtiene acceso al origen de datos especificado, recupera la información, procesa los datos opcionalmente y devuelve la información resultante a la aplicación de cliente de modo que pueda utilizarse fácilmente. RDS permite llevar a cabo la siguiente secuencia de acciones:

- Especifique el programa que se va a invocar en el servidor y haga referencia al mismo desde el cliente. (Esta referencia se denomina a veces un servidor * proxy*. Representa el programa de servidor remoto. La aplicación de cliente "llamará" al proxy como si fuese un programa local pero, en realidad, invoca el programa de servidor remoto.)

- Invoque el programa de servidor. Pase al programa de servidor los parámetros que identifiquen el origen de datos y el comando que se va a emitir. (En realidad, el programa de servidor utiliza ADO para obtener acceso al origen de datos. ADO establece una conexión con uno de los parámetros especificados y, después, emite el comando especificado en el otro parámetro.)

- El programa de servidor obtiene un objeto [Recordset](recordset-object-ado.md) desde el origen de datos. El objeto **Recordset** se procesa opcionalmente en el servidor.

- El programa de servidor devuelve el objeto **Recordset** final a la aplicación de cliente.

- En el cliente, el objeto **Recordset** se coloca de manera que los controles visuales lo puedan utilizar fácilmente.

- Cualquier modificación que se realice en el objeto ** Recordset** se envía de nuevo al programa de servidor, que las usa para actualizar el origen de datos.

Este modelo de programación contiene algunas características prácticas. Si no necesita un programa de servidor complejo para obtener acceso al origen de datos y si proporciona los parámetros de conexión y comando necesarios, RDS recuperará automáticamente los datos especificados con un sencillo programa de servidor predeterminado.

Si necesita un procesamiento más complejo, puede especificar su propio programa de servidor personalizado. Por ejemplo, dado que un programa de servidor personalizado tiene a su disposición todas las funciones de ADO, podrá conectarse a varios orígenes de datos, combinar sus datos de alguna manera compleja y, a continuación, devolver un resultado simple procesado a la aplicación de cliente.

Finalmente, si sus necesidades son intermedias, ADO admite ahora la personalización del comportamiento del programa de servidor predeterminado.

