---
title: Count (propiedad, ADO)
TOCTitle: Count Property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad02d854a560e3fa99bf7454c97083e88638c520
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484937"
---
# <a name="count-property-ado"></a><span data-ttu-id="4ac39-102">Count (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="4ac39-102">Count Property (ADO)</span></span>


<span data-ttu-id="4ac39-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ac39-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4ac39-104">Indica el número de objetos de una colección.</span><span class="sxs-lookup"><span data-stu-id="4ac39-104">Indicates the number of objects in a collection.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ac39-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ac39-105">Return Value</span></span>

<span data-ttu-id="4ac39-106">Devuelve un valor de tipo **Long**.</span><span class="sxs-lookup"><span data-stu-id="4ac39-106">Returns a **Long** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ac39-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ac39-107">Remarks</span></span>

<span data-ttu-id="4ac39-108">Utilice la propiedad **Count** para determinar cuántos objetos contiene una colección.</span><span class="sxs-lookup"><span data-stu-id="4ac39-108">Use the **Count** property to determine how many objects are in a given collection.</span></span>

<span data-ttu-id="4ac39-p101">Dado que la numeración de los miembros de una colección comienza por cero, deberá codificar siempre los bucles empezando con el miembro cero y terminando con el valor de la propiedad **Count** menos 1. Si utiliza Microsoft Visual Basic y desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, utilice el comando **For** **Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="4ac39-p101">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="4ac39-111">Si la propiedad **Count** es cero, significa que no hay ningún objeto en la colección.</span><span class="sxs-lookup"><span data-stu-id="4ac39-111">If the **Count** property is zero, there are no objects in the collection.</span></span>

