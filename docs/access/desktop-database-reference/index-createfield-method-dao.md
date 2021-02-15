---
title: Método Index.CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: fc82b785-8768-b144-a2a4-c1f1798865a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837208(v=office.15)
ms:contentKeyID: 48548892
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aedda14273446ff6823776e535eb7995aa127fa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291834"
---
# <a name="indexcreatefield-method-dao"></a><span data-ttu-id="19de1-102">Método Index.CreateField (DAO)</span><span class="sxs-lookup"><span data-stu-id="19de1-102">Index.CreateField method (DAO)</span></span>

<span data-ttu-id="19de1-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19de1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19de1-104">Crea un nuevo objeto **[Field](field-object-dao.md)** (solo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="19de1-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="19de1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19de1-105">Syntax</span></span>

<span data-ttu-id="19de1-106">*expresión* . CreateField(***Name***, ***Type***, ***Size***)</span><span class="sxs-lookup"><span data-stu-id="19de1-106">*expression* .CreateField(***Name***, ***Type***, ***Size***)</span></span>

<span data-ttu-id="19de1-107">*expresión* Variable que representa un **objeto Index.**</span><span class="sxs-lookup"><span data-stu-id="19de1-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="19de1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19de1-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19de1-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="19de1-109">Name</span></span></p></th>
<th><p><span data-ttu-id="19de1-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="19de1-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="19de1-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="19de1-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="19de1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="19de1-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19de1-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="19de1-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="19de1-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="19de1-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="19de1-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="19de1-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="19de1-p101">Una cadena que asigna nombres únicos al nuevo objeto <strong>Field</strong>. Consulte la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong> para obtener más detalles sobre los nombres de <strong>Field</strong> válidos.</span><span class="sxs-lookup"><span data-stu-id="19de1-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19de1-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="19de1-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="19de1-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="19de1-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="19de1-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="19de1-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="19de1-121">Argumento no admitido en este objeto.</span><span class="sxs-lookup"><span data-stu-id="19de1-121">Argument not supported for this object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19de1-122"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="19de1-122"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="19de1-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="19de1-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="19de1-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="19de1-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="19de1-125">Argumento no admitido en este objeto.</span><span class="sxs-lookup"><span data-stu-id="19de1-125">Argument not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="19de1-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19de1-126">Return value</span></span>

<span data-ttu-id="19de1-127">Field</span><span class="sxs-lookup"><span data-stu-id="19de1-127">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="19de1-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19de1-128">Remarks</span></span>

<span data-ttu-id="19de1-p102">Puede usar el método **CreateField** para crear un nuevo campo, así como para especificar el nombre, el tipo de datos y el tamaño del campo. Si omite una o más partes opcionales al usar **CreateField**, puede usar una instrucción de asignación adecuada para configurar o restablecer la propiedad correspondiente antes de anexar el nuevo objeto a la colección. Tras anexar el nuevo objeto, puede modificar algunas, pero no todas, las configuraciones de la propiedad. Consulte los temas de propiedades individuales para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="19de1-p102">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="19de1-133">Los argumentos de tipo y tamaño sólo se aplican a **objetos Field** en un **objeto TableDef** .</span><span class="sxs-lookup"><span data-stu-id="19de1-133">The type and size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="19de1-134">Estos argumentos se omiten cuando se asocia un campo **Field** con un objeto **Index** o **Relation**.</span><span class="sxs-lookup"><span data-stu-id="19de1-134">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="19de1-135">Si el nombre hace referencia a un objeto que ya es miembro de la colección, se produce un error en tiempo de ejecución cuando se usa el **[método Append.](fields-append-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="19de1-135">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="19de1-p104">Para eliminar un objeto **Field** de una colección **Fields**, use el método **[Delete](fields-delete-method-dao.md)** de una colección. No puede eliminar un objeto **Field** de una colección **Fields** de un objeto **TableDef** después de crear un índice que hace referencia al campo.</span><span class="sxs-lookup"><span data-stu-id="19de1-p104">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

