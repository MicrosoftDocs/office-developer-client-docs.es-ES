---
title: AbsolutePosition (propiedad, ADO)
TOCTitle: AbsolutePosition Property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3258ffcab87b16e4931c9881a8e8d1cd2143262f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486270"
---
# <a name="absoluteposition-property-ado"></a><span data-ttu-id="4dd1f-102">AbsolutePosition (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="4dd1f-102">AbsolutePosition Property (ADO)</span></span>


<span data-ttu-id="4dd1f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4dd1f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4dd1f-104">Indica la posición ordinal del registro actual de un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4dd1f-104">Indicates the ordinal position of a [Recordset](recordset-object-ado.md) object's current record.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4dd1f-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4dd1f-105">Settings and Return Values</span></span>

<span data-ttu-id="4dd1f-106">Establece o devuelve un valor de tipo **Long** comprendido entre 1 y el número de registros del objeto **Recordset** ([RecordCount](recordcount-property-ado.md)), o bien, devuelve uno de los valores de [PositionEnum](positionenum.md).</span><span class="sxs-lookup"><span data-stu-id="4dd1f-106">Sets or returns a **Long** value from 1 to the number of records in the **Recordset** object ([RecordCount](recordcount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dd1f-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4dd1f-107">Remarks</span></span>

<span data-ttu-id="4dd1f-108">Para establecer la propiedad **AbsolutePosition**, ADO requiere que el proveedor OLE DB utilizado implemente la interfaz IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="4dd1f-108">In order to set the **AbsolutePosition** property, ADO requires that the OLE DB provider you are using implement the IRowsetLocate interface.</span></span>

<span data-ttu-id="4dd1f-p101">Al obtener acceso a la propiedad **AbsolutePosition** de un objeto **Recordset** que se ha abierto con un cursor de sólo avance o un cursor dinámico, se genera el error **adErrFeatureNotAvailable**. Con otros tipos de cursor, se devolverá la posición correcta, siempre y cuando el proveedor admita la interfaz IRowsetScroll. Si el proveedor no admite la interfaz *IRowsetScroll*, el valor de la propiedad se establece en **adPosUnknown**. Vea la documentación de su proveedor para determinar si admite *IRowsetScroll*.</span><span class="sxs-lookup"><span data-stu-id="4dd1f-p101">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**. With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface. If the provider does not support the *IRowsetScroll* interface, the property is set to **adPosUnknown**. See the documentation for your provider to determine whether it supports *IRowsetScroll*.</span></span>

<span data-ttu-id="4dd1f-p102">Use la propiedad **AbsolutePosition** para desplazarse a un registro basándose en su posición ordinal en el objeto **Recordset** o para especificar la posición ordinal del registro actual. El proveedor debe admitir la funcionalidad adecuada para que esta propiedad esté disponible.</span><span class="sxs-lookup"><span data-stu-id="4dd1f-p102">Use the **AbsolutePosition** property to move to a record based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="4dd1f-p103">Al igual que la propiedad [AbsolutePage](absolutepage-property-ado.md), **AbsolutePosition** se basa en 1 y es igual a 1 cuando el registro actual es el primer registro del objeto **Recordset**. Se puede obtener el número total de registros del objeto **Recordset** mediante la propiedad [RecordCount](recordcount-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4dd1f-p103">Like the [AbsolutePage](absolutepage-property-ado.md) property, **AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. You can obtain the total number of records in the **Recordset** object from the [RecordCount](recordcount-property-ado.md) property.</span></span>

<span data-ttu-id="4dd1f-p104">Cuando establece la propiedad **AbsolutePosition**, incluso estableciéndola en un registro de la caché actual, ADO vuelve a cargar la caché con un nuevo grupo de registros empezando por el registro especificado. La propiedad [CacheSize](cachesize-property-ado.md) determina el tamaño de este grupo.</span><span class="sxs-lookup"><span data-stu-id="4dd1f-p104">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified. The [CacheSize](cachesize-property-ado.md) property determines the size of this group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4dd1f-p105">[!NOTA] La propiedad <STRONG>AbsolutePosition</STRONG> no debe utilizarse como un número de registro suplente. La posición de un registro determinado cambia al eliminar un registro anterior. Tampoco hay ninguna garantía de que un registro determinado tenga el mismo valor de <STRONG>AbsolutePosition</STRONG> si se vuelve a consultar o a abrir el objeto <STRONG>Recordset</STRONG>. Se recomienda usar marcadores para mantener y volver a una posición determinada. Además, son la única forma de establecer el posicionamiento en todos los tipos de objetos <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="4dd1f-p105">You should not use the <STRONG>AbsolutePosition</STRONG> property as a surrogate record number. The position of a given record changes when you delete a preceding record. There is also no assurance that a given record will have the same <STRONG>AbsolutePosition</STRONG> if the <STRONG>Recordset</STRONG> object is requeried or reopened. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way of positioning across all types of <STRONG>Recordset</STRONG> objects.</span></span></P>


