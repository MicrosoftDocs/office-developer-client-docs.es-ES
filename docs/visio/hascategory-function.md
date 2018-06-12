---
title: HASCATEGORY (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Devuelve TRUE si la cadena especificada se encuentra en la lista de categorías de la forma.
ms.openlocfilehash: 2445b4c3af63b331b303897997ce38b0747f17fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822273"
---
# <a name="hascategory-function"></a><span data-ttu-id="78e0b-103">HASCATEGORY (función)</span><span class="sxs-lookup"><span data-stu-id="78e0b-103">HASCATEGORY Function</span></span>

<span data-ttu-id="78e0b-104">Devuelve TRUE si la cadena especificada se encuentra en la lista de categorías de la forma.</span><span class="sxs-lookup"><span data-stu-id="78e0b-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="78e0b-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="78e0b-105">Version Information</span></span>

<span data-ttu-id="78e0b-106">Versión agregada: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="78e0b-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="78e0b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78e0b-107">Syntax</span></span>

<span data-ttu-id="78e0b-108">HASCATEGORY (** *categoría* **)</span><span class="sxs-lookup"><span data-stu-id="78e0b-108">HASCATEGORY(** *category* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="78e0b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78e0b-109">Parameters</span></span>

|<span data-ttu-id="78e0b-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="78e0b-110">**Name**</span></span>|<span data-ttu-id="78e0b-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="78e0b-111">**Required/Optional**</span></span>|<span data-ttu-id="78e0b-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="78e0b-112">**Data Type**</span></span>|<span data-ttu-id="78e0b-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="78e0b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="78e0b-114">_category_</span><span class="sxs-lookup"><span data-stu-id="78e0b-114">_category_</span></span> <br/> |<span data-ttu-id="78e0b-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="78e0b-115">Required</span></span>  <br/> |<span data-ttu-id="78e0b-116">**String**</span><span class="sxs-lookup"><span data-stu-id="78e0b-116">**String**</span></span> <br/> |<span data-ttu-id="78e0b-117">Categoría que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="78e0b-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="78e0b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78e0b-118">Return value</span></span>

 <span data-ttu-id="78e0b-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="78e0b-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="78e0b-120">Notas</span><span class="sxs-lookup"><span data-stu-id="78e0b-120">Remarks</span></span>

 <span data-ttu-id="78e0b-121">*Las categorías* son cadenas definidas por el usuario que puede usar para clasificar las formas.</span><span class="sxs-lookup"><span data-stu-id="78e0b-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="78e0b-122">Puede definir las categorías en la celda User.msvShapeCategories de la ShapeSheet de una forma.</span><span class="sxs-lookup"><span data-stu-id="78e0b-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="78e0b-123">Puede definir varias categorías de una forma, separe las categorías con punto y coma.</span><span class="sxs-lookup"><span data-stu-id="78e0b-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

