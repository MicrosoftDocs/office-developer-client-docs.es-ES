---
title: Método Relations.Append (DAO)
TOCTitle: Append Method
ms:assetid: dafcc7b8-b30d-2ba2-631d-eca0f882fc2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835334(v=office.15)
ms:contentKeyID: 48548094
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052904
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b8374832ad6cd6bac30fa9d129e54fb6ab4c8fd4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306989"
---
# <a name="relationsappend-method-dao"></a><span data-ttu-id="7a38b-102">Método Relations.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="7a38b-102">Relations.Append method (DAO)</span></span>

<span data-ttu-id="7a38b-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a38b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7a38b-104">Agrega un nuevo objeto **Relation** a la colección **Relations**.</span><span class="sxs-lookup"><span data-stu-id="7a38b-104">Adds a new **Relation** to the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a38b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a38b-105">Syntax</span></span>

<span data-ttu-id="7a38b-106">*expression* .Append(***Object***)</span><span class="sxs-lookup"><span data-stu-id="7a38b-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="7a38b-107">*expresión* Variable que representa un objeto **Relations** .</span><span class="sxs-lookup"><span data-stu-id="7a38b-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a38b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a38b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a38b-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="7a38b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7a38b-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="7a38b-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7a38b-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7a38b-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="7a38b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a38b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a38b-113"><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="7a38b-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="7a38b-114">Necesario</span><span class="sxs-lookup"><span data-stu-id="7a38b-114">Required</span></span></p></td>
<td><p><span data-ttu-id="7a38b-115"><strong>Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="7a38b-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="7a38b-116">Variable de objeto que representa el campo que se va a anexar a la colección.</span><span class="sxs-lookup"><span data-stu-id="7a38b-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7a38b-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7a38b-117">Remarks</span></span>

<span data-ttu-id="7a38b-118">El objeto anexado se convierte en un objeto persistente, almacenado en un disco, hasta que lo elimine mediante el método **Delete**.</span><span class="sxs-lookup"><span data-stu-id="7a38b-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="7a38b-119">La agregación de un nuevo objeto se produce de inmediato pero debe utilizar el método **Refresh** en cualquier otra colección que pueda verse afectada por los cambios en la estructura de base de datos.</span><span class="sxs-lookup"><span data-stu-id="7a38b-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="7a38b-120">Si el objeto que está anexando está incompleto (como cuando no ha anexado ningún objeto **Field** a una colección **Fields** de un objeto **Index** antes de anexarlo a una colección **Indexes**) o si las propiedades establecidas en uno o varios objetos subordinados son incorrectas, el uso del método **Append** provoca un error.</span><span class="sxs-lookup"><span data-stu-id="7a38b-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="7a38b-121">Por ejemplo, si no ha especificado un campo e intenta anexar el objeto **Field** a la colección **Fields** en un objeto **TableDef**, el uso del método **Append** desencadena un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7a38b-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

