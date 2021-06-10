---
title: Propiedad TableDefs.Count (DAO)
TOCTitle: Count Property
ms:assetid: 6e2cf3e5-524f-a643-b1dc-99a4b2bb2e63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195561(v=office.15)
ms:contentKeyID: 48545508
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6c997a437cc7a7ae1461e7308899c85dac44fbda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314269"
---
# <a name="tabledefscount-property-dao"></a><span data-ttu-id="0971e-102">Propiedad TableDefs.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="0971e-102">TableDefs.Count property (DAO)</span></span>


<span data-ttu-id="0971e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0971e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0971e-p101">Devuelve el número de objetos de la colección especificada. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0971e-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0971e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0971e-106">Syntax</span></span>

<span data-ttu-id="0971e-107">*expresión* . Recuento</span><span class="sxs-lookup"><span data-stu-id="0971e-107">*expression* .Count</span></span>

<span data-ttu-id="0971e-108">*expresión* Variable que representa un **objeto TableDefs.**</span><span class="sxs-lookup"><span data-stu-id="0971e-108">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0971e-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0971e-109">Remarks</span></span>

<span data-ttu-id="0971e-p102">Dado que los miembros de una colección comienzan por 0, deberá codificar siempre los bucles empezando con el miembro 0 y terminando con el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede utilizar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="0971e-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="0971e-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, indica que no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="0971e-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

