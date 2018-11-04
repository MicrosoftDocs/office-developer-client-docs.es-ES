---
title: Método Delete (colección de parámetros de ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 213d29ecd6599803c0fa2211a17ac14da7dc698a
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949456"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="744da-102">Método Delete (colección de parámetros de ADO)</span><span class="sxs-lookup"><span data-stu-id="744da-102">Delete method (ADO Parameters Collection)</span></span>

<span data-ttu-id="744da-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="744da-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="744da-104">Elimina un objeto de la colección [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="744da-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="744da-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="744da-105">Syntax</span></span>

<span data-ttu-id="744da-106">*Los parámetros*. Eliminar *índice*</span><span class="sxs-lookup"><span data-stu-id="744da-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="744da-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="744da-107">Parameters</span></span>

|<span data-ttu-id="744da-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="744da-108">Parameter</span></span>|<span data-ttu-id="744da-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="744da-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="744da-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="744da-110">*Index*</span></span> |<span data-ttu-id="744da-111">Valor de tipo **String** que contiene el nombre del objeto que se va a eliminar, o bien, la posición ordinal (índice) del objeto en la colección.</span><span class="sxs-lookup"><span data-stu-id="744da-111">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="744da-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="744da-112">Remarks</span></span>

<span data-ttu-id="744da-p101">El uso del método **Delete** en una colección permite quitar uno de los objetos de la colección. Este método está disponible solo en la colección **Parameters** de un objeto [Command](command-object-ado.md). Debe usar la propiedad [Name](parameter-object-ado.md) del objeto [Parameter](name-property-ado.md) o su índice de colección al llamar al método **Delete**; una variable de objeto no es un argumento válido.</span><span class="sxs-lookup"><span data-stu-id="744da-p101">Using the **Delete** method on a collection lets you remove one of the objects in the collection. This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object. You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

