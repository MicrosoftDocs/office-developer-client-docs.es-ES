---
title: HASCATEGORY (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Devuelve TRUE si la cadena especificada se encuentra en la lista de categorías de la forma.
ms.openlocfilehash: 902819f981b53aed96695e181ab556d3841d97c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433356"
---
# <a name="hascategory-function"></a><span data-ttu-id="30c52-103">Función HASCATEGORY</span><span class="sxs-lookup"><span data-stu-id="30c52-103">HASCATEGORY Function</span></span>

<span data-ttu-id="30c52-104">Devuelve TRUE si la cadena especificada se encuentra en la lista de categorías de la forma.</span><span class="sxs-lookup"><span data-stu-id="30c52-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="30c52-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="30c52-105">Version Information</span></span>

<span data-ttu-id="30c52-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="30c52-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="30c52-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30c52-107">Syntax</span></span>

<span data-ttu-id="30c52-108">HASCATEGORY (\* \* *categoría* \* \*)</span><span class="sxs-lookup"><span data-stu-id="30c52-108">HASCATEGORY(\*\* *category* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="30c52-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30c52-109">Parameters</span></span>

|<span data-ttu-id="30c52-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="30c52-110">**Name**</span></span>|<span data-ttu-id="30c52-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="30c52-111">**Required/Optional**</span></span>|<span data-ttu-id="30c52-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="30c52-112">**Data Type**</span></span>|<span data-ttu-id="30c52-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="30c52-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="30c52-114">_Categoría_</span><span class="sxs-lookup"><span data-stu-id="30c52-114">_category_</span></span> <br/> |<span data-ttu-id="30c52-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="30c52-115">Required</span></span>  <br/> |<span data-ttu-id="30c52-116">**String**</span><span class="sxs-lookup"><span data-stu-id="30c52-116">**String**</span></span> <br/> |<span data-ttu-id="30c52-117">Categoría que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="30c52-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="30c52-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30c52-118">Return value</span></span>

 <span data-ttu-id="30c52-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="30c52-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30c52-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="30c52-120">Remarks</span></span>

 <span data-ttu-id="30c52-121">Las *categorías* son cadenas definidas por el usuario que puede usar para clasificar formas.</span><span class="sxs-lookup"><span data-stu-id="30c52-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="30c52-122">Las categorías se pueden definir en la celda User.msvShapeCategories, en la ShapeSheet de una forma.</span><span class="sxs-lookup"><span data-stu-id="30c52-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="30c52-123">Puede definir varias categorías relativas a una forma si las separa con punto y coma.</span><span class="sxs-lookup"><span data-stu-id="30c52-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

