---
title: Principal (propiedad, ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb1606a745cb8572f54b253bdbbbbbb461cfc74a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484566"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="62034-102">Principal (propiedad, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="62034-102">Parent Property (ADO MD)</span></span>


<span data-ttu-id="62034-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="62034-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="62034-104">Indica cuál es el elemento principal del elemento activo en una jerarquía.</span><span class="sxs-lookup"><span data-stu-id="62034-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="62034-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="62034-105">Return Values</span></span>

<span data-ttu-id="62034-106">Devuelve un objeto [Member](member-object-ado-md.md) y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="62034-106">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="62034-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62034-107">Remarks</span></span>

<span data-ttu-id="62034-p101">Un elemento que está en el nivel superior de una jerarquía (la raíz) no tiene elemento principal. Esta propiedad sólo es compatible con objetos **Member** pertenecientes a un objeto [Level](level-object-ado-md.md). Si se hace referencia a esta propiedad desde objetos **Member** pertenecientes a un objeto [Position](position-object-ado-md.md), se produce un error.</span><span class="sxs-lookup"><span data-stu-id="62034-p101">A member that is at the top level of a hierarchy (the root) has no parent. This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

