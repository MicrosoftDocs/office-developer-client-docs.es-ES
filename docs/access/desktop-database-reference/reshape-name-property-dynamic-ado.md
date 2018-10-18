---
title: dinámica Reshape Name (propiedad, ADO)
TOCTitle: Reshape Name Property--Dynamic (ADO)
ms:assetid: 59ef99c8-da40-5cf6-b987-d47ea1433f45
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249307(v=office.15)
ms:contentKeyID: 48545030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bebdec8bdc68724522331714052a0079f75b28e3
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603171"
---
# <a name="reshape-name-property--dynamic-ado"></a>dinámica Reshape Name (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Especifica un nombre para el objeto [Recordset](recordset-object-ado.md).

<<<<<<< HEAD
## <a name="return-values"></a>Valores devueltos
=======
## <a name="return-values"></a>Valores devueltos
>>>>>>> master

Devuelve un valor de tipo **String** que es el nombre del objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Los nombres se conservan durante la conexión o hasta que se cierra el objeto **Recordset**.

La propiedad **Reshape Name** está destinada al uso con la característica de cambio de forma del proveedor de servicios del [Servicio de forma de datos de Microsoft para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md). Para poder participar en el cambio de forma, los nombres deben ser exclusivos.

Esta propiedad es de sólo lectura, aunque se puede establecer de forma indirecta al crear un objeto Recordset. Por ejemplo, si una cláusula de un comando SHAPE crea un objeto Recordset y le asigna un nombre de alias con la palabra clave "AS", el alias se asigna a la propiedad Reshape Name. Si no se declara ningún alias, a la propiedad se le asigna un nombre exclusivo generado por el servicio de forma de datos. Si el nombre de alias es el mismo que el de un objeto **Recordset** existente, ninguno de estos objetos **Recordset** cambiará de forma hasta que se libere alguno. Es posible cambiar el comportamiento predeterminado si se establece la propiedad "Ubique Reshape Names" (vea "Servicio de forma de datos de Microsoft para OLE DB") de la conexión ADO en TRUE. Así se concede permiso al servicio de forma de datos para cambiar los nombres de usuario asignados si eso fuera necesario para garantizar la exclusividad.

Utilice la propiedad **Reshape Name** cuando desee hacer referencia a un objeto **Recordset** en un comando SHAPE o cuando no conozca el nombre debido a que ha sido generado por el Servicio de forma de datos. En ese caso, es posible generar un comando SHAPE al concatenar el comando con la cadena devuelta por la propiedad **Reshape Name**.

**Reshape Name** es una propiedad dinámica que se anexa a la colección **Properties** del objeto [Recordset](properties-collection-ado.md) cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.

