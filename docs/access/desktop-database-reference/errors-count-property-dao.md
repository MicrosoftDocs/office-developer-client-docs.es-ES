---
title: Propiedad Errors.Count (DAO)
TOCTitle: Count Property
ms:assetid: ad135955-3b18-4f99-66d9-aff1492df13b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821719(v=office.15)
ms:contentKeyID: 48547028
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2cbbed2c7061b225d969dbd7554191e8db4a28a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293402"
---
# <a name="errorscount-property-dao"></a><span data-ttu-id="f991c-102">Propiedad Errors.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="f991c-102">Errors.Count property (DAO)</span></span>


<span data-ttu-id="f991c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f991c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f991c-104">Devuelve el número de objetos de la colección especificada.</span><span class="sxs-lookup"><span data-stu-id="f991c-104">Returns the number of objects in the specified collection.</span></span> <span data-ttu-id="f991c-105">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f991c-105">Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f991c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f991c-106">Syntax</span></span>

<span data-ttu-id="f991c-107">*expresión* . Count</span><span class="sxs-lookup"><span data-stu-id="f991c-107">*expression* .Count</span></span>

<span data-ttu-id="f991c-108">*expresión* Variable que representa un objeto **Errors.**</span><span class="sxs-lookup"><span data-stu-id="f991c-108">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f991c-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f991c-109">Remarks</span></span>

<span data-ttu-id="f991c-p102">Dado que los miembros de una colección comienzan por 0, deberá codificar siempre los bucles empezando con el miembro 0 y terminando con el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede utilizar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="f991c-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="f991c-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, indica que no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="f991c-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

