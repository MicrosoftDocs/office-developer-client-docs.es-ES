---
title: Propiedad Recordsets.Count (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a81c1ede8a3afb95e39b2c33fb8112119faf8bd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309293"
---
# <a name="recordsetscount-property-dao"></a><span data-ttu-id="8912a-102">Propiedad Recordsets.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="8912a-102">Recordsets.Count property (DAO)</span></span>


<span data-ttu-id="8912a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8912a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8912a-104">Devuelve el número de objetos de la colección especificada.</span><span class="sxs-lookup"><span data-stu-id="8912a-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="8912a-105">**Integer** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="8912a-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8912a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8912a-106">Syntax</span></span>

<span data-ttu-id="8912a-107">*expresión* . Count</span><span class="sxs-lookup"><span data-stu-id="8912a-107">*expression* .Count</span></span>

<span data-ttu-id="8912a-108">*expresión* Variable que representa un objeto **Recordsets.**</span><span class="sxs-lookup"><span data-stu-id="8912a-108">*expression* A variable that represents a **Recordsets** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8912a-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8912a-109">Remarks</span></span>

<span data-ttu-id="8912a-p102">Dado que los miembros de una colección comienzan por 0, deberá codificar siempre los bucles empezando con el miembro 0 y terminando con el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede utilizar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="8912a-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="8912a-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, indica que no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="8912a-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

