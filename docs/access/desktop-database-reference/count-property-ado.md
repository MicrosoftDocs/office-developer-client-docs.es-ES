---
title: Propiedad Count (ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a341a82e5cdc9ed5a55ca9f4b80ba80c6875bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295474"
---
# <a name="count-property-ado"></a><span data-ttu-id="dfd81-102">Propiedad Count (ADO)</span><span class="sxs-lookup"><span data-stu-id="dfd81-102">Count property (ADO)</span></span>


<span data-ttu-id="dfd81-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfd81-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dfd81-104">Indica el número de objetos de una colección.</span><span class="sxs-lookup"><span data-stu-id="dfd81-104">Indicates the number of objects in a collection.</span></span>

## <a name="return-value"></a><span data-ttu-id="dfd81-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfd81-105">Return value</span></span>

<span data-ttu-id="dfd81-106">Devuelve un valor de tipo **Long**.</span><span class="sxs-lookup"><span data-stu-id="dfd81-106">Returns a **Long** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfd81-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dfd81-107">Remarks</span></span>

<span data-ttu-id="dfd81-108">Utilice la propiedad **Count** para determinar cuántos objetos contiene una colección.</span><span class="sxs-lookup"><span data-stu-id="dfd81-108">Use the **Count** property to determine how many objects are in a given collection.</span></span>

<span data-ttu-id="dfd81-p101">Dado que la numeración de los miembros de una colección comienza por cero, deberá codificar siempre los bucles empezando con el miembro cero y terminando con el valor de la propiedad **Count** menos 1. Si utiliza Microsoft Visual Basic y desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, utilice el comando **For** **Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="dfd81-p101">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="dfd81-111">Si la propiedad **Count** es cero, significa que no hay ningún objeto en la colección.</span><span class="sxs-lookup"><span data-stu-id="dfd81-111">If the **Count** property is zero, there are no objects in the collection.</span></span>

