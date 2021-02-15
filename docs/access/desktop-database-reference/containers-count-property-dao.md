---
title: Propiedad Containers.Count (DAO)
TOCTitle: Count Property
ms:assetid: 3b0bf865-a4d5-82bb-c1a9-9957f110db4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192657(v=office.15)
ms:contentKeyID: 48544276
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7553b0e7d64e059dfeed50f158f21f48455976d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295593"
---
# <a name="containerscount-property-dao"></a><span data-ttu-id="8d946-102">Propiedad Containers.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="8d946-102">Containers.Count property (DAO)</span></span>


<span data-ttu-id="8d946-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d946-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d946-104">Devuelve el número de objetos **[Connection](connection-object-dao.md)** de la colección **[Connections](connections-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="8d946-104">Returns the number of **[Connection](connection-object-dao.md)** objects in the **[Connections](connections-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d946-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d946-105">Syntax</span></span>

<span data-ttu-id="8d946-106">*expresión* . Count</span><span class="sxs-lookup"><span data-stu-id="8d946-106">*expression* .Count</span></span>

<span data-ttu-id="8d946-107">*expresión* Variable que representa un objeto **Connections.**</span><span class="sxs-lookup"><span data-stu-id="8d946-107">*expression* A variable that represents a **Connections** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d946-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8d946-108">Remarks</span></span>

<span data-ttu-id="8d946-p101">Dado que los miembros de una colección comienzan por 0, deberá codificar siempre los bucles empezando con el miembro 0 y terminando con el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede utilizar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="8d946-p101">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="8d946-p102">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, indica que no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="8d946-p102">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

