---
title: Método Document.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 834fda60-1edf-38df-a9a5-d9d15e55e425
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196739(v=office.15)
ms:contentKeyID: 48546003
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052967
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d1e2e2200953580406dded7d5c014b533129b133
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293822"
---
# <a name="documentcreateproperty-method-dao"></a><span data-ttu-id="291ac-102">Método Document.CreateProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="291ac-102">Document.CreateProperty method (DAO)</span></span>

<span data-ttu-id="291ac-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="291ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="291ac-104">Crea un nuevo objeto **[Property](property-object-dao.md)** definido por el usuario (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="291ac-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="291ac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="291ac-105">Syntax</span></span>

<span data-ttu-id="291ac-106">*expresión* . CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="291ac-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="291ac-107">*expresión* Variable que representa un **objeto Document.**</span><span class="sxs-lookup"><span data-stu-id="291ac-107">*expression* A variable that represents a **Document** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="291ac-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="291ac-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="291ac-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="291ac-109">Name</span></span></p></th>
<th><p><span data-ttu-id="291ac-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="291ac-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="291ac-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="291ac-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="291ac-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="291ac-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="291ac-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="291ac-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="291ac-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="291ac-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="291ac-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="291ac-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="291ac-p101"><strong>String</strong> que identifica inequívocamente el nuevo objeto <strong>Property</strong>. Vea el tema relativo a la propiedad <strong>Name</strong> para obtener información detallada sobre los nombres de <strong>Property</strong> válidos.</span><span class="sxs-lookup"><span data-stu-id="291ac-p101">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="291ac-118"><em>Tipo</em></span><span class="sxs-lookup"><span data-stu-id="291ac-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="291ac-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="291ac-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="291ac-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="291ac-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="291ac-p102">Constante que define el tipo de datos del nuevo objeto <strong>Property</strong>. Vea el tema relativo a la propiedad <strong><a href="field-type-property-dao.md">Type</a></strong> para obtener información sobre los tipos de datos válidos.</span><span class="sxs-lookup"><span data-stu-id="291ac-p102">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="291ac-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="291ac-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="291ac-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="291ac-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="291ac-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="291ac-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="291ac-p103"><strong>Variant</strong> que contiene el valor inicial de la propiedad. Vea el tema relativo a la propiedad <strong><a href="field-value-property-dao.md">Value</a></strong> para obtener información detallada.</span><span class="sxs-lookup"><span data-stu-id="291ac-p103">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="291ac-128"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="291ac-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="291ac-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="291ac-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="291ac-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="291ac-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="291ac-131"><strong>Variant</strong> (subtipo <strong>Boolean</strong>) que indica si el objeto <strong>Property</strong> es un objeto DLL.</span><span class="sxs-lookup"><span data-stu-id="291ac-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="291ac-132">El valor predeterminado es <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="291ac-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="291ac-133">Si DDL es <strong>True,</strong>los usuarios no pueden cambiar ni eliminar este objeto <strong>Property</strong> a menos que tengan <strong>permiso dbSecWriteDef.</strong></span><span class="sxs-lookup"><span data-stu-id="291ac-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="291ac-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="291ac-134">Return value</span></span>

<span data-ttu-id="291ac-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="291ac-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="291ac-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="291ac-136">Remarks</span></span>

<span data-ttu-id="291ac-137">Sólo puede crear un objeto **Property** definido por el usuario en la colección **[Properties](properties-collection-dao.md)** de un objeto que sea persistente.</span><span class="sxs-lookup"><span data-stu-id="291ac-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="291ac-p105">Si omite uno o varios de los argumentos opcionales cuando utiliza **CreateProperty**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad correspondiente antes de agregar el nuevo objeto a una colección. Después de agregar el objeto, podrá modificar algunos de sus valores, pero no todos. Vea los temas relativos a las propiedades **Name**, **Type** y **Value** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="291ac-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="291ac-141">Si name hace referencia a un objeto que ya es miembro de la colección, se produce un error en tiempo de ejecución cuando se usa el **[método Append.](fields-append-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="291ac-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="291ac-p106">Para quitar un objeto **Property** definido por el usuario de la colección, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección **Properties**. No se pueden eliminar propiedades integradas.</span><span class="sxs-lookup"><span data-stu-id="291ac-p106">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection. You can't delete built-in properties.</span></span>


> [!NOTE]
> <span data-ttu-id="291ac-144">Si omite el argumento DDL, el valor predeterminado es False (que no es DDL).</span><span class="sxs-lookup"><span data-stu-id="291ac-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="291ac-145">Como no se expone ninguna propiedad DLL correspondiente, debe eliminar y volver a crear un objeto **Property** que desee cambiar de DDL a no DDL.</span><span class="sxs-lookup"><span data-stu-id="291ac-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


