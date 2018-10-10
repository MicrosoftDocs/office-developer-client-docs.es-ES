---
title: Delete (método, Colección Parameters de ADO)
TOCTitle: Delete Method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 43d193a78be10ec5cedc2fe1a4001e677878dfb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485569"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="6b462-102">Delete (método, Colección Parameters de ADO)</span><span class="sxs-lookup"><span data-stu-id="6b462-102">Delete Method (ADO Parameters Collection)</span></span>


<span data-ttu-id="6b462-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b462-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="6b462-104">Elimina un objeto de la colección [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6b462-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b462-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b462-105">Syntax</span></span>

<span data-ttu-id="6b462-106">*Los parámetros*. Eliminar *índice*</span><span class="sxs-lookup"><span data-stu-id="6b462-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="6b462-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b462-107">Parameters</span></span>

  - <span data-ttu-id="6b462-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="6b462-108">*Index*</span></span>

  - <span data-ttu-id="6b462-109">Valor de tipo **String** que contiene el nombre del objeto que se va a eliminar, o bien, la posición ordinal (índice) del objeto en la colección.</span><span class="sxs-lookup"><span data-stu-id="6b462-109">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b462-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b462-110">Remarks</span></span>

<span data-ttu-id="6b462-p101">El uso del método **Delete** en una colección permite quitar uno de los objetos de la colección. Este método está disponible solo en la colección **Parameters** de un objeto [Command](command-object-ado.md). Debe usar la propiedad [Name](parameter-object-ado.md) del objeto [Parameter](name-property-ado.md) o su índice de colección al llamar al método **Delete**; una variable de objeto no es un argumento válido.</span><span class="sxs-lookup"><span data-stu-id="6b462-p101">Using the **Delete** method on a collection lets you remove one of the objects in the collection. This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object. You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

