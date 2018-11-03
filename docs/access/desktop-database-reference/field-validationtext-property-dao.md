---
title: Propiedad Field.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3244c4e41761095378e3be3ad928effc6444f842
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930409"
---
# <a name="fieldvalidationtext-property-dao"></a><span data-ttu-id="b824b-102">Propiedad Field.ValidationText (DAO)</span><span class="sxs-lookup"><span data-stu-id="b824b-102">Field.ValidationText property (DAO)</span></span>


<span data-ttu-id="b824b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b824b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b824b-p101">Establece o devuelve un valor que especifica el texto del mensaje que la aplicación muestra si el valor de un objeto **Field** no cumple la regla de validación especificada por el valor de la propiedad **ValidationRule** (únicamente áreas de trabajo de Microsoft Access). **String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b824b-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b824b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b824b-106">Syntax</span></span>

<span data-ttu-id="b824b-107">*expresión* . ValidationText</span><span class="sxs-lookup"><span data-stu-id="b824b-107">*expression* .ValidationText</span></span>

<span data-ttu-id="b824b-108">*expresión* Variable que representa un objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="b824b-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b824b-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b824b-109">Remarks</span></span>

<span data-ttu-id="b824b-p102">La configuración o el valor devuelto es un objeto **String** que especifica el texto que se muestra si un usuario intenta escribir un valor no válido en un campo. Para un objeto no anexado todavía a una colección, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b824b-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="b824b-112">Para un objeto **Field**, el uso de la propiedad **ValidationText** dependerá del objeto que contenga la colección **[Fields](fields-collection-dao.md)** a la que se anexa el objeto **Field**, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b824b-112">For a **Field** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b824b-113">Objeto anexado a</span><span class="sxs-lookup"><span data-stu-id="b824b-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="b824b-114">Uso</span><span class="sxs-lookup"><span data-stu-id="b824b-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b824b-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="b824b-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="b824b-116">No admitido</span><span class="sxs-lookup"><span data-stu-id="b824b-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b824b-117"><strong>Objeto QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="b824b-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="b824b-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="b824b-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b824b-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="b824b-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="b824b-120">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="b824b-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b824b-121"><strong>Relación</strong></span><span class="sxs-lookup"><span data-stu-id="b824b-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="b824b-122">No admitido</span><span class="sxs-lookup"><span data-stu-id="b824b-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b824b-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="b824b-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="b824b-124">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="b824b-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

