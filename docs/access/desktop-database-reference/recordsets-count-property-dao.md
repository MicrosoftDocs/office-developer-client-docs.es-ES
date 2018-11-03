---
title: Propiedad Recordsets.Count (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 778367a39a1e27bdf405b897e88ad37c72f0cd6f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927903"
---
# <a name="recordsetscount-property-dao"></a><span data-ttu-id="c5e8b-102">Propiedad Recordsets.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="c5e8b-102">Recordsets.Count property (DAO)</span></span>


<span data-ttu-id="c5e8b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5e8b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5e8b-p101">Devuelve el número de objetos de la colección especificada. **Integer** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c5e8b-p101">Returns the number of objects in the specified collection. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e8b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5e8b-106">Syntax</span></span>

<span data-ttu-id="c5e8b-107">*expresión* . Recuento</span><span class="sxs-lookup"><span data-stu-id="c5e8b-107">*expression* .Count</span></span>

<span data-ttu-id="c5e8b-108">*expresión* Variable que representa un objeto **Recordsets** .</span><span class="sxs-lookup"><span data-stu-id="c5e8b-108">*expression* A variable that represents a **Recordsets** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5e8b-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5e8b-109">Remarks</span></span>

<span data-ttu-id="c5e8b-p102">Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="c5e8b-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="c5e8b-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="c5e8b-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

