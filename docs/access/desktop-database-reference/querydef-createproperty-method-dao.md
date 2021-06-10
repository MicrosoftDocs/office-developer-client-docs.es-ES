---
title: Método QueryDef.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: e107b7d0-5556-7b87-f131-95f518893e4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835663(v=office.15)
ms:contentKeyID: 48548250
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f33198ac13b6695bfa592e2015aaed84d57f3b2d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303034"
---
# <a name="querydefcreateproperty-method-dao"></a><span data-ttu-id="2d7e5-102">Método QueryDef.CreateProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="2d7e5-102">QueryDef.CreateProperty method (DAO)</span></span>

<span data-ttu-id="2d7e5-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d7e5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d7e5-104">Crea un nuevo objeto **[Property](property-object-dao.md)** definido por el usuario (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2d7e5-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d7e5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d7e5-105">Syntax</span></span>

<span data-ttu-id="2d7e5-106">*expresión* . CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="2d7e5-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="2d7e5-107">*expression* Variable que representa un objeto **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="2d7e5-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d7e5-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d7e5-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d7e5-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="2d7e5-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2d7e5-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="2d7e5-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="2d7e5-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2d7e5-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="2d7e5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d7e5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d7e5-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="2d7e5-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="2d7e5-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="2d7e5-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="2d7e5-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2d7e5-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2d7e5-p101"><strong>String</strong> que identifica inequívocamente el nuevo objeto <strong>Property</strong>. Vea el tema relativo a la propiedad <strong>Name</strong> para obtener información detallada sobre los nombres de <strong>Property</strong> válidos.</span><span class="sxs-lookup"><span data-stu-id="2d7e5-p101">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d7e5-118"><em>Tipo</em></span><span class="sxs-lookup"><span data-stu-id="2d7e5-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="2d7e5-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="2d7e5-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="2d7e5-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2d7e5-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2d7e5-p102">Constante que define el tipo de datos del nuevo objeto <strong>Property</strong>. Vea el tema relativo a la propiedad <strong><a href="field-type-property-dao.md">Type</a></strong> para obtener información sobre los tipos de datos válidos.</span><span class="sxs-lookup"><span data-stu-id="2d7e5-p102">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d7e5-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="2d7e5-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="2d7e5-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="2d7e5-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="2d7e5-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2d7e5-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2d7e5-p103"><strong>Variant</strong> que contiene el valor inicial de la propiedad. Vea el tema relativo a la propiedad <strong><a href="field-value-property-dao.md">Value</a></strong> para obtener información detallada.</span><span class="sxs-lookup"><span data-stu-id="2d7e5-p103">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d7e5-128"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="2d7e5-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="2d7e5-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="2d7e5-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="2d7e5-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2d7e5-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2d7e5-131"><strong>Variant</strong> (subtipo <strong>Boolean</strong>) que indica si el objeto <strong>Property</strong> es un objeto DLL.</span><span class="sxs-lookup"><span data-stu-id="2d7e5-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="2d7e5-132">El valor predeterminado es <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d7e5-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="2d7e5-133">Si DDL es <strong>True,</strong>los usuarios no pueden cambiar ni eliminar este objeto <strong>Property</strong> a menos que tengan <strong>permiso dbSecWriteDef.</strong></span><span class="sxs-lookup"><span data-stu-id="2d7e5-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="2d7e5-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d7e5-134">Return value</span></span>

<span data-ttu-id="2d7e5-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2d7e5-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="2d7e5-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2d7e5-136">Remarks</span></span>

<span data-ttu-id="2d7e5-137">Sólo puede crear un objeto **Property** definido por el usuario en la colección **[Properties](properties-collection-dao.md)** de un objeto que sea persistente.</span><span class="sxs-lookup"><span data-stu-id="2d7e5-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="2d7e5-p105">Si omite uno o varios de los argumentos opcionales cuando utiliza **CreateProperty**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad correspondiente antes de agregar el nuevo objeto a una colección. Después de agregar el objeto, podrá modificar algunos de sus valores, pero no todos. Vea los temas relativos a las propiedades **Name**, **Type** y **Value** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2d7e5-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="2d7e5-141">Si name hace referencia a un objeto que ya es miembro de la colección, se produce un error en tiempo de ejecución cuando se usa el **[método Append.](fields-append-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="2d7e5-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="2d7e5-p106">Para quitar un objeto **Property** definido por el usuario de la colección, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección **[Properties](properties-collection-dao.md)**. No se pueden eliminar propiedades integradas.</span><span class="sxs-lookup"><span data-stu-id="2d7e5-p106">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **[Properties](properties-collection-dao.md)** collection. You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="2d7e5-144">Si omite el argumento DDL, el valor predeterminado es False (que no es DDL).</span><span class="sxs-lookup"><span data-stu-id="2d7e5-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="2d7e5-145">Dado que no se expone ninguna propiedad DDL correspondiente, debe eliminar y volver a crear un objeto **Property** que desee cambiar de DDL a que no sea DDL.</span><span class="sxs-lookup"><span data-stu-id="2d7e5-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object that you want to change from DDL to non-DDL.</span></span>


