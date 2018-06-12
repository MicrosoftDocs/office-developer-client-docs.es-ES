---
title: MSOSHADE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifica el color disminuyendo su luminosidad en el porcentaje especificado.
ms.openlocfilehash: f5f6eb0b6009473dcec017e951cca2f90b6c4d55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822665"
---
# <a name="msoshade-function"></a><span data-ttu-id="61a10-103">MSOSHADE (función)</span><span class="sxs-lookup"><span data-stu-id="61a10-103">MSOSHADE Function</span></span>

<span data-ttu-id="61a10-104">Modifica el color disminuyendo su luminosidad en el porcentaje especificado.</span><span class="sxs-lookup"><span data-stu-id="61a10-104">Modifies the color by decreasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="61a10-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="61a10-105">Version Information</span></span>

<span data-ttu-id="61a10-106">Versión agregada: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="61a10-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="61a10-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61a10-107">Syntax</span></span>

<span data-ttu-id="61a10-108">MSOSHADE (** *color* **, ** *- deltaLum* **)</span><span class="sxs-lookup"><span data-stu-id="61a10-108">MSOSHADE(** *color* **, ** *-deltaLum* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="61a10-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61a10-109">Parameters</span></span>

|<span data-ttu-id="61a10-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="61a10-110">**Name**</span></span>|<span data-ttu-id="61a10-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="61a10-111">**Required/Optional**</span></span>|<span data-ttu-id="61a10-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="61a10-112">**Data Type**</span></span>|<span data-ttu-id="61a10-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="61a10-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="61a10-114">_color_</span><span class="sxs-lookup"><span data-stu-id="61a10-114">_color_</span></span> <br/> |<span data-ttu-id="61a10-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="61a10-115">Required</span></span>  <br/> |<span data-ttu-id="61a10-116">**RVA**</span><span class="sxs-lookup"><span data-stu-id="61a10-116">**RGB**</span></span> <br/> |<span data-ttu-id="61a10-117">Valor de color RGB estándar (rojo, verde, azul) o referencia a un color.</span><span class="sxs-lookup"><span data-stu-id="61a10-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="61a10-118">_-deltaLum_</span><span class="sxs-lookup"><span data-stu-id="61a10-118">_-deltaLum_</span></span> <br/> |<span data-ttu-id="61a10-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="61a10-119">Required</span></span>  <br/> |<span data-ttu-id="61a10-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="61a10-120">**Integer**</span></span> <br/> |<span data-ttu-id="61a10-121">El cambio de porcentaje hacia blanco (-100%) o negro (100%) desde el valor de _color_ .</span><span class="sxs-lookup"><span data-stu-id="61a10-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61a10-122">Notas</span><span class="sxs-lookup"><span data-stu-id="61a10-122">Remarks</span></span>

<span data-ttu-id="61a10-123">Cuanto más se aproxime el valor de _color_ blanco o negro, menor será el cambio a la sombra que es generada por un valor específico de _-deltaLum_ .</span><span class="sxs-lookup"><span data-stu-id="61a10-123">The closer the  _color_ value is to white or black, the smaller the change to the shade that is produced by a specific  _-deltaLum_ value.</span></span> 
  

