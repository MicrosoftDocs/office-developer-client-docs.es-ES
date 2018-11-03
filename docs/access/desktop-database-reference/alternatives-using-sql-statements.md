---
title: 'Alternativas: Utilizar instrucciones SQL'
TOCTitle: 'Alternatives: Using SQL statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bcda13d8b785f1048890d1ed9492f5da3e7288b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945561"
---
# <a name="alternatives-using-sql-statements"></a>Alternativas: Utilizar instrucciones SQL


**Se aplica a**: Access 2013, Office 2013

ADO también permite utilizar comandos como alternativa a sus propiedades y métodos integrados para modificar datos. Dependiendo de su proveedor, todas las operaciones mencionadas en este capítulo también se podrían realizar pasando comandos a su origen de datos. Por ejemplo, se pueden utilizar instrucciones SQL UPDATE para modificar datos sin usar la propiedad **Valor** de un **campo**. Se pueden utilizar instrucciones INSERT para agregar nuevos registros a un origen de datos, en lugar del método **AddNew** de ADO. Para obtener más información acerca de SQL o el lenguaje de manipulación de datos de su proveedor, vea la documentación de su origen de datos.

Por ejemplo, puede pasar una cadena SQL que contiene una instrucción DELETE a una base de datos, como se muestra en el código siguiente:

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

