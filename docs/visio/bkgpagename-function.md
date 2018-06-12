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
description: Devuelve un nombre de la página de fondo como una cadena.
ms.openlocfilehash: 290fa62242298b3c513bf2870df37204fab31bf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821659"
---
# <a name="bkgpagename-function"></a><span data-ttu-id="6f09a-103">BKGPAGENAME (función)</span><span class="sxs-lookup"><span data-stu-id="6f09a-103">BKGPAGENAME Function</span></span>

<span data-ttu-id="6f09a-104">Devuelve un nombre de la página de fondo como una cadena.</span><span class="sxs-lookup"><span data-stu-id="6f09a-104">Returns a background page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6f09a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f09a-105">Syntax</span></span>

<span data-ttu-id="6f09a-106">BKGPAGENAME (** *IdIdiomaOpc* **)</span><span class="sxs-lookup"><span data-stu-id="6f09a-106">BKGPAGENAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6f09a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f09a-107">Parameters</span></span>

|<span data-ttu-id="6f09a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6f09a-108">**Name**</span></span>|<span data-ttu-id="6f09a-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="6f09a-109">**Required/Optional**</span></span>|<span data-ttu-id="6f09a-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="6f09a-110">**Data Type**</span></span>|<span data-ttu-id="6f09a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f09a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6f09a-112">_IdIdiomaOpc_</span><span class="sxs-lookup"><span data-stu-id="6f09a-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="6f09a-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="6f09a-113">Optional</span></span>  <br/> |<span data-ttu-id="6f09a-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="6f09a-114">**Numeric**</span></span> <br/> |<span data-ttu-id="6f09a-p101">Se usa para especificar un idioma para la cadena devuelta por la función. Use 0 (valor predeterminado) para especificar el idioma local. Use 750 para especificar un idioma universal.</span><span class="sxs-lookup"><span data-stu-id="6f09a-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6f09a-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f09a-118">Return value</span></span>

<span data-ttu-id="6f09a-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="6f09a-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f09a-120">Notas</span><span class="sxs-lookup"><span data-stu-id="6f09a-120">Remarks</span></span>

<span data-ttu-id="6f09a-121">Si la página para la que se utiliza la función no tiene una página de fondo, la cadena "\<ningún fondo\>" se devuelve.</span><span class="sxs-lookup"><span data-stu-id="6f09a-121">If the page for which you are using the function doesn't have a background page, the string "\<no background\>" is returned.</span></span> 
  
<span data-ttu-id="6f09a-122">Si el código de idioma indicado no es válido, se utiliza el idioma local.</span><span class="sxs-lookup"><span data-stu-id="6f09a-122">If you pass an illegal language code, the local language is used.</span></span> 
  

