---
title: Método QueryDefs. Append (DAO)
TOCTitle: Append Method
ms:assetid: 9b62a26b-3b7c-6d26-7707-177b00a23178
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198041(v=office.15)
ms:contentKeyID: 48546570
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4183a7b438d3f55d73eb63adb2d124da7eeecc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300941"
---
# <a name="querydefsappend-method-dao"></a><span data-ttu-id="1c747-102">Método QueryDefs. Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="1c747-102">QueryDefs.Append method (DAO)</span></span>

<span data-ttu-id="1c747-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c747-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c747-104">Agrega un nuevo objeto **QueryDef** a la colección **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="1c747-104">Adds a new **QueryDef** to the **QueryDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c747-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c747-105">Syntax</span></span>

<span data-ttu-id="1c747-106">*expresión* . Append (***objeto***)</span><span class="sxs-lookup"><span data-stu-id="1c747-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="1c747-107">*expresión* Variable que representa un objeto **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="1c747-107">*expression* A variable that represents a **QueryDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1c747-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="1c747-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c747-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="1c747-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1c747-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="1c747-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="1c747-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1c747-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="1c747-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c747-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c747-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="1c747-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="1c747-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1c747-114">Required</span></span></p></td>
<td><p><span data-ttu-id="1c747-115"><strong>Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="1c747-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="1c747-116">Variable de objeto que representa el campo que se va a anexar a la colección.</span><span class="sxs-lookup"><span data-stu-id="1c747-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1c747-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c747-117">Remarks</span></span>

<span data-ttu-id="1c747-118">El objeto anexado se convierte en un objeto persistente, almacenado en un disco, hasta que lo elimine mediante el método **Delete**.</span><span class="sxs-lookup"><span data-stu-id="1c747-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="1c747-119">La agregación de un nuevo objeto se produce de inmediato pero debe utilizar el método **Refresh** en cualquier otra colección que pueda verse afectada por los cambios en la estructura de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1c747-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="1c747-120">Si el objeto que está anexando está incompleto (como cuando no ha anexado ningún objeto **Field** a una colección **Fields** de un objeto **Index** antes de anexarlo a una colección **Indexes**) o si las propiedades establecidas en uno o varios objetos subordinados son incorrectas, el uso del método **Append** provoca un error.</span><span class="sxs-lookup"><span data-stu-id="1c747-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="1c747-121">Por ejemplo, si no ha especificado un tipo de campo e intenta anexar el objeto **Field** a la colección **Fields** en un objeto **TableDef** , al usar el método **Append** se desencadena un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="1c747-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

