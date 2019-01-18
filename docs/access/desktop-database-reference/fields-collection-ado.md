---
title: Fields (colección, ADO)
TOCTitle: Fields collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a537756483361733c087d5dc1c6bba6e649d17d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726263"
---
# <a name="fields-collection-ado"></a><span data-ttu-id="811ae-102">Fields (colección, ADO)</span><span class="sxs-lookup"><span data-stu-id="811ae-102">Fields collection (ADO)</span></span>


<span data-ttu-id="811ae-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="811ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="811ae-104">Contiene todos los objetos [Field](field-object-ado.md) de un objeto [Recordset](recordset-object-ado.md) o [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="811ae-104">Contains all the [Field](field-object-ado.md) objects of a [Recordset](recordset-object-ado.md) or [Record](record-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="811ae-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="811ae-105">Remarks</span></span>

<span data-ttu-id="811ae-p101">Los objetos **Recordset** tienen una colección **Fields** formada por objetos **Field**. Cada objeto **Field** corresponde a una columna del objeto **Recordset**. Puede rellenar la colección **Fields** antes de abrir el objeto **Recordset** llamando al método [Refresh](refresh-method-ado.md) en la colección.</span><span class="sxs-lookup"><span data-stu-id="811ae-p101">A **Recordset** object has a **Fields** collection made up of **Field** objects. Each **Field** object corresponds to a column in the **Recordset**. You can populate the **Fields** collection before opening the **Recordset** by calling the [Refresh](refresh-method-ado.md) method on the collection.</span></span>

> [!NOTE]
> <span data-ttu-id="811ae-109">[!NOTA] Para obtener una explicación más detallada sobre cómo se usan los objetos **Field**, vea el tema sobre el objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="811ae-109">See the **Field** object topic for a more detailed explanation of how to use **Field** objects.</span></span>

<span data-ttu-id="811ae-110">La colección **Fields** tiene un método [Append](append-method-ado.md) que, provisionalmente, crea y agrega un objeto **Field** a la colección, y un método **Update** que finaliza las incorporaciones o eliminaciones.</span><span class="sxs-lookup"><span data-stu-id="811ae-110">The **Fields** collection has an [Append](append-method-ado.md) method, which provisionally creates and adds a **Field** object to the collection, and an **Update** method, which finalizes any additions or deletions.</span></span>

<span data-ttu-id="811ae-p102">Los objetos **Record** tienen dos campos especiales que se pueden indizar con constantes [FieldEnum](fieldenum.md). Una constante obtiene acceso a un campo que contiene la secuencia predeterminada correspondiente al objeto **Record**, y la otra obtiene acceso a un campo que contiene la cadena de la dirección URL absoluta correspondiente al objeto **Record**.</span><span class="sxs-lookup"><span data-stu-id="811ae-p102">A **Record** object has two special fields that can be indexed with [FieldEnum](fieldenum.md) constants. One constant accesses a field containing the default stream for the **Record**, and the other accesses a field containing the absolute URL string for the **Record**.</span></span>

<span data-ttu-id="811ae-p103">Algunos proveedores (por ejemplo, [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) pueden rellenar la colección **Fields** con un subconjunto de campos disponibles correspondientes al objeto **Record** o **Recordset**. No se agregarán otros campos a la colección hasta que se haga referencia a ellos por su nombre o sean indizados por el código.</span><span class="sxs-lookup"><span data-stu-id="811ae-p103">Certain providers (for example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) may populate the **Fields** collection with a subset of available fields for the **Record** or **Recordset**. Other fields will not be added to the collection until they are first referenced by name or indexed by your code.</span></span>

<span data-ttu-id="811ae-p104">Si se intenta hacer referencia a un campo no existente por su nombre, se anexará un nuevo objeto **Field** a la colección **Fields** con un [Status](status-property-ado-field.md) de **adFieldPendingInsert**. Cuando se llame a [Update](update-method-ado.md), ADO creará un nuevo campo en el origen de datos si lo permite el proveedor.</span><span class="sxs-lookup"><span data-stu-id="811ae-p104">If you attempt to reference a nonexistent field by name, a new **Field** object will be appended to the **Fields** collection with a [Status](status-property-ado-field.md) of **adFieldPendingInsert**. When you call [Update](update-method-ado.md), ADO will create a new field in your data source if allowed by your provider.</span></span>

