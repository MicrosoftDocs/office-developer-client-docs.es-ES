---
title: Propiedad Databases.Count (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd8908492721315202c5bdf26109753c88905a07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294627"
---
# <a name="databasescount-property-dao"></a><span data-ttu-id="911e1-102">Propiedad Databases.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="911e1-102">Databases.Count property (DAO)</span></span>


<span data-ttu-id="911e1-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="911e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="911e1-p101">Devuelve el número de objetos de la colección especificada. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="911e1-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="911e1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="911e1-106">Syntax</span></span>

<span data-ttu-id="911e1-107">*expresión* . Recuento</span><span class="sxs-lookup"><span data-stu-id="911e1-107">*expression* .Count</span></span>

<span data-ttu-id="911e1-108">*expresión* Variable que representa un **objeto Databases.**</span><span class="sxs-lookup"><span data-stu-id="911e1-108">*expression* A variable that represents a **Databases** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="911e1-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="911e1-109">Remarks</span></span>

<span data-ttu-id="911e1-p102">Dado que los miembros de una colección comienzan por 0, deberá codificar siempre los bucles empezando con el miembro 0 y terminando con el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede utilizar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="911e1-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="911e1-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, indica que no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="911e1-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

