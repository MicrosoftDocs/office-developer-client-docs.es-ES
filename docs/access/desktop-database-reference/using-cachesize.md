---
title: Utilizar CacheSize (referencia de escritorio de la base de datos de Access)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8e4937ee83251f9e4114827860da2ea571887ad8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485368"
---
# <a name="using-cachesize"></a>Utilizar CacheSize


**Se aplica a**: Access 2013 | Office 2013

Use la propiedad **CacheSize** para controlar el número de registros que se van a recuperar a la vez en la memoria local del proveedor. Por ejemplo, si el valor de **CacheSize** es 10, tras abrir el objeto **Recordset**, el proveedor recupera los 10 primeros registros en la memoria local. Cuando el usuario se mueve por el objeto **Recordset**, el proveedor devuelve los datos desde el búfer de memoria local. Cuando el usuario se desplaza hasta un punto situado más allá del último registro de la memoria caché, el proveedor recupera en la memoria caché los 10 siguientes registros del origen de datos.


> [!NOTE]
> <P>[!NOTA] <STRONG>CacheSize</STRONG> se basa en la propiedad específica del proveedor <STRONG>Número máximo de filas abiertas</STRONG> (en la colección <STRONG>Properties</STRONG> del objeto <STRONG>Recordset</STRONG> ). No puede establecer <STRONG>CacheSize</STRONG> en un valor mayor que el valor de <STRONG>Número máximo de filas abiertas</STRONG>. Para modificar el número de filas que puede abrir el proveedor, establezca el valor de <STRONG>Número máximo de filas abiertas</STRONG>.</P>



El valor de **CacheSize** se puede ajustar durante la vida del objeto **Recordset**, pero cambiar este valor solo afecta al número de registros en la memoria caché después de recuperaciones posteriores desde el origen de datos. Si solo se cambia el valor de la propiedad, el contenido de la memoria caché en ese momento no cambiará.

Si hay menos registros para recuperar que la cantidad especificada con **CacheSize**, el proveedor devuelve los registros restantes y no se produce ningún error.

No se puede establecer **CacheSize** en cero, ya que devolvería un error.

Los registros recuperados de la caché no reflejan cambios simultáneos realizados por otros usuarios en los datos del origen. Para forzar una actualización de todos los datos en caché, utilice el método [Resync](resync-method-ado.md).

Si **CacheSize** se establece en un valor mayor que 1, los métodos de navegación ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext y MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) pueden provocar la navegación a un registro eliminado, si la eliminación se efectuó después de haber recuperado los registros. Después de la recuperación inicial, las eliminaciones posteriores no se reflejarán en su caché de datos hasta que intente obtener acceso a un valor de datos de una fila eliminada. Sin embargo, si se establece **CacheSize** en 1, se elimina este problema porque no se pueden recuperar filas eliminadas.

