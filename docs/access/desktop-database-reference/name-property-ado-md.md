---
title: Name (propiedad, ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63e098a8b97bb37fad2ef256affb2da142daf434
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878650"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="c6d3f-102">Name (propiedad, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="c6d3f-102">Name Property (ADO MD)</span></span>


<span data-ttu-id="c6d3f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6d3f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c6d3f-104">Indica el nombre de un objeto.</span><span class="sxs-lookup"><span data-stu-id="c6d3f-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="c6d3f-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="c6d3f-105">Return values</span></span>

<span data-ttu-id="c6d3f-106">Devuelve un valor **String** y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c6d3f-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6d3f-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c6d3f-107">Remarks</span></span>

<span data-ttu-id="c6d3f-p101">Puede recuperar la propiedad **Name** de un objeto mediante una referencia ordinal, después de la cual, puede hacer referencia al objeto directamente por el nombre. Por ejemplo, si cdf.CubeDefs(0).Name devuelve "Videoclub Bobs", puede hacer referencia a este [CubeDef](cubedef-object-ado-md.md) como cdf.CubeDefs("Videoclub Bobs").</span><span class="sxs-lookup"><span data-stu-id="c6d3f-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

