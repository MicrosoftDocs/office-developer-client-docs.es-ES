---
title: Propiedad Field2.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8e7bf23dcde9b522e5a9ed74c4dc969c5312f5a3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931235"
---
# <a name="field2validationtext-property-dao"></a><span data-ttu-id="ec8cd-102">Propiedad Field2.ValidationText (DAO)</span><span class="sxs-lookup"><span data-stu-id="ec8cd-102">Field2.ValidationText property (DAO)</span></span>


<span data-ttu-id="ec8cd-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec8cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec8cd-p101">Establece o devuelve un valor que especifica el texto del mensaje que su aplicación muestra si el valor de un objeto **Field2** no satisface la regla de validación que especifica el valor de la propiedad **ValidationRule** (sólo para áreas de trabajo de Microsoft Access). **String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ec8cd-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field2** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec8cd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec8cd-106">Syntax</span></span>

<span data-ttu-id="ec8cd-107">*expresión* . ValidationText</span><span class="sxs-lookup"><span data-stu-id="ec8cd-107">*expression* .ValidationText</span></span>

<span data-ttu-id="ec8cd-108">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="ec8cd-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec8cd-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec8cd-109">Remarks</span></span>

<span data-ttu-id="ec8cd-p102">La configuración o el valor devuelto es **String** que especifica el texto que aparece si un usuario intenta especificar un valor no válido para un campo. Para un objeto que todavía no está anexado a una colección, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ec8cd-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="ec8cd-112">Para un objeto **Field2**, la utilización de la propiedad **ValidationText** depende del objeto que contiene la colección **[Fields](fields-collection-dao.md)** a la que está anexado el objeto **Field2**, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ec8cd-112">For a **Field2** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field2** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec8cd-113">Objeto anexado a</span><span class="sxs-lookup"><span data-stu-id="ec8cd-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="ec8cd-114">Uso</span><span class="sxs-lookup"><span data-stu-id="ec8cd-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec8cd-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="ec8cd-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="ec8cd-116">No admitido</span><span class="sxs-lookup"><span data-stu-id="ec8cd-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec8cd-117"><strong>Objeto QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="ec8cd-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="ec8cd-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec8cd-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec8cd-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="ec8cd-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="ec8cd-120">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec8cd-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec8cd-121"><strong>Relación</strong></span><span class="sxs-lookup"><span data-stu-id="ec8cd-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="ec8cd-122">No admitido</span><span class="sxs-lookup"><span data-stu-id="ec8cd-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec8cd-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="ec8cd-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="ec8cd-124">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="ec8cd-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

