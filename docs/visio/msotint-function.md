---
title: MSOTINT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Modifica el color aumentando su luminosidad en el porcentaje especificado.
ms.openlocfilehash: d63b90d0cd6fcb35e23a8efa4ca9e13e2838bc21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335199"
---
# <a name="msotint-function"></a><span data-ttu-id="99839-103">Función MSOTINT</span><span class="sxs-lookup"><span data-stu-id="99839-103">MSOTINT Function</span></span>

<span data-ttu-id="99839-104">Modifica el color aumentando su luminosidad en el porcentaje especificado.</span><span class="sxs-lookup"><span data-stu-id="99839-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="99839-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="99839-105">Version Information</span></span>

<span data-ttu-id="99839-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="99839-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="99839-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99839-107">Syntax</span></span>

<span data-ttu-id="99839-108">MSOTINT (\* \* *color* \* \*, \* \* *deltaLum* \* \*)</span><span class="sxs-lookup"><span data-stu-id="99839-108">MSOTINT(\*\* *color* \*\*, \*\* *deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="99839-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99839-109">Parameters</span></span>

|<span data-ttu-id="99839-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="99839-110">**Name**</span></span>|<span data-ttu-id="99839-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="99839-111">**Required/Optional**</span></span>|<span data-ttu-id="99839-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="99839-112">**Data Type**</span></span>|<span data-ttu-id="99839-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99839-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="99839-114">_color_</span><span class="sxs-lookup"><span data-stu-id="99839-114">_color_</span></span> <br/> |<span data-ttu-id="99839-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="99839-115">Required</span></span>  <br/> |<span data-ttu-id="99839-116">**RVA**</span><span class="sxs-lookup"><span data-stu-id="99839-116">**RGB**</span></span> <br/> |<span data-ttu-id="99839-117">Valor de color RGB estándar (rojo, verde, azul) o referencia a un color.</span><span class="sxs-lookup"><span data-stu-id="99839-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="99839-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="99839-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="99839-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="99839-119">Required</span></span>  <br/> |<span data-ttu-id="99839-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="99839-120">**Integer**</span></span> <br/> |<span data-ttu-id="99839-121">El cambio porcentual hacia el blanco (-100%) o negro (100%) del valor de _color_ .</span><span class="sxs-lookup"><span data-stu-id="99839-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99839-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99839-122">Remarks</span></span>

<span data-ttu-id="99839-123">Cuanto más se aproxime el valor de _color_ a blanco o negro, menor será el cambio en el tinte generado por un valor de _deltaLum_ específico.</span><span class="sxs-lookup"><span data-stu-id="99839-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  

