---
title: MASTERNAME (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Devuelve el nombre de patrón de una hoja como una cadena o devuelve la cadena 'no master' si la hoja no tiene un patrón.
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414756"
---
# <a name="mastername-function"></a><span data-ttu-id="5002d-103">Función MASTERNAME</span><span class="sxs-lookup"><span data-stu-id="5002d-103">MASTERNAME Function</span></span>

<span data-ttu-id="5002d-104">Devuelve el nombre de patrón de una hoja como una cadena o devuelve la cadena " sin patrón " si la hoja \< \> no tiene un patrón.</span><span class="sxs-lookup"><span data-stu-id="5002d-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5002d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5002d-105">Syntax</span></span>

<span data-ttu-id="5002d-106">MASTERNAME ([ \*\* *langID_opt* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="5002d-106">MASTERNAME ([ \*\* *langID_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5002d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5002d-107">Parameters</span></span>

|<span data-ttu-id="5002d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5002d-108">**Name**</span></span>|<span data-ttu-id="5002d-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="5002d-109">**Required/Optional**</span></span>|<span data-ttu-id="5002d-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5002d-110">**Data Type**</span></span>|<span data-ttu-id="5002d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5002d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5002d-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="5002d-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="5002d-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="5002d-113">Optional</span></span>  <br/> |<span data-ttu-id="5002d-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="5002d-114">**Number**</span></span> <br/> |<span data-ttu-id="5002d-p101">Se usa para especificar un idioma para la cadena devuelta por la función. Use 0 (valor predeterminado) para especificar el idioma local. Use 750 para especificar un idioma universal.</span><span class="sxs-lookup"><span data-stu-id="5002d-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5002d-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5002d-118">Return value</span></span>

<span data-ttu-id="5002d-119">String</span><span class="sxs-lookup"><span data-stu-id="5002d-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5002d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5002d-120">Remarks</span></span>

<span data-ttu-id="5002d-121">Si el código de idioma indicado no es válido, se utiliza el idioma local.</span><span class="sxs-lookup"><span data-stu-id="5002d-121">If you pass an illegal language code, the local language is used.</span></span> 
  

