---
title: Name (propiedad, ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90a77ae9d8c32ff8d0a13eacb146fc0e3ab3f397
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602471"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="0a744-102">Name (propiedad, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="0a744-102">Name Property (ADO MD)</span></span>


<span data-ttu-id="0a744-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a744-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0a744-104">Indica el nombre de un objeto.</span><span class="sxs-lookup"><span data-stu-id="0a744-104">Indicates the name of an object.</span></span>

<span data-ttu-id="0a744-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="0a744-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="0a744-106">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="0a744-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="0a744-107">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="0a744-107">Return values</span></span>
>>>>>>> <span data-ttu-id="0a744-108">master</span><span class="sxs-lookup"><span data-stu-id="0a744-108">master</span></span>

<span data-ttu-id="0a744-109">Devuelve un valor **String** y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0a744-109">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a744-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a744-110">Remarks</span></span>

<span data-ttu-id="0a744-p101">Puede recuperar la propiedad **Name** de un objeto mediante una referencia ordinal, después de la cual, puede hacer referencia al objeto directamente por el nombre. Por ejemplo, si cdf.CubeDefs(0).Name devuelve "Videoclub Bobs", puede hacer referencia a este [CubeDef](cubedef-object-ado-md.md) como cdf.CubeDefs("Videoclub Bobs").</span><span class="sxs-lookup"><span data-stu-id="0a744-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

