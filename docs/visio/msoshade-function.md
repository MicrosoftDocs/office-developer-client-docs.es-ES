---
title: MSOSHADE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifica el color disminuyendo su luminosidad en el porcentaje especificado.
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414497"
---
# <a name="msoshade-function"></a><span data-ttu-id="18fcd-103">Función MSOSHADE</span><span class="sxs-lookup"><span data-stu-id="18fcd-103">MSOSHADE Function</span></span>

<span data-ttu-id="18fcd-104">Modifica el color disminuyendo su luminosidad en el porcentaje especificado.</span><span class="sxs-lookup"><span data-stu-id="18fcd-104">Modifies the color by decreasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="18fcd-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="18fcd-105">Version Information</span></span>

<span data-ttu-id="18fcd-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="18fcd-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="18fcd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18fcd-107">Syntax</span></span>

<span data-ttu-id="18fcd-108">MSOSHADE (\* \* *color* \* \*, \* \* *-deltaLum* \* \*)</span><span class="sxs-lookup"><span data-stu-id="18fcd-108">MSOSHADE(\*\* *color* \*\*, \*\* *-deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="18fcd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18fcd-109">Parameters</span></span>

|<span data-ttu-id="18fcd-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="18fcd-110">**Name**</span></span>|<span data-ttu-id="18fcd-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="18fcd-111">**Required/Optional**</span></span>|<span data-ttu-id="18fcd-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="18fcd-112">**Data Type**</span></span>|<span data-ttu-id="18fcd-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18fcd-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="18fcd-114">_color_</span><span class="sxs-lookup"><span data-stu-id="18fcd-114">_color_</span></span> <br/> |<span data-ttu-id="18fcd-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="18fcd-115">Required</span></span>  <br/> |<span data-ttu-id="18fcd-116">**RVA**</span><span class="sxs-lookup"><span data-stu-id="18fcd-116">**RGB**</span></span> <br/> |<span data-ttu-id="18fcd-117">Valor de color RGB estándar (rojo, verde, azul) o referencia a un color.</span><span class="sxs-lookup"><span data-stu-id="18fcd-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="18fcd-118">_-deltaLum_</span><span class="sxs-lookup"><span data-stu-id="18fcd-118">_-deltaLum_</span></span> <br/> |<span data-ttu-id="18fcd-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="18fcd-119">Required</span></span>  <br/> |<span data-ttu-id="18fcd-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="18fcd-120">**Integer**</span></span> <br/> |<span data-ttu-id="18fcd-121">El cambio porcentual hacia el blanco (-100%) o negro (100%) del valor de _color_ .</span><span class="sxs-lookup"><span data-stu-id="18fcd-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18fcd-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18fcd-122">Remarks</span></span>

<span data-ttu-id="18fcd-123">Cuanto más se aproxime el valor de _color_ a blanco o negro, menor será el cambio de la sombra producido por un valor _de deltaLum_ específico.</span><span class="sxs-lookup"><span data-stu-id="18fcd-123">The closer the  _color_ value is to white or black, the smaller the change to the shade that is produced by a specific  _-deltaLum_ value.</span></span> 
  

