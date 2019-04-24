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
description: Devuelve el nombre del patrón de una hoja como una cadena, o devuelve la cadena "sin patrón" si la hoja no tiene un patrón.
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341800"
---
# <a name="mastername-function"></a><span data-ttu-id="f9e64-103">Función MASTERNAME</span><span class="sxs-lookup"><span data-stu-id="f9e64-103">MASTERNAME Function</span></span>

<span data-ttu-id="f9e64-104">Devuelve el nombre del patrón de una hoja como una cadena o devuelve la cadena\<"sin\>patrón" si la hoja no tiene un patrón.</span><span class="sxs-lookup"><span data-stu-id="f9e64-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f9e64-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9e64-105">Syntax</span></span>

<span data-ttu-id="f9e64-106">MASTERNAME ([\* \* *ididiomaopc* \* \*])</span><span class="sxs-lookup"><span data-stu-id="f9e64-106">MASTERNAME ([ \*\* *langID_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f9e64-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9e64-107">Parameters</span></span>

|<span data-ttu-id="f9e64-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f9e64-108">**Name**</span></span>|<span data-ttu-id="f9e64-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="f9e64-109">**Required/Optional**</span></span>|<span data-ttu-id="f9e64-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="f9e64-110">**Data Type**</span></span>|<span data-ttu-id="f9e64-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f9e64-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f9e64-112">_Ididiomaopc_</span><span class="sxs-lookup"><span data-stu-id="f9e64-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="f9e64-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="f9e64-113">Optional</span></span>  <br/> |<span data-ttu-id="f9e64-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="f9e64-114">**Number**</span></span> <br/> |<span data-ttu-id="f9e64-p101">Se usa para especificar un idioma para la cadena devuelta por la función. Use 0 (valor predeterminado) para especificar el idioma local. Use 750 para especificar un idioma universal.</span><span class="sxs-lookup"><span data-stu-id="f9e64-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f9e64-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9e64-118">Return value</span></span>

<span data-ttu-id="f9e64-119">String</span><span class="sxs-lookup"><span data-stu-id="f9e64-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f9e64-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9e64-120">Remarks</span></span>

<span data-ttu-id="f9e64-121">Si el código de idioma indicado no es válido, se utiliza el idioma local.</span><span class="sxs-lookup"><span data-stu-id="f9e64-121">If you pass an illegal language code, the local language is used.</span></span> 
  

