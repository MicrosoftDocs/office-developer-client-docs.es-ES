---
title: CONTAINERSHEETREF (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Devuelve una hoja de referencia al contenedor especificado que contiene la forma.
ms.openlocfilehash: 473d8c0b81ecc568c1d4f3a3b3a885e1ceb4e00d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437269"
---
# <a name="containersheetref-function"></a><span data-ttu-id="b71f4-103">Función CONTAINERSHEETREF</span><span class="sxs-lookup"><span data-stu-id="b71f4-103">CONTAINERSHEETREF Function</span></span>

<span data-ttu-id="b71f4-104">Devuelve una hoja de referencia al contenedor especificado que contiene la forma.</span><span class="sxs-lookup"><span data-stu-id="b71f4-104">Returns a sheet reference to the specified container that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="b71f4-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="b71f4-105">Version Information</span></span>

<span data-ttu-id="b71f4-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="b71f4-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b71f4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b71f4-107">Syntax</span></span>

<span data-ttu-id="b71f4-108">CONTAINERSHEETREF (\* \* *Índice* \* \* \* \* *[, categoría]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b71f4-108">CONTAINERSHEETREF(\*\* *index* \*\* \*\* *[, category]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b71f4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b71f4-109">Parameters</span></span>

|<span data-ttu-id="b71f4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="b71f4-110">**Name**</span></span>|<span data-ttu-id="b71f4-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="b71f4-111">**Required/Optional**</span></span>|<span data-ttu-id="b71f4-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="b71f4-112">**Data Type**</span></span>|<span data-ttu-id="b71f4-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b71f4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b71f4-114">_index_</span><span class="sxs-lookup"><span data-stu-id="b71f4-114">_index_</span></span> <br/> |<span data-ttu-id="b71f4-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b71f4-115">Required</span></span>  <br/> |<span data-ttu-id="b71f4-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="b71f4-116">**Integer**</span></span> <br/> |<span data-ttu-id="b71f4-117">Índice basado en 1 del contenedor.</span><span class="sxs-lookup"><span data-stu-id="b71f4-117">The 1-based index of the container.</span></span> <span data-ttu-id="b71f4-118">Para obtener más información, vea los Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b71f4-118">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="b71f4-119">_Categoría_</span><span class="sxs-lookup"><span data-stu-id="b71f4-119">_category_</span></span> <br/> |<span data-ttu-id="b71f4-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="b71f4-120">Optional</span></span>  <br/> |<span data-ttu-id="b71f4-121">**String**</span><span class="sxs-lookup"><span data-stu-id="b71f4-121">**String**</span></span> <br/> |<span data-ttu-id="b71f4-122">Categoría del contenedor.</span><span class="sxs-lookup"><span data-stu-id="b71f4-122">The category of the container.</span></span> <span data-ttu-id="b71f4-123">Para obtener más información, vea los comentarios.</span><span class="sxs-lookup"><span data-stu-id="b71f4-123">See Remarks for more information.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b71f4-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b71f4-124">Return value</span></span>

<span data-ttu-id="b71f4-125">Referencia de ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="b71f4-125">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b71f4-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b71f4-126">Remarks</span></span>

<span data-ttu-id="b71f4-127">El índice de un contenedor se calcula a partir del orden Z de los contenedores, de delante hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="b71f4-127">The index of a container is calculated based on the z-order of containers from front to back.</span></span>
  
 <span data-ttu-id="b71f4-128">Las *categorías* son cadenas definidas por el usuario que puede usar para clasificar formas.</span><span class="sxs-lookup"><span data-stu-id="b71f4-128">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="b71f4-129">Las categorías se pueden definir en la celda User.msvShapeCategories, en la ShapeSheet de una forma.</span><span class="sxs-lookup"><span data-stu-id="b71f4-129">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="b71f4-130">Puede definir varias categorías para una forma si las separa con punto y coma.</span><span class="sxs-lookup"><span data-stu-id="b71f4-130">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  
<span data-ttu-id="b71f4-131">Si la forma no es miembro de un contenedor o si no hay un contenedor que concuerde tanto con la categoría como con el número de índice especificados, CONTAINERSHEETREF devuelve #REF!.</span><span class="sxs-lookup"><span data-stu-id="b71f4-131">If the shape is not a member of a container, or if there is no container that matches both the specified index number and the category, CONTAINERSHEETREF returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="b71f4-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b71f4-132">Example</span></span>

<span data-ttu-id="b71f4-133">CONTAINERSHEETREF (1)! Alto</span><span class="sxs-lookup"><span data-stu-id="b71f4-133">CONTAINERSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="b71f4-134">Devuelve el valor de la celda Height del contenedor que se encuentra más hacia delante en la página a la que pertenece la forma.</span><span class="sxs-lookup"><span data-stu-id="b71f4-134">Returns the value in the Height cell of the container that is most forward on the page to which the shape belongs.</span></span> 
  

