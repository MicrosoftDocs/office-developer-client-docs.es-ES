---
title: Principal (propiedad, ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1da5b763d85fc9975a42e357860d87ce64cf618
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930591"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="7a41c-102">Principal (propiedad, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="7a41c-102">Parent property (ADO MD)</span></span>


<span data-ttu-id="7a41c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a41c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7a41c-104">Indica cuál es el elemento principal del elemento activo en una jerarquía.</span><span class="sxs-lookup"><span data-stu-id="7a41c-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="7a41c-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="7a41c-105">Return values</span></span>

<span data-ttu-id="7a41c-106">Devuelve un objeto [Member](member-object-ado-md.md) y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="7a41c-106">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a41c-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7a41c-107">Remarks</span></span>

<span data-ttu-id="7a41c-p101">Un elemento que está en el nivel superior de una jerarquía (la raíz) no tiene elemento principal. Esta propiedad sólo es compatible con objetos **Member** pertenecientes a un objeto [Level](level-object-ado-md.md). Si se hace referencia a esta propiedad desde objetos **Member** pertenecientes a un objeto [Position](position-object-ado-md.md), se produce un error.</span><span class="sxs-lookup"><span data-stu-id="7a41c-p101">A member that is at the top level of a hierarchy (the root) has no parent. This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

