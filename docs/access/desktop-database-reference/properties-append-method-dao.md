---
title: Método Properties. Append (DAO)
TOCTitle: Append Method
ms:assetid: 47f1e24f-975c-3fdc-5c3c-8c91f2920c81
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193232(v=office.15)
ms:contentKeyID: 48544609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 528809495ebefd15a8895b15a9d51f84e6892980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301312"
---
# <a name="propertiesappend-method-dao"></a><span data-ttu-id="1596a-102">Método Properties. Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="1596a-102">Properties.Append method (DAO)</span></span>

<span data-ttu-id="1596a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1596a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1596a-104">Agrega un nuevo objeto **Property** a la colección **Properties**.</span><span class="sxs-lookup"><span data-stu-id="1596a-104">Adds a new **Property** to the **Properties** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1596a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1596a-105">Syntax</span></span>

<span data-ttu-id="1596a-106">*expresión* . Append (***objeto***)</span><span class="sxs-lookup"><span data-stu-id="1596a-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="1596a-107">*expresión* Variable que representa un objeto **Properties** .</span><span class="sxs-lookup"><span data-stu-id="1596a-107">*expression* A variable that represents a **Properties** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1596a-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="1596a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1596a-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="1596a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1596a-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="1596a-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="1596a-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1596a-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="1596a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1596a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1596a-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="1596a-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="1596a-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1596a-114">Required</span></span></p></td>
<td><p><span data-ttu-id="1596a-115"><strong>Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="1596a-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="1596a-116">Variable de objeto que representa el campo que se va a anexar a la colección.</span><span class="sxs-lookup"><span data-stu-id="1596a-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1596a-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1596a-117">Remarks</span></span>

<span data-ttu-id="1596a-118">El objeto anexado se convierte en un objeto persistente, almacenado en un disco, hasta que lo elimine mediante el método **Delete**.</span><span class="sxs-lookup"><span data-stu-id="1596a-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="1596a-119">La agregación de un nuevo objeto se produce de inmediato pero debe utilizar el método **Refresh** en cualquier otra colección que pueda verse afectada por los cambios en la estructura de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1596a-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="1596a-120">Si el objeto que está anexando está incompleto (como cuando no ha anexado ningún objeto **Field** a una colección **Fields** de un objeto **Index** antes de anexarlo a una colección **Indexes**) o si las propiedades establecidas en uno o varios objetos subordinados son incorrectas, el uso del método **Append** provoca un error.</span><span class="sxs-lookup"><span data-stu-id="1596a-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="1596a-121">Por ejemplo, si no ha especificado un tipo de campo e intenta anexar el objeto **Field** a la colección **Fields** en un objeto **TableDef** , al usar el método **Append** se desencadena un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="1596a-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

