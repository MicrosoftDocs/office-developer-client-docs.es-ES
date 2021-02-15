---
title: Propiedad Parameters.Count (DAO)
TOCTitle: Count Property
ms:assetid: bc8c814b-da55-22b7-431f-a0f7e6cac994
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822720(v=office.15)
ms:contentKeyID: 48547415
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 536e058a0485479cabd1cc2a0aae09f2396bfbcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287877"
---
# <a name="parameterscount-property-dao"></a><span data-ttu-id="01ef4-102">Propiedad Parameters.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="01ef4-102">Parameters.Count property (DAO)</span></span>


<span data-ttu-id="01ef4-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="01ef4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01ef4-104">Devuelve el número de objetos de la colección especificada.</span><span class="sxs-lookup"><span data-stu-id="01ef4-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="01ef4-105">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01ef4-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="01ef4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01ef4-106">Syntax</span></span>

<span data-ttu-id="01ef4-107">*expresión* . Count</span><span class="sxs-lookup"><span data-stu-id="01ef4-107">*expression* .Count</span></span>

<span data-ttu-id="01ef4-108">*expresión* Variable que representa un objeto **Parameters** .</span><span class="sxs-lookup"><span data-stu-id="01ef4-108">*expression* A variable that represents a **Parameters** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="01ef4-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01ef4-109">Remarks</span></span>

<span data-ttu-id="01ef4-p102">Dado que los miembros de una colección comienzan por 0, deberá codificar siempre los bucles empezando con el miembro 0 y terminando con el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede utilizar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="01ef4-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="01ef4-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, indica que no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="01ef4-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

