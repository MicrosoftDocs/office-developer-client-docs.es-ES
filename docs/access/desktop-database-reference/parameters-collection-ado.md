---
title: Colección Parameters (ADO)
TOCTitle: Parameters collection (ADO)
ms:assetid: 554387c3-3572-5391-3b24-c7d3443844cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249283(v=office.15)
ms:contentKeyID: 48544923
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: feb24e0f498e02bae01ef689a2ad62e487e314bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287947"
---
# <a name="parameters-collection-ado"></a><span data-ttu-id="09ad6-102">Colección Parameters (ADO)</span><span class="sxs-lookup"><span data-stu-id="09ad6-102">Parameters collection (ADO)</span></span>


<span data-ttu-id="09ad6-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="09ad6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09ad6-104">Contiene todos los objetos [Parameter](parameter-object-ado.md) de un objeto [Command](command-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="09ad6-104">Contains all the [Parameter](parameter-object-ado.md) objects of a [Command](command-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="09ad6-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09ad6-105">Remarks</span></span>

<span data-ttu-id="09ad6-106">Los objetos **Command** tienen una colección **Parameters** formada por objetos **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="09ad6-106">A **Command** object has a **Parameters** collection made up of **Parameter** objects.</span></span>

<span data-ttu-id="09ad6-p101">Si se usa el método [Refresh](refresh-method-ado.md) en la colección **Parameters** de un objeto **Command**, se recupera la información de parámetros del proveedor para el procedimiento almacenado o la consulta parametrizada especificados en el objeto **Command**. Algunos proveedores no admiten llamadas a procedimientos almacenados ni consultas parametrizadas. La llamada al método **Refresh** en la colección **Parameters** cuando se usa un proveedor de este tipo devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="09ad6-p101">Using the [Refresh](refresh-method-ado.md) method on a **Command** object's **Parameters** collection retrieves provider parameter information for the stored procedure or parameterized query specified in the **Command** object. Some providers do not support stored procedure calls or parameterized queries; calling the **Refresh** method on the **Parameters** collection when using such a provider will return an error.</span></span>

<span data-ttu-id="09ad6-109">Si no ha definido sus propios objetos **Parameter** y obtiene acceso a la colección **Parameters** antes de llamar al método **Refresh**, ADO realizará automáticamente la llamada al método y el relleno de la colección.</span><span class="sxs-lookup"><span data-stu-id="09ad6-109">If you have not defined your own **Parameter** objects and you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>

<span data-ttu-id="09ad6-p102">Puede reducir al mínimo las llamadas al proveedor para mejorar el rendimiento si sabe las propiedades de los parámetros asociados al procedimiento almacenado o a la consulta parametrizada que desea invocar. Utilice el método [CreateParameter](createparameter-method-ado.md) para crear objetos **Parameter** con los valores de propiedad adecuados y utilice el método [Append](append-method-ado.md) para agregarlos a la colección **Parameters**. Esto le permite establecer y devolver los valores de parámetro sin tener que llamar al proveedor para obtener la información de los parámetros. Si escribe a un proveedor que no proporciona información de parámetros, debe rellenar manualmente la colección **Parameters** utilizando este método para poder usar parámetros. Utilice el método [Delete](delete-method-ado-parameters-collection.md) para quitar objetos **Parameter** de la colección **Parameters** si es necesario.</span><span class="sxs-lookup"><span data-stu-id="09ad6-p102">You can minimize calls to the provider to improve performance if you know the properties of the parameters associated with the stored procedure or parameterized query you wish to call. Use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the **Parameters** collection. This lets you set and return parameter values without having to call the provider for the parameter information. If you are writing to a provider that does not supply parameter information, you must manually populate the **Parameters** collection using this method to be able to use parameters at all. Use the [Delete](delete-method-ado-parameters-collection.md) method to remove **Parameter** objects from the **Parameters** collection if necessary.</span></span>

<span data-ttu-id="09ad6-115">Los objetos de la colección **Parameters** de un objeto **Recordset** quedan fuera del ámbito (y, por lo tanto, no están disponibles) cuando el objeto **Recordset** está cerrado.</span><span class="sxs-lookup"><span data-stu-id="09ad6-115">The objects in the **Parameters** collection of a **Recordset** go out of scope (therefore becoming unavailable) when the **Recordset** is closed.</span></span>

