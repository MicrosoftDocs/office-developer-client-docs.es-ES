---
title: Item (propiedad, ADO)
TOCTitle: Item Property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29453ac2801f606640fd6d9506a8ee1ee8625396
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483605"
---
# <a name="item-property-ado"></a><span data-ttu-id="8dfc3-102">Item (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="8dfc3-102">Item Property (ADO)</span></span>

<span data-ttu-id="8dfc3-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8dfc3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8dfc3-104">Indica un miembro específico de una colección, por nombre o número ordinal.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dfc3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8dfc3-105">Syntax</span></span>

<span data-ttu-id="8dfc3-106">*Objeto*de conjunto de = *colección*. Item (Index)</span><span class="sxs-lookup"><span data-stu-id="8dfc3-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="8dfc3-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8dfc3-107">Return Value</span></span>

<span data-ttu-id="8dfc3-108">Devuelve una referencia de objeto.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="8dfc3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8dfc3-109">Parameters</span></span>

- <span data-ttu-id="8dfc3-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="8dfc3-110">*Index*</span></span>

- <span data-ttu-id="8dfc3-111">Una expresión de tipo **Variant** que evalúa el nombre o el número ordinal de un objeto de una colección.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-111">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dfc3-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8dfc3-112">Remarks</span></span>

<span data-ttu-id="8dfc3-113">Utilice la propiedad **Item** para devolver un objeto específico de una colección.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-113">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="8dfc3-114">Si el **elemento** no se puede encontrar un objeto en la colección que corresponde al argumento *Index* , se produce un error.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-114">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="8dfc3-115">Además, algunas colecciones no admiten objetos con nombre; en estas colecciones es necesario utilizar referencias de número ordinal.</span><span class="sxs-lookup"><span data-stu-id="8dfc3-115">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="8dfc3-116">**Item** es la propiedad predeterminada para todas las colecciones; por lo tanto, los siguientes formatos de sintaxis son intercambiables:</span><span class="sxs-lookup"><span data-stu-id="8dfc3-116">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
