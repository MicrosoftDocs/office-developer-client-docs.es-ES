---
title: Item (propiedad, ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4afbb31fb95aeea66d9cf93624b95c8796e2d25
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949365"
---
# <a name="item-property-ado"></a><span data-ttu-id="dec24-102">Item (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="dec24-102">Item property (ADO)</span></span>

<span data-ttu-id="dec24-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dec24-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dec24-104">Indica un miembro específico de una colección, por nombre o número ordinal.</span><span class="sxs-lookup"><span data-stu-id="dec24-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec24-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dec24-105">Syntax</span></span>

<span data-ttu-id="dec24-106">*Objeto*de conjunto de = *colección*. Item (Index)</span><span class="sxs-lookup"><span data-stu-id="dec24-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="dec24-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dec24-107">Return value</span></span>

<span data-ttu-id="dec24-108">Devuelve una referencia de objeto.</span><span class="sxs-lookup"><span data-stu-id="dec24-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="dec24-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dec24-109">Parameters</span></span>

|<span data-ttu-id="dec24-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dec24-110">Parameter</span></span>|<span data-ttu-id="dec24-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="dec24-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="dec24-112">*Index*</span><span class="sxs-lookup"><span data-stu-id="dec24-112">*Index*</span></span> |<span data-ttu-id="dec24-113">Una expresión de tipo **Variant** que evalúa el nombre o el número ordinal de un objeto de una colección.</span><span class="sxs-lookup"><span data-stu-id="dec24-113">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="dec24-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dec24-114">Remarks</span></span>

<span data-ttu-id="dec24-115">Utilice la propiedad **Item** para devolver un objeto específico de una colección.</span><span class="sxs-lookup"><span data-stu-id="dec24-115">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="dec24-116">Si el **elemento** no se puede encontrar un objeto en la colección que corresponde al argumento *Index* , se produce un error.</span><span class="sxs-lookup"><span data-stu-id="dec24-116">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="dec24-117">Además, algunas colecciones no admiten objetos con nombre; en estas colecciones es necesario utilizar referencias de número ordinal.</span><span class="sxs-lookup"><span data-stu-id="dec24-117">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="dec24-118">**Item** es la propiedad predeterminada para todas las colecciones; por lo tanto, los siguientes formatos de sintaxis son intercambiables:</span><span class="sxs-lookup"><span data-stu-id="dec24-118">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
