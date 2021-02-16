---
title: PAGENAME (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251577
localization_priority: Normal
ms.assetid: 12e45f46-e773-9445-4c7f-c726ab648671
description: Devuelve el nombre de página como una cadena.
ms.openlocfilehash: d5527bde58a68c96bd75773f3a0a8c30f64fa20d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438655"
---
# <a name="pagename-function"></a><span data-ttu-id="4ac45-103">Función PAGENAME</span><span class="sxs-lookup"><span data-stu-id="4ac45-103">PAGENAME Function</span></span>

<span data-ttu-id="4ac45-104">Devuelve el nombre de página como una cadena.</span><span class="sxs-lookup"><span data-stu-id="4ac45-104">Returns the page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4ac45-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ac45-105">Syntax</span></span>

<span data-ttu-id="4ac45-106">PAGENAME (\*\* *langID_opt* \*\* )</span><span class="sxs-lookup"><span data-stu-id="4ac45-106">PAGENAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4ac45-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ac45-107">Parameters</span></span>

|<span data-ttu-id="4ac45-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4ac45-108">**Name**</span></span>|<span data-ttu-id="4ac45-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="4ac45-109">**Required/Optional**</span></span>|<span data-ttu-id="4ac45-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4ac45-110">**Data Type**</span></span>|<span data-ttu-id="4ac45-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4ac45-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4ac45-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="4ac45-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="4ac45-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="4ac45-113">Optional</span></span>  <br/> |<span data-ttu-id="4ac45-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="4ac45-114">**Number**</span></span> <br/> |<span data-ttu-id="4ac45-p101">Se usa para especificar un idioma para la cadena devuelta por la función. Use 0 (valor predeterminado) para especificar el idioma local. Use 750 para especificar un idioma universal.</span><span class="sxs-lookup"><span data-stu-id="4ac45-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4ac45-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ac45-118">Return value</span></span>

<span data-ttu-id="4ac45-119">String</span><span class="sxs-lookup"><span data-stu-id="4ac45-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ac45-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ac45-120">Remarks</span></span>

<span data-ttu-id="4ac45-121">Si el código de idioma indicado no es válido, se utiliza el idioma local.</span><span class="sxs-lookup"><span data-stu-id="4ac45-121">If you pass an illegal language code, the local language is used.</span></span>
  

