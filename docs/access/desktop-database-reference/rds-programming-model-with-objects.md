---
title: Modelo de programación de RDS con objetos
TOCTitle: RDS Programming Model with Objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 833d3676c8fa3fac1e5cb8e16477073cde611199
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484294"
---
# <a name="rds-programming-model-with-objects"></a>Modelo de programación de RDS con objetos


**Se aplica a**: Access 2013 | Office 2013

El objetivo de RDS es obtener acceso y actualizar los orígenes de datos a través de un intermediario como IIS. El modelo de programación especifica la secuencia de las actividades necesarias para lograr este objetivo. El modelo de objetos especifica los objetos cuyos métodos y propiedades afectan al modelo de programación.

RDS proporciona el medio para realizar la siguiente secuencia de acciones:

  - Especifique el programa que se va a invocar en el servidor y obtenga una forma (proxy) de hacer referencia al mismo desde el cliente ([RDS.DataSpace](dataspace-object-rds.md)).

  - Invoque el programa de servidor. Pase al programa de servidor los parámetros que identifiquen el origen de datos y el comando que se va a emitir (proxy o [ RDS.DataControl ](datacontrol-object-rds.md)).

  - El programa de servidor obtiene un objeto [Recordset](recordset-object-ado.md) desde el origen de datos, normalmente mediante ADO. De manera opcional, el objeto **Recordset** se procesa en el servidor ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).

  - El programa de servidor devuelve el objeto **Recordset** final a la aplicación de cliente (proxy).

  - En el cliente, el objeto **Recordset** se coloca de manera que los controles visuales lo puedan utilizar fácilmente (control visual y **RDS.DataControl**).

  - Los cambios realizados en el objeto **Recordset** se envían de nuevo al servidor y se utilizan para actualizar el origen de datos (**RDS.DataControl** o **RDSServer.DataFactory**).

