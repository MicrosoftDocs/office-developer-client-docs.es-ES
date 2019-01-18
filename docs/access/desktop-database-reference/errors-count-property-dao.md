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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707258"
---
# <a name="errorscount-property-dao"></a><span data-ttu-id="b8194-102">Propiedad Errors.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="b8194-102">Errors.Count property (DAO)</span></span>


<span data-ttu-id="b8194-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8194-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b8194-p101">Devuelve el número de objetos de la colección especificada. Es de solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8194-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8194-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8194-106">Syntax</span></span>

<span data-ttu-id="b8194-107">*expresión* . Recuento</span><span class="sxs-lookup"><span data-stu-id="b8194-107">*expression* .Count</span></span>

<span data-ttu-id="b8194-108">*expresión* Variable que representa un objeto **Errors** .</span><span class="sxs-lookup"><span data-stu-id="b8194-108">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8194-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8194-109">Remarks</span></span>

<span data-ttu-id="b8194-p102">Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="b8194-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="b8194-p103">El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.</span><span class="sxs-lookup"><span data-stu-id="b8194-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

