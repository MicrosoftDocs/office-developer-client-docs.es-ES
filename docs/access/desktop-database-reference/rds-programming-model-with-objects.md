---
title: Modelo de programación de RDS con objetos
TOCTitle: RDS programming model with objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9743fb1e7329457abb60ed8ed41bc39067f3551d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710968"
---
# <a name="rds-programming-model-with-objects"></a>Modelo de programación de RDS con objetos

**Se aplica a**: Access 2013, Office 2013

El objetivo de RDS es obtener acceso y actualizar los orígenes de datos a través de un intermediario como IIS. El modelo de programación especifica la secuencia de las actividades necesarias para lograr este objetivo. El modelo de objetos especifica los objetos cuyos métodos y propiedades afectan al modelo de programación.

RDS proporciona el medio para realizar la siguiente secuencia de acciones:

- Especifique el programa que se va a invocar en el servidor y obtenga una forma (proxy) de hacer referencia al mismo desde el cliente ([RDS.DataSpace](dataspace-object-rds.md)).

- Invoque el programa de servidor. Pase al programa de servidor los parámetros que identifiquen el origen de datos y el comando que se va a emitir (proxy o [ RDS.DataControl ](datacontrol-object-rds.md)).

- El programa de servidor obtiene un objeto [Recordset](recordset-object-ado.md) desde el origen de datos, normalmente mediante ADO. De manera opcional, el objeto **Recordset** se procesa en el servidor ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).

- El programa de servidor devuelve el objeto **Recordset** final a la aplicación de cliente (proxy).

- En el cliente, el objeto **Recordset** se coloca de manera que los controles visuales lo puedan utilizar fácilmente (control visual y **RDS.DataControl**).

- Los cambios realizados en el objeto **Recordset** se envían de nuevo al servidor y se utilizan para actualizar el origen de datos (**RDS.DataControl** o **RDSServer.DataFactory**).

