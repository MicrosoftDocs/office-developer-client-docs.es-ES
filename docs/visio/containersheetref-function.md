---
title: CONTAINERSHEETREF (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Devuelve una hoja de referencia al contenedor especificado que contiene la forma.
ms.openlocfilehash: 6392b4c1a2652f1a831dc585c0be0f430a5ffe0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821865"
---
# <a name="containersheetref-function"></a><span data-ttu-id="8d8bb-103">Función CONTAINERSHEETREF</span><span class="sxs-lookup"><span data-stu-id="8d8bb-103">CONTAINERSHEETREF Function</span></span>

<span data-ttu-id="8d8bb-104">Devuelve una hoja de referencia al contenedor especificado que contiene la forma.</span><span class="sxs-lookup"><span data-stu-id="8d8bb-104">Returns a sheet reference to the specified container that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="8d8bb-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="8d8bb-105">Version Information</span></span>

<span data-ttu-id="8d8bb-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="8d8bb-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8d8bb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d8bb-107">Syntax</span></span>

<span data-ttu-id="8d8bb-108">CONTAINERSHEETREF (** *índice* ** ** *[, categoría]* **)</span><span class="sxs-lookup"><span data-stu-id="8d8bb-108">CONTAINERSHEETREF(** *index* ** ** *[, category]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8d8bb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d8bb-109">Parameters</span></span>

|<span data-ttu-id="8d8bb-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8d8bb-110">**Name**</span></span>|<span data-ttu-id="8d8bb-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="8d8bb-111">**Required/Optional**</span></span>|<span data-ttu-id="8d8bb-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="8d8bb-112">**Data Type**</span></span>|<span data-ttu-id="8d8bb-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d8bb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8d8bb-114">_index_</span><span class="sxs-lookup"><span data-stu-id="8d8bb-114">_index_</span></span> <br/> |<span data-ttu-id="8d8bb-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8d8bb-115">Required</span></span>  <br/> |<span data-ttu-id="8d8bb-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8d8bb-116">**Integer**</span></span> <br/> |<span data-ttu-id="8d8bb-p101">Índice basado en 1 del contenedor. Para obtener más información, vea los comentarios.</span><span class="sxs-lookup"><span data-stu-id="8d8bb-p101">The 1-based index of the container. See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="8d8bb-119">_category_</span><span class="sxs-lookup"><span data-stu-id="8d8bb-119">_category_</span></span> <br/> |<span data-ttu-id="8d8bb-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="8d8bb-120">Optional</span></span>  <br/> |<span data-ttu-id="8d8bb-121">**String**</span><span class="sxs-lookup"><span data-stu-id="8d8bb-121">**String**</span></span> <br/> |<span data-ttu-id="8d8bb-p102">Categoría del contenedor. Para obtener más información, vea los comentarios.</span><span class="sxs-lookup"><span data-stu-id="8d8bb-p102">The category of the container. See Remarks for more information.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8d8bb-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d8bb-124">Return value</span></span>

<span data-ttu-id="8d8bb-125">Referencia de ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="8d8bb-125">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d8bb-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d8bb-126">Remarks</span></span>

<span data-ttu-id="8d8bb-127">El índice de un contenedor se calcula a partir del orden Z de los contenedores, de delante hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="8d8bb-127">The index of a container is calculated based on the z-order of containers from front to back.</span></span>
  
 <span data-ttu-id="8d8bb-128">*Las categorías* son cadenas definidas por el usuario que puede usar para clasificar las formas.</span><span class="sxs-lookup"><span data-stu-id="8d8bb-128">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="8d8bb-129">Puede definir las categorías en la celda User.msvShapeCategories de la ShapeSheet de una forma.</span><span class="sxs-lookup"><span data-stu-id="8d8bb-129">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="8d8bb-130">Puede definir varias categorías de una forma, separe las categorías con punto y coma.</span><span class="sxs-lookup"><span data-stu-id="8d8bb-130">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  
<span data-ttu-id="8d8bb-131">Si la forma no es miembro de un contenedor o si no hay un contenedor que concuerde tanto con la categoría como con el número de índice especificados, CONTAINERSHEETREF devuelve #REF!.</span><span class="sxs-lookup"><span data-stu-id="8d8bb-131">If the shape is not a member of a container, or if there is no container that matches both the specified index number and the category, CONTAINERSHEETREF returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="8d8bb-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8d8bb-132">Example</span></span>

<span data-ttu-id="8d8bb-133">CONTAINERSHEETREF(1)!Height</span><span class="sxs-lookup"><span data-stu-id="8d8bb-133">CONTAINERSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="8d8bb-134">Devuelve el valor de la celda Height del contenedor que se encuentra más hacia delante en la página a la que pertenece la forma.</span><span class="sxs-lookup"><span data-stu-id="8d8bb-134">Returns the value in the Height cell of the container that is most forward on the page to which the shape belongs.</span></span> 
  

