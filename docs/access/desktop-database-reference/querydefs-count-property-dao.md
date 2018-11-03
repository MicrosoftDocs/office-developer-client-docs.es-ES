---
title: Propiedad QueryDefs.Count (DAO)
TOCTitle: Count Property
ms:assetid: 8caa01c5-692f-95e4-4b11-6e6c591f5872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197340(v=office.15)
ms:contentKeyID: 48546240
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5efc7479f69d379f406a9a7cda5d4c522df6325
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930899"
---
# <a name="querydefscount-property-dao"></a><span data-ttu-id="0616f-102">Propiedad QueryDefs.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="0616f-102">QueryDefs.Count property (DAO)</span></span>


<span data-ttu-id="0616f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0616f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0616f-p101">Devuelve el número de objetos de la colección especificada. Es de solo lectura</span><span class="sxs-lookup"><span data-stu-id="0616f-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0616f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0616f-106">Syntax</span></span>

<span data-ttu-id="0616f-107">*expresión* . Recuento</span><span class="sxs-lookup"><span data-stu-id="0616f-107">*expression* .Count</span></span>

<span data-ttu-id="0616f-108">*expresión* Variable que representa un objeto **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="0616f-108">*expression* A variable that represents a **QueryDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0616f-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0616f-109">Remarks</span></span>

<span data-ttu-id="0616f-p102">Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="0616f-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="0616f-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="0616f-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

