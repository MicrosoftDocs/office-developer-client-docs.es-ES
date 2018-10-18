---
title: Description (propiedad, ADO MD)
TOCTitle: Description Property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dd66e0288e20bcf38adefc2fcc30f1856ebf3e6
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606874"
---
# <a name="description-property-ado-md"></a><span data-ttu-id="48598-102">Description (propiedad, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="48598-102">Description Property (ADO MD)</span></span>


<span data-ttu-id="48598-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="48598-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="48598-104">Devuelve un texto de explicación del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="48598-104">Returns a text explanation of the current object.</span></span>

<span data-ttu-id="48598-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="48598-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="48598-106">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="48598-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="48598-107">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="48598-107">Return values</span></span>
>>>>>>> <span data-ttu-id="48598-108">master</span><span class="sxs-lookup"><span data-stu-id="48598-108">master</span></span>

<span data-ttu-id="48598-109">Devuelve un valor **String** y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="48598-109">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="48598-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48598-110">Remarks</span></span>

<span data-ttu-id="48598-p101">Para objetos [Member](member-object-ado-md.md), **Description** se aplica únicamente a elementos de medida y de fórmula. **Description** devuelve una cadena vacía ("") para todos los demás tipos de elementos. Para obtener más información acerca de los distintos tipos de elementos, vea la propiedad [Tipo](type-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="48598-p101">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members. **Description** returns an empty string ("") for all other types of members. For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span></span>

<span data-ttu-id="48598-p102">Esta propiedad sólo es compatible con objetos **Member** pertenecientes a un objeto [Level](level-object-ado-md.md). Si se hace referencia a esta propiedad desde objetos **Member** pertenecientes a un objeto [Position](position-object-ado-md.md), se produce un error.</span><span class="sxs-lookup"><span data-stu-id="48598-p102">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

