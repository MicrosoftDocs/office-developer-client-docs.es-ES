---
title: Relations.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 7cb3885f-6896-8402-8b18-12769473f051
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196377(v=office.15)
ms:contentKeyID: 48545843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1be0766c1f1a2057e5cb7137d2e9131a2505f75
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876011"
---
# <a name="relationscount-property-dao"></a><span data-ttu-id="73714-102">Relations.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="73714-102">Relations.Count Property (DAO)</span></span>


<span data-ttu-id="73714-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73714-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73714-p101">Devuelve el número de objetos de la colección especificada. Es de solo lectura</span><span class="sxs-lookup"><span data-stu-id="73714-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="73714-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73714-106">Syntax</span></span>

<span data-ttu-id="73714-107">*expresión* . Recuento</span><span class="sxs-lookup"><span data-stu-id="73714-107">*expression* .Count</span></span>

<span data-ttu-id="73714-108">*expresión* Variable que representa un objeto **Relations** .</span><span class="sxs-lookup"><span data-stu-id="73714-108">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="73714-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73714-109">Remarks</span></span>

<span data-ttu-id="73714-p102">Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="73714-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="73714-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="73714-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

