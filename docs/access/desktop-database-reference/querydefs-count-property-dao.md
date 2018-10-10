---
title: QueryDefs.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 8caa01c5-692f-95e4-4b11-6e6c591f5872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197340(v=office.15)
ms:contentKeyID: 48546240
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be630e54ef55fae335347dabd61440dfe457c5ed
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485328"
---
# <a name="querydefscount-property-dao"></a><span data-ttu-id="d7aae-102">QueryDefs.Count Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="d7aae-102">QueryDefs.Count Property (DAO)</span></span>


<span data-ttu-id="d7aae-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7aae-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d7aae-p101">Devuelve el número de objetos de la colección especificada. Es de solo lectura</span><span class="sxs-lookup"><span data-stu-id="d7aae-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7aae-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7aae-106">Syntax</span></span>

<span data-ttu-id="d7aae-107">*expresión* . Recuento</span><span class="sxs-lookup"><span data-stu-id="d7aae-107">*expression* .Count</span></span>

<span data-ttu-id="d7aae-108">*expresión* Variable que representa un objeto **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="d7aae-108">*expression* A variable that represents a **QueryDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7aae-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7aae-109">Remarks</span></span>

<span data-ttu-id="d7aae-p102">Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="d7aae-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="d7aae-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="d7aae-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

