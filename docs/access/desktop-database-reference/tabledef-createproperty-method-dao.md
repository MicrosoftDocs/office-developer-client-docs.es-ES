---
title: TableDef.CreateProperty (método) (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 8a92cc64-414e-f33c-1c3e-d1b62c1688c2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197102(v=office.15)
ms:contentKeyID: 48546197
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 85299765a598b969e4d9229c85e9f2e9b165d64e
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996891"
---
# <a name="tabledefcreateproperty-method-dao"></a><span data-ttu-id="71316-102">TableDef.CreateProperty (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="71316-102">TableDef.CreateProperty method (DAO)</span></span>

<span data-ttu-id="71316-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="71316-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71316-104">Crea un nuevo objeto **[Property](property-object-dao.md)** definido por el usuario (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="71316-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="71316-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71316-105">Syntax</span></span>

<span data-ttu-id="71316-106">*expresión* . CreateProperty (***nombre***, ***tipo***, ***valor***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="71316-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="71316-107">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="71316-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="71316-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71316-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71316-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="71316-109">Name</span></span></p></th>
<th><p><span data-ttu-id="71316-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="71316-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="71316-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="71316-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="71316-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="71316-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71316-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="71316-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="71316-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="71316-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="71316-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="71316-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="71316-p101"><strong>String</strong> que identifica inequívocamente el nuevo objeto <strong>Property</strong>. Vea el tema relativo a la propiedad <strong>Name</strong> para obtener información detallada sobre los nombres de <strong>Property</strong> válidos.</span><span class="sxs-lookup"><span data-stu-id="71316-p101">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71316-118"><em>Tipo</em></span><span class="sxs-lookup"><span data-stu-id="71316-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="71316-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="71316-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="71316-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="71316-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="71316-p102">Constante que define el tipo de datos del nuevo objeto <strong>Property</strong>. Vea el tema relativo a la propiedad <strong><a href="field-type-property-dao.md">Type</a></strong> para obtener información sobre los tipos de datos válidos.</span><span class="sxs-lookup"><span data-stu-id="71316-p102">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71316-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="71316-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="71316-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="71316-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="71316-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="71316-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="71316-p103"><strong>Variant</strong> que contiene el valor inicial de la propiedad. Vea el tema relativo a la propiedad <strong><a href="field-value-property-dao.md">Value</a></strong> para obtener información detallada.</span><span class="sxs-lookup"><span data-stu-id="71316-p103">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71316-128"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="71316-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="71316-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="71316-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="71316-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="71316-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="71316-131"><strong>Variant</strong> (subtipo<strong>Boolean</strong> ) que indica si la <strong>propiedad</strong> es un objeto DDL.</span><span class="sxs-lookup"><span data-stu-id="71316-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="71316-132">El valor predeterminado es <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="71316-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="71316-133">Si DDL es <strong>True</strong>, los usuarios no pueden cambiar o eliminar este objeto <strong>Property</strong> a menos que tengan un permiso <strong>dbSecWriteDef</strong> .</span><span class="sxs-lookup"><span data-stu-id="71316-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="71316-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71316-134">Return value</span></span>

<span data-ttu-id="71316-135">Property</span><span class="sxs-lookup"><span data-stu-id="71316-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="71316-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71316-136">Remarks</span></span>

<span data-ttu-id="71316-137">Solo puede crear un objeto **Property** definido por el usuario en la colección **[Properties](properties-collection-dao.md)** de un objeto que sea persistente.</span><span class="sxs-lookup"><span data-stu-id="71316-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="71316-p105">Si omite uno o varios de los argumentos opcionales cuando utiliza **CreateProperty**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad correspondiente antes de agregar el nuevo objeto a una colección. Después de agregar el objeto, podrá modificar algunos de sus valores, pero no todos. Vea los temas relativos a las propiedades **Name**, **Type** y **Value** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="71316-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="71316-141">Si name hace referencia a un objeto que ya es un miembro de la colección, se produce un error en tiempo de ejecución cuando se utiliza el método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="71316-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="71316-p106">Para quitar un objeto **Property** definido por el usuario de la colección, use el método **[Delete](fields-delete-method-dao.md)** en la colección **[Properties](properties-collection-dao.md)**. No se pueden eliminar propiedades integradas.</span><span class="sxs-lookup"><span data-stu-id="71316-p106">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **[Properties](properties-collection-dao.md)** collection. You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="71316-144">Si se omite el argumento DDL, el valor predeterminado es False (no DDL).</span><span class="sxs-lookup"><span data-stu-id="71316-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="71316-145">Debido a que no se expone ninguna propiedad DDL correspondiente, debe eliminar y volver a crear un objeto **Property** que desea cambiar de DDL a no DDL.</span><span class="sxs-lookup"><span data-stu-id="71316-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object that you want to change from DDL to non-DDL.</span></span>


