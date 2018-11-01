---
title: Indexes.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 195ede10-f91e-50c6-6af4-b318c476b9ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845647(v=office.15)
ms:contentKeyID: 48543499
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 47c42a1275b4d19f79cb73599fc2ef376e0ca25d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884180"
---
# <a name="indexescount-property-dao"></a><span data-ttu-id="b47d9-102">Indexes.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="b47d9-102">Indexes.Count Property (DAO)</span></span>


<span data-ttu-id="b47d9-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b47d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b47d9-p101">Devuelve el número de objetos de la colección especificada. Es de solo lectura</span><span class="sxs-lookup"><span data-stu-id="b47d9-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b47d9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b47d9-106">Syntax</span></span>

<span data-ttu-id="b47d9-107">*expresión* . Recuento</span><span class="sxs-lookup"><span data-stu-id="b47d9-107">*expression* .Count</span></span>

<span data-ttu-id="b47d9-108">*expresión* Variable que representa un objeto **Indexes** .</span><span class="sxs-lookup"><span data-stu-id="b47d9-108">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b47d9-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b47d9-109">Remarks</span></span>

<span data-ttu-id="b47d9-p102">Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="b47d9-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="b47d9-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="b47d9-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

