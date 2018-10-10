---
title: Errors.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: ad135955-3b18-4f99-66d9-aff1492df13b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821719(v=office.15)
ms:contentKeyID: 48547028
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b554b88153e79dfc1909bd55d95a3c3e48a855e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486406"
---
# <a name="errorscount-property-dao"></a><span data-ttu-id="2e2ae-102">Errors.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="2e2ae-102">Errors.Count Property (DAO)</span></span>


<span data-ttu-id="2e2ae-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e2ae-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2e2ae-p101">Devuelve el número de objetos de la colección especificada. Es de solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e2ae-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e2ae-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e2ae-106">Syntax</span></span>

<span data-ttu-id="2e2ae-107">*expresión* . Recuento</span><span class="sxs-lookup"><span data-stu-id="2e2ae-107">*expression* .Count</span></span>

<span data-ttu-id="2e2ae-108">*expresión* Variable que representa un objeto **Errors** .</span><span class="sxs-lookup"><span data-stu-id="2e2ae-108">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e2ae-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e2ae-109">Remarks</span></span>

<span data-ttu-id="2e2ae-p102">Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="2e2ae-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="2e2ae-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

