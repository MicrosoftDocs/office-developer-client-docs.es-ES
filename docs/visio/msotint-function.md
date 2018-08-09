---
title: MSOTINT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Modifica el color aumentando su luminosidad en el porcentaje especificado.
ms.openlocfilehash: 50e81b5202174c61905d3914c50feddcb05a91cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822694"
---
# <a name="msotint-function"></a><span data-ttu-id="d3cfe-103">Función MSOTINT</span><span class="sxs-lookup"><span data-stu-id="d3cfe-103">MSOTINT Function</span></span>

<span data-ttu-id="d3cfe-104">Modifica el color aumentando su luminosidad en el porcentaje especificado.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="d3cfe-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="d3cfe-105">Version Information</span></span>

<span data-ttu-id="d3cfe-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="d3cfe-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d3cfe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3cfe-107">Syntax</span></span>

<span data-ttu-id="d3cfe-108">MSOTINT (** *color* **, ** *deltaLum* **)</span><span class="sxs-lookup"><span data-stu-id="d3cfe-108">MSOTINT(** *color* **, ** *deltaLum* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d3cfe-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3cfe-109">Parameters</span></span>

|<span data-ttu-id="d3cfe-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="d3cfe-110">**Name**</span></span>|<span data-ttu-id="d3cfe-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="d3cfe-111">**Required/Optional**</span></span>|<span data-ttu-id="d3cfe-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="d3cfe-112">**Data Type**</span></span>|<span data-ttu-id="d3cfe-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d3cfe-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d3cfe-114">_color_</span><span class="sxs-lookup"><span data-stu-id="d3cfe-114">_color_</span></span> <br/> |<span data-ttu-id="d3cfe-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d3cfe-115">Required</span></span>  <br/> |<span data-ttu-id="d3cfe-116">**RVA**</span><span class="sxs-lookup"><span data-stu-id="d3cfe-116">**RGB**</span></span> <br/> |<span data-ttu-id="d3cfe-117">Valor de color RGB estándar (rojo, verde, azul) o referencia a un color.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="d3cfe-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="d3cfe-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="d3cfe-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d3cfe-119">Required</span></span>  <br/> |<span data-ttu-id="d3cfe-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="d3cfe-120">**Integer**</span></span> <br/> |<span data-ttu-id="d3cfe-121">El cambio de porcentaje hacia blanco (-100%) o negro (100%) desde el valor de _color_ .</span><span class="sxs-lookup"><span data-stu-id="d3cfe-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3cfe-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d3cfe-122">Remarks</span></span>

<span data-ttu-id="d3cfe-123">Cuanto más se aproxime el valor de _color_ blanco o negro, menor será el cambio al tono que es generada por un valor específico _deltaLum_ .</span><span class="sxs-lookup"><span data-stu-id="d3cfe-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  

