---
title: Databases.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1860f1719b4e26ab192450c66d610517f0ca9a6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868647"
---
# <a name="databasescount-property-dao"></a><span data-ttu-id="24052-102">Databases.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="24052-102">Databases.Count Property (DAO)</span></span>


<span data-ttu-id="24052-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24052-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24052-p101">Devuelve el número de objetos de la colección especificada. Es de solo lectura</span><span class="sxs-lookup"><span data-stu-id="24052-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="24052-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24052-106">Syntax</span></span>

<span data-ttu-id="24052-107">*expresión* . Recuento</span><span class="sxs-lookup"><span data-stu-id="24052-107">*expression* .Count</span></span>

<span data-ttu-id="24052-108">*expresión* Variable que representa un objeto de **las bases de datos** .</span><span class="sxs-lookup"><span data-stu-id="24052-108">*expression* A variable that represents a **Databases** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="24052-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24052-109">Remarks</span></span>

<span data-ttu-id="24052-p102">Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="24052-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="24052-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="24052-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

