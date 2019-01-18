---
title: Propiedad Fields.Count (DAO)
TOCTitle: Count Property
ms:assetid: 574de1db-2640-159b-7756-28c37acc9f83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194261(v=office.15)
ms:contentKeyID: 48544969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99eb21ba4f4ef13c902fc0d029dba59c30066853
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701198"
---
# <a name="fieldscount-property-dao"></a><span data-ttu-id="9507e-102">Propiedad Fields.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="9507e-102">Fields.Count property (DAO)</span></span>


<span data-ttu-id="9507e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9507e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9507e-p101">Devuelve el número de objetos de la colección especificada. **Integer** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="9507e-p101">Returns the number of objects in the specified collection. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9507e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9507e-106">Syntax</span></span>

<span data-ttu-id="9507e-107">*expresión* . Recuento</span><span class="sxs-lookup"><span data-stu-id="9507e-107">*expression* .Count</span></span>

<span data-ttu-id="9507e-108">*expresión* Variable que representa un objeto **Fields** .</span><span class="sxs-lookup"><span data-stu-id="9507e-108">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9507e-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9507e-109">Remarks</span></span>

<span data-ttu-id="9507e-p102">Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="9507e-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="9507e-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="9507e-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

