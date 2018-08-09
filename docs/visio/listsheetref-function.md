---
title: LISTSHEETREF (función)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ddbc35-8577-0a96-20b8-aa7734764c5b
description: Devuelve una referencia de hoja a la forma del contenedor de lista que contiene la forma.
ms.openlocfilehash: 75c765fab2d287c2da83a659dbbf070d29a9d325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822504"
---
# <a name="listsheetref-function"></a><span data-ttu-id="80f53-103">Función LISTSHEETREF</span><span class="sxs-lookup"><span data-stu-id="80f53-103">LISTSHEETREF Function</span></span>

<span data-ttu-id="80f53-104">Devuelve una referencia de hoja a la forma del contenedor de lista que contiene la forma.</span><span class="sxs-lookup"><span data-stu-id="80f53-104">Returns a sheet reference to the list container shape that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="80f53-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="80f53-105">Version Information</span></span>

<span data-ttu-id="80f53-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="80f53-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="80f53-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80f53-107">Syntax</span></span>

<span data-ttu-id="80f53-108">LISTMEMBERCOUNT()</span><span class="sxs-lookup"><span data-stu-id="80f53-108">LISTMEMBERCOUNT()</span></span>
  
### <a name="return-value"></a><span data-ttu-id="80f53-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80f53-109">Return value</span></span>

<span data-ttu-id="80f53-110">Referencia de ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="80f53-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="80f53-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80f53-111">Remarks</span></span>

<span data-ttu-id="80f53-112">Si la forma no es un miembro de la lista, la función LISTSHEETREF devuelve #REF!.</span><span class="sxs-lookup"><span data-stu-id="80f53-112">If the shape is not a list member, the LISTSHEETREF function returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="80f53-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="80f53-113">Example</span></span>

<span data-ttu-id="80f53-114">LISTSHEETREF(1)!Height</span><span class="sxs-lookup"><span data-stu-id="80f53-114">LISTSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="80f53-115">Devuelve el valor de la celda Height de la forma del contenedor de lista que contiene la forma.</span><span class="sxs-lookup"><span data-stu-id="80f53-115">Returns the value in the Height cell of the list container shape that contains the shape.</span></span> 
  

