---
title: Count (propiedad, ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c710b02678940d898f910ef5215d879cd6ded163
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880862"
---
# <a name="count-property-ado"></a><span data-ttu-id="98bd1-102">Count (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="98bd1-102">Count property (ADO)</span></span>


<span data-ttu-id="98bd1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98bd1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98bd1-104">Indica el número de objetos de una colección.</span><span class="sxs-lookup"><span data-stu-id="98bd1-104">Indicates the number of objects in a collection.</span></span>

## <a name="return-value"></a><span data-ttu-id="98bd1-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98bd1-105">Return value</span></span>

<span data-ttu-id="98bd1-106">Devuelve un valor de tipo **Long**.</span><span class="sxs-lookup"><span data-stu-id="98bd1-106">Returns a **Long** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98bd1-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98bd1-107">Remarks</span></span>

<span data-ttu-id="98bd1-108">Utilice la propiedad **Count** para determinar cuántos objetos contiene una colección.</span><span class="sxs-lookup"><span data-stu-id="98bd1-108">Use the **Count** property to determine how many objects are in a given collection.</span></span>

<span data-ttu-id="98bd1-p101">Dado que la numeración de los miembros de una colección comienza por cero, deberá codificar siempre los bucles empezando con el miembro cero y terminando con el valor de la propiedad **Count** menos 1. Si utiliza Microsoft Visual Basic y desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, utilice el comando **For** **Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="98bd1-p101">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="98bd1-111">Si la propiedad **Count** es cero, significa que no hay ningún objeto en la colección.</span><span class="sxs-lookup"><span data-stu-id="98bd1-111">If the **Count** property is zero, there are no objects in the collection.</span></span>

