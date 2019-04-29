---
title: Función LOC (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Toma un punto definido en las coordenadas locales de una forma y devuelve el punto equivalente expresado en las coordenadas locales de la forma asociada a la fórmula.
ms.openlocfilehash: 4728e5f8301c6ef10ddb0c14b6c0868a7a48b2a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422428"
---
# <a name="loc-function-visioshapesheet"></a><span data-ttu-id="10e06-103">Función LOC (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="10e06-103">LOC Function (VisioShapeSheet)</span></span>

<span data-ttu-id="10e06-104">Toma un punto definido en las coordenadas locales de una forma y devuelve el punto equivalente expresado en las coordenadas locales de la forma asociada a la fórmula.</span><span class="sxs-lookup"><span data-stu-id="10e06-104">Takes a point defined in one shape's local coordinates and returns the equivalent point expressed in the local coordinates of the shape associated with the formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="10e06-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10e06-105">Syntax</span></span>

<span data-ttu-id="10e06-106">LOC (\* \* *punto* \* \*)</span><span class="sxs-lookup"><span data-stu-id="10e06-106">LOC(\*\* *point* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="10e06-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10e06-107">Parameters</span></span>

|<span data-ttu-id="10e06-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="10e06-108">**Name**</span></span>|<span data-ttu-id="10e06-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="10e06-109">**Required/Optional**</span></span>|<span data-ttu-id="10e06-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="10e06-110">**Data Type**</span></span>|<span data-ttu-id="10e06-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="10e06-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="10e06-112">_indique_</span><span class="sxs-lookup"><span data-stu-id="10e06-112">_point_</span></span> <br/> |<span data-ttu-id="10e06-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="10e06-113">Required</span></span>  <br/> |<span data-ttu-id="10e06-114">**String**</span><span class="sxs-lookup"><span data-stu-id="10e06-114">**String**</span></span> <br/> | <span data-ttu-id="10e06-115">Un punto definido en una de las coordenadas locales de la forma.</span><span class="sxs-lookup"><span data-stu-id="10e06-115">A point defined in one shape's local coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="10e06-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10e06-116">Return value</span></span>

<span data-ttu-id="10e06-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="10e06-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="10e06-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="10e06-118">Remarks</span></span>

<span data-ttu-id="10e06-p101">Las coordenadas locales se miden desde la esquina inferior izquierda del rectángulo de selección de la forma. Ambas formas deben estar en la misma página.</span><span class="sxs-lookup"><span data-stu-id="10e06-p101">Local coordinates are measured from the lower-left corner of the shape's selection rectangle. Both shapes must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="10e06-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="10e06-121">Example</span></span>

<span data-ttu-id="10e06-122">LOC (PNT (hoja. 5! LocPinX, sheet. 5! LocPinY))</span><span class="sxs-lookup"><span data-stu-id="10e06-122">LOC(PNT(Sheet.5!LocPinX, Sheet.5!LocPinY))</span></span> 
  
<span data-ttu-id="10e06-p102">En esta expresión, PNT convierte un conjunto de coordenadas locales de Hoja.5 en un punto (Hoja.5 es otra forma que se encuentra en la misma página de dibujo). LOC convierte a continuación ese punto en un punto equivalente del sistema de coordenadas locales de la forma actual, en relación con la esquina inferior izquierda del rectángulo de selección de la forma actual.</span><span class="sxs-lookup"><span data-stu-id="10e06-p102">In this expression, PNT converts a set of local coordinates in Sheet.5 to a point. (Sheet.5 is another shape on the same drawing page.) LOC then converts that point to an equivalent point in the current shape's local coordinate system, relative to the lower-left corner of the selection rectangle of the current shape.</span></span> 
  
<span data-ttu-id="10e06-125">El número 5 de Hoja.5 es el número identificador de la forma, que se muestra en el cuadro de diálogo **Nombre de forma** (en la ficha **Programador**).</span><span class="sxs-lookup"><span data-stu-id="10e06-125">The 5 in Sheet.5 is the ID number for the shape, which is displayed in the **Shape Name** dialog box (**Developer** tab).</span></span> 
  

