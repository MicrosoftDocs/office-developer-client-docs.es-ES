---
title: BKGPAGENAME (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
localization_priority: Normal
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: Devuelve un nombre de página de fondo como una cadena.
ms.openlocfilehash: 3b628315052117fe853c8f9c0fc36572de25d871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410318"
---
# <a name="bkgpagename-function"></a><span data-ttu-id="e5f34-103">Función BKGPAGENAME</span><span class="sxs-lookup"><span data-stu-id="e5f34-103">BKGPAGENAME Function</span></span>

<span data-ttu-id="e5f34-104">Devuelve un nombre de página de fondo como una cadena.</span><span class="sxs-lookup"><span data-stu-id="e5f34-104">Returns a background page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e5f34-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5f34-105">Syntax</span></span>

<span data-ttu-id="e5f34-106">BKGPAGENAME (\*\* *langID_opt* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e5f34-106">BKGPAGENAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e5f34-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5f34-107">Parameters</span></span>

|<span data-ttu-id="e5f34-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e5f34-108">**Name**</span></span>|<span data-ttu-id="e5f34-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e5f34-109">**Required/Optional**</span></span>|<span data-ttu-id="e5f34-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="e5f34-110">**Data Type**</span></span>|<span data-ttu-id="e5f34-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e5f34-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e5f34-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="e5f34-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="e5f34-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="e5f34-113">Optional</span></span>  <br/> |<span data-ttu-id="e5f34-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="e5f34-114">**Numeric**</span></span> <br/> |<span data-ttu-id="e5f34-p101">Se usa para especificar un idioma para la cadena devuelta por la función. Use 0 (valor predeterminado) para especificar el idioma local. Use 750 para especificar un idioma universal.</span><span class="sxs-lookup"><span data-stu-id="e5f34-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e5f34-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5f34-118">Return value</span></span>

<span data-ttu-id="e5f34-119">String</span><span class="sxs-lookup"><span data-stu-id="e5f34-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e5f34-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e5f34-120">Remarks</span></span>

<span data-ttu-id="e5f34-121">Si la página para la que usa la función no tiene una página de fondo, se devuelve la cadena " \< sin \> fondo".</span><span class="sxs-lookup"><span data-stu-id="e5f34-121">If the page for which you are using the function doesn't have a background page, the string "\<no background\>" is returned.</span></span> 
  
<span data-ttu-id="e5f34-122">Si el código de idioma indicado no es válido, se utiliza el idioma local.</span><span class="sxs-lookup"><span data-stu-id="e5f34-122">If you pass an illegal language code, the local language is used.</span></span> 
  

