---
title: Crear una conexión
TOCTitle: Making a connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 487212acd8847928e1fab405593edb172d0172d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289787"
---
# <a name="making-a-connection"></a>Crear una conexión

**Se aplica a:** Access 2013, Office 2013

Para conectarse a un origen de datos, debe especificar una *cadena de conexión*, cuyos parámetros podrían ser distintos para cada proveedor y para cada origen de datos. Para obtener más información, vea [Crear la cadena de conexión](creating-the-connection-string.md).

Lo más normal es que ADO abra una conexión utilizando el método **Open** del objeto **Connection**. La sintaxis del método **Open** se muestra aquí:

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

Otra posibilidad es invocar una técnica de acceso directo, **Recordset.Open**, para abrir una conexión implícita y emitir un comando a través de esa conexión en una sola operación. Para hacerlo, pase una cadena de conexión válida como argumento *ActiveConnection* para el método **Open**. Esta es la sintaxis para cada método en Visual Basic:

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> [!NOTA] ¿Cuándo conviene utilizar un objeto **Connection** y cuando el acceso directo **Recordset.Open** ? Utilice el objeto **Connection** si piensa abrir más de un **conjunto de registros**, o cuando tenga que ejecutar varios comandos. ADO sigue creando una conexión implícitamente cuando se utiliza el acceso directo **Recordset.Open**.


