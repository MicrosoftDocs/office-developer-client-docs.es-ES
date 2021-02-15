---
title: Método TableDef.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 8a92cc64-414e-f33c-1c3e-d1b62c1688c2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197102(v=office.15)
ms:contentKeyID: 48546197
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3018bf8cc9a62cb866b35992e25ecb1f8f41514f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308424"
---
# <a name="tabledefcreateproperty-method-dao"></a><span data-ttu-id="9f8ea-102">Método TableDef.CreateProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="9f8ea-102">TableDef.CreateProperty method (DAO)</span></span>

<span data-ttu-id="9f8ea-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f8ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f8ea-104">Crea un nuevo objeto **[Property](property-object-dao.md)** definido por el usuario (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9f8ea-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f8ea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f8ea-105">Syntax</span></span>

<span data-ttu-id="9f8ea-106">*expresión* . CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="9f8ea-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="9f8ea-107">*expression* Variable que representa un objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f8ea-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="9f8ea-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9f8ea-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="9f8ea-109">Name</span></span></p></th>
<th><p><span data-ttu-id="9f8ea-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="9f8ea-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="9f8ea-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9f8ea-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="9f8ea-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f8ea-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f8ea-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="9f8ea-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="9f8ea-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="9f8ea-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="9f8ea-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9f8ea-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9f8ea-116"><strong>String</strong> que identifica inequívocamente el nuevo objeto <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-116">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="9f8ea-117">Vea el tema relativo a la propiedad <strong>Name</strong> para obtener información detallada sobre los nombres de <strong>Property</strong> válidos.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-117">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f8ea-118"><em>Tipo</em></span><span class="sxs-lookup"><span data-stu-id="9f8ea-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="9f8ea-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="9f8ea-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="9f8ea-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9f8ea-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9f8ea-121">Constante que define el tipo de datos del nuevo objeto <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-121">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="9f8ea-122">Consulte la propiedad <strong><a href="field-type-property-dao.md">Type</a></strong> para obtener los tipos de datos válidos.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-122">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f8ea-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="9f8ea-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="9f8ea-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="9f8ea-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="9f8ea-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9f8ea-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9f8ea-126"><strong>Variant</strong> que contiene el valor inicial de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-126">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="9f8ea-127">Vea la <strong><a href="field-value-property-dao.md">propiedad Value</a></strong> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-127">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f8ea-128"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="9f8ea-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="9f8ea-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="9f8ea-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="9f8ea-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9f8ea-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9f8ea-131"><strong>Variant</strong> (subtipo <strong>Boolean</strong>) que indica si el objeto <strong>Property</strong> es un objeto DLL.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="9f8ea-132">El valor predeterminado es <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="9f8ea-133">Si DDL es <strong>True</strong>, los usuarios no pueden cambiar ni eliminar este objeto <strong>Property</strong> a menos que tengan el permiso <strong>dbSecWriteDef.</strong></span><span class="sxs-lookup"><span data-stu-id="9f8ea-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="9f8ea-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f8ea-134">Return value</span></span>

<span data-ttu-id="9f8ea-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f8ea-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="9f8ea-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f8ea-136">Remarks</span></span>

<span data-ttu-id="9f8ea-137">Sólo puede crear un objeto **Property** definido por el usuario en la colección **[Properties](properties-collection-dao.md)** de un objeto que sea persistente.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="9f8ea-p105">Si omite uno o varios de los argumentos opcionales cuando utiliza **CreateProperty**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad correspondiente antes de agregar el nuevo objeto a una colección. Después de agregar el objeto, podrá modificar algunos de sus valores, pero no todos. Vea los temas relativos a las propiedades **Name**, **Type** y **Value** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="9f8ea-141">Si el nombre hace referencia a un objeto que ya es miembro de la colección, se produce un error en tiempo de ejecución cuando se usa el **[método Append.](fields-append-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="9f8ea-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="9f8ea-142">Para quitar un objeto **Property** definido por el usuario de la colección, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección **[Properties](properties-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-142">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **[Properties](properties-collection-dao.md)** collection.</span></span> <span data-ttu-id="9f8ea-143">No se pueden eliminar propiedades integradas.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-143">You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="9f8ea-144">Si omite el argumento DDL, el valor predeterminado es False (no DDL).</span><span class="sxs-lookup"><span data-stu-id="9f8ea-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="9f8ea-145">Dado que no se expone ninguna propiedad DDL correspondiente, debe eliminar y volver a crear un objeto **Property** que desee cambiar de DDL a no DDL.</span><span class="sxs-lookup"><span data-stu-id="9f8ea-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object that you want to change from DDL to non-DDL.</span></span>


