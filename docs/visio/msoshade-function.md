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
# <a name="msoshade-function"></a><span data-ttu-id="faa0e-103">Función MSOSHADE</span><span class="sxs-lookup"><span data-stu-id="faa0e-103">MSOSHADE Function</span></span>

<span data-ttu-id="faa0e-104">Modifica el color disminuyendo su luminosidad en el porcentaje especificado.</span><span class="sxs-lookup"><span data-stu-id="faa0e-104">Modifies the color by decreasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="faa0e-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="faa0e-105">Version Information</span></span>

<span data-ttu-id="faa0e-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="faa0e-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="faa0e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="faa0e-107">Syntax</span></span>

<span data-ttu-id="faa0e-108">MSOSHADE(\*\* *color* \*\*, \*\* *-deltaLum* \*\* )</span><span class="sxs-lookup"><span data-stu-id="faa0e-108">MSOSHADE(\*\* *color* \*\*, \*\* *-deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="faa0e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="faa0e-109">Parameters</span></span>

|<span data-ttu-id="faa0e-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="faa0e-110">**Name**</span></span>|<span data-ttu-id="faa0e-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="faa0e-111">**Required/Optional**</span></span>|<span data-ttu-id="faa0e-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="faa0e-112">**Data Type**</span></span>|<span data-ttu-id="faa0e-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="faa0e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="faa0e-114">_color_</span><span class="sxs-lookup"><span data-stu-id="faa0e-114">_color_</span></span> <br/> |<span data-ttu-id="faa0e-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="faa0e-115">Required</span></span>  <br/> |<span data-ttu-id="faa0e-116">**RVA**</span><span class="sxs-lookup"><span data-stu-id="faa0e-116">**RGB**</span></span> <br/> |<span data-ttu-id="faa0e-117">Valor de color RGB estándar (rojo, verde, azul) o referencia a un color.</span><span class="sxs-lookup"><span data-stu-id="faa0e-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="faa0e-118">_-deltaLum_</span><span class="sxs-lookup"><span data-stu-id="faa0e-118">_-deltaLum_</span></span> <br/> |<span data-ttu-id="faa0e-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="faa0e-119">Required</span></span>  <br/> |<span data-ttu-id="faa0e-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="faa0e-120">**Integer**</span></span> <br/> |<span data-ttu-id="faa0e-121">El porcentaje cambia hacia blanco (-100%) o negro (100%) del valor  _de_ color.</span><span class="sxs-lookup"><span data-stu-id="faa0e-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="faa0e-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="faa0e-122">Remarks</span></span>

<span data-ttu-id="faa0e-123">Cuanto más cerca  _esté el valor_ de color a blanco o negro, menor será el cambio a la sombra que produce un valor  _-deltaLum_ específico.</span><span class="sxs-lookup"><span data-stu-id="faa0e-123">The closer the  _color_ value is to white or black, the smaller the change to the shade that is produced by a specific  _-deltaLum_ value.</span></span> 
  

