---
title: AbsolutePosition (propiedad, ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: a090630b5db741f761314f598fcc783dd124d1cf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881863"
---
# <a name="absoluteposition-property-ado"></a><span data-ttu-id="dcaa7-102">AbsolutePosition (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="dcaa7-102">AbsolutePosition property (ADO)</span></span>

<span data-ttu-id="dcaa7-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dcaa7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dcaa7-104">Indica la posición ordinal del registro actual de un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="dcaa7-104">Indicates the ordinal position of a [Recordset](recordset-object-ado.md) object's current record.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="dcaa7-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="dcaa7-105">Settings and return values</span></span>

<span data-ttu-id="dcaa7-106">Establece o devuelve un valor de tipo **Long** comprendido entre 1 y el número de registros del objeto **Recordset** ([RecordCount](recordcount-property-ado.md)), o bien, devuelve uno de los valores de [PositionEnum](positionenum.md).</span><span class="sxs-lookup"><span data-stu-id="dcaa7-106">Sets or returns a **Long** value from 1 to the number of records in the **Recordset** object ([RecordCount](recordcount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcaa7-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dcaa7-107">Remarks</span></span>

<span data-ttu-id="dcaa7-108">Para establecer la propiedad **AbsolutePosition** , ADO requiere que el proveedor OLE DB que esté utilizando implemente la interfaz IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="dcaa7-108">To set the **AbsolutePosition** property, ADO requires that the OLE DB provider you are using implement the IRowsetLocate interface.</span></span>

<span data-ttu-id="dcaa7-p101">Al obtener acceso a la propiedad **AbsolutePosition** de un objeto **Recordset** que se ha abierto con un cursor de sólo avance o un cursor dinámico, se genera el error **adErrFeatureNotAvailable**. Con otros tipos de cursor, se devolverá la posición correcta, siempre y cuando el proveedor admita la interfaz IRowsetScroll. Si el proveedor no admite la interfaz *IRowsetScroll*, el valor de la propiedad se establece en **adPosUnknown**. Vea la documentación de su proveedor para determinar si admite *IRowsetScroll*.</span><span class="sxs-lookup"><span data-stu-id="dcaa7-p101">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**. With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface. If the provider does not support the *IRowsetScroll* interface, the property is set to **adPosUnknown**. See the documentation for your provider to determine whether it supports *IRowsetScroll*.</span></span>

<span data-ttu-id="dcaa7-p102">Use la propiedad **AbsolutePosition** para desplazarse a un registro basándose en su posición ordinal en el objeto **Recordset** o para especificar la posición ordinal del registro actual. El proveedor debe admitir la funcionalidad adecuada para que esta propiedad esté disponible.</span><span class="sxs-lookup"><span data-stu-id="dcaa7-p102">Use the **AbsolutePosition** property to move to a record based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="dcaa7-p103">Al igual que la propiedad [AbsolutePage](absolutepage-property-ado.md), **AbsolutePosition** se basa en 1 y es igual a 1 cuando el registro actual es el primer registro del objeto **Recordset**. Se puede obtener el número total de registros del objeto **Recordset** mediante la propiedad [RecordCount](recordcount-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="dcaa7-p103">Like the [AbsolutePage](absolutepage-property-ado.md) property, **AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. You can obtain the total number of records in the **Recordset** object from the [RecordCount](recordcount-property-ado.md) property.</span></span>

<span data-ttu-id="dcaa7-117">Cuando se establece la propiedad **AbsolutePosition** , incluso si se va a un registro en la memoria caché actual, ADO vuelve a cargar la memoria caché con un nuevo grupo de registros empezando por el registro que ha especificado.</span><span class="sxs-lookup"><span data-stu-id="dcaa7-117">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record that you specified.</span></span> <span data-ttu-id="dcaa7-118">La propiedad [CacheSize](cachesize-property-ado.md) determina el tamaño de este grupo.</span><span class="sxs-lookup"><span data-stu-id="dcaa7-118">The [CacheSize](cachesize-property-ado.md) property determines the size of this group.</span></span>


> [!NOTE]
> <span data-ttu-id="dcaa7-119">[!NOTA] No es aconsejable usar la propiedad **AbsolutePosition** como número de registro suplente.</span><span class="sxs-lookup"><span data-stu-id="dcaa7-119">You should not use the **AbsolutePosition** property as a surrogate record number.</span></span> <span data-ttu-id="dcaa7-120">La posición de un registro determinado cambia cuando se elimina un registro anterior.</span><span class="sxs-lookup"><span data-stu-id="dcaa7-120">The position of a given record changes when you delete a preceding record.</span></span> <span data-ttu-id="dcaa7-121">No hay ninguna garantía de que un registro determinado tenga el mismo **AbsolutePosition** si se vuelve a consultar o se vuelve a abrir el objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="dcaa7-121">There is also no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened.</span></span> <span data-ttu-id="dcaa7-122">Los marcadores siguen siendo la forma recomendada de conservar y volver a una posición determinada y son la única manera de ubicarse a través de todos los tipos de objetos **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="dcaa7-122">Bookmarks are still the recommended way of retaining and returning to a given position, and are the only way of positioning across all types of **Recordset** objects.</span></span>


