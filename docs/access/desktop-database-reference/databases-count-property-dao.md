---
title: Propiedad Databases.Count (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbdaad343e1c149ea1f30b5c2d360cbd7bd6f1d8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927651"
---
# <a name="databasescount-property-dao"></a><span data-ttu-id="43247-102">Propiedad Databases.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="43247-102">Databases.Count property (DAO)</span></span>


<span data-ttu-id="43247-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="43247-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43247-p101">Devuelve el número de objetos de la colección especificada. Es de solo lectura</span><span class="sxs-lookup"><span data-stu-id="43247-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="43247-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43247-106">Syntax</span></span>

<span data-ttu-id="43247-107">*expresión* . Recuento</span><span class="sxs-lookup"><span data-stu-id="43247-107">*expression* .Count</span></span>

<span data-ttu-id="43247-108">*expresión* Variable que representa un objeto de **las bases de datos** .</span><span class="sxs-lookup"><span data-stu-id="43247-108">*expression* A variable that represents a **Databases** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="43247-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43247-109">Remarks</span></span>

<span data-ttu-id="43247-p102">Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="43247-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="43247-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="43247-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

