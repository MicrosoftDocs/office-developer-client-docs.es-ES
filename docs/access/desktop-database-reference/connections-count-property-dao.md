---
title: Connections.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c4f341abfea455acdc96a2883d0f4dee3bd2a5fe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484070"
---
# <a name="connectionscount-property-dao"></a><span data-ttu-id="46694-102">Connections.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="46694-102">Connections.Count Property (DAO)</span></span>


<span data-ttu-id="46694-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="46694-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="46694-104">Devuelve el número de objetos **[Connection](connection-object-dao.md)** de la colección **[Connections](connections-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="46694-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="46694-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46694-105">Syntax</span></span>

<span data-ttu-id="46694-106">*expresión* . Recuento</span><span class="sxs-lookup"><span data-stu-id="46694-106">*expression* .Count</span></span>

<span data-ttu-id="46694-107">*expresión* Variable que representa un objeto **Connections** .</span><span class="sxs-lookup"><span data-stu-id="46694-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="46694-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46694-108">Remarks</span></span>

<span data-ttu-id="46694-p101">Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="46694-p101">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="46694-p102">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="46694-p102">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

