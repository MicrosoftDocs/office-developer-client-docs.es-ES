---
title: Name (propiedad, ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 971a528c0efe97626f08ff94490e8aee25230f60
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926538"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="4ca66-102">Name (propiedad, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="4ca66-102">Name property (ADO MD)</span></span>


<span data-ttu-id="4ca66-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ca66-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ca66-104">Indica el nombre de un objeto.</span><span class="sxs-lookup"><span data-stu-id="4ca66-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="4ca66-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4ca66-105">Return values</span></span>

<span data-ttu-id="4ca66-106">Devuelve un valor **String** y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="4ca66-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ca66-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ca66-107">Remarks</span></span>

<span data-ttu-id="4ca66-p101">Puede recuperar la propiedad **Name** de un objeto mediante una referencia ordinal, después de la cual, puede hacer referencia al objeto directamente por el nombre. Por ejemplo, si cdf.CubeDefs(0).Name devuelve "Videoclub Bobs", puede hacer referencia a este [CubeDef](cubedef-object-ado-md.md) como cdf.CubeDefs("Videoclub Bobs").</span><span class="sxs-lookup"><span data-stu-id="4ca66-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

