---
title: NAME (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251580
localization_priority: Normal
ms.assetid: 1ca67a09-9df2-37f5-b269-e761d76bb011
description: Devuelve el nombre de una hoja como una cadena.
ms.openlocfilehash: 7d0a4e9f3c5f70be07e9cc5691f52afcbc7bea68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416800"
---
# <a name="name-function"></a><span data-ttu-id="e94bb-103">Función NAME</span><span class="sxs-lookup"><span data-stu-id="e94bb-103">NAME Function</span></span>

<span data-ttu-id="e94bb-104">Devuelve el nombre de una hoja como una cadena.</span><span class="sxs-lookup"><span data-stu-id="e94bb-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e94bb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e94bb-105">Syntax</span></span>

<span data-ttu-id="e94bb-106">NAME (\*\* *langID_opt* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e94bb-106">NAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e94bb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e94bb-107">Parameters</span></span>

|<span data-ttu-id="e94bb-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e94bb-108">**Name**</span></span>|<span data-ttu-id="e94bb-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e94bb-109">**Required/Optional**</span></span>|<span data-ttu-id="e94bb-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="e94bb-110">**Data Type**</span></span>|<span data-ttu-id="e94bb-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e94bb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e94bb-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="e94bb-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="e94bb-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="e94bb-113">Optional</span></span>  <br/> |<span data-ttu-id="e94bb-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="e94bb-114">**Number**</span></span> <br/> |<span data-ttu-id="e94bb-p101">Se usa para especificar un idioma para la cadena devuelta por la función. Use 0 (valor predeterminado) para especificar el idioma local. Use 750 para especificar un idioma universal.</span><span class="sxs-lookup"><span data-stu-id="e94bb-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e94bb-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e94bb-118">Return value</span></span>

<span data-ttu-id="e94bb-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="e94bb-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e94bb-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e94bb-120">Remarks</span></span>

<span data-ttu-id="e94bb-121">Si el código de idioma indicado no es válido, se utiliza el idioma local.</span><span class="sxs-lookup"><span data-stu-id="e94bb-121">If you pass an illegal language code, the local language is used.</span></span> 
  

