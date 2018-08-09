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
description: Devuelve el nombre del patrón de una hoja como una cadena, o no devuelve la cadena 'ningún patrón' Si la hoja no tiene un patrón.
ms.openlocfilehash: c1d5891fba0f967cde4a4e9ca58d07f87239f0b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822587"
---
# <a name="mastername-function"></a><span data-ttu-id="d6bf6-103">Función MASTERNAME</span><span class="sxs-lookup"><span data-stu-id="d6bf6-103">MASTERNAME Function</span></span>

<span data-ttu-id="d6bf6-104">Devuelve el nombre del patrón de una hoja como una cadena, o devuelve la cadena "\<ningún patrón\>" si la hoja no tiene un patrón.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d6bf6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6bf6-105">Syntax</span></span>

<span data-ttu-id="d6bf6-106">MASTERNAME ([** *IdIdiomaOpc* **])</span><span class="sxs-lookup"><span data-stu-id="d6bf6-106">MASTERNAME ([ ** *langID_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d6bf6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6bf6-107">Parameters</span></span>

|<span data-ttu-id="d6bf6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d6bf6-108">**Name**</span></span>|<span data-ttu-id="d6bf6-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="d6bf6-109">**Required/Optional**</span></span>|<span data-ttu-id="d6bf6-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="d6bf6-110">**Data Type**</span></span>|<span data-ttu-id="d6bf6-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d6bf6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d6bf6-112">_IdIdiomaOpc_</span><span class="sxs-lookup"><span data-stu-id="d6bf6-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="d6bf6-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="d6bf6-113">Optional</span></span>  <br/> |<span data-ttu-id="d6bf6-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="d6bf6-114">**Number**</span></span> <br/> |<span data-ttu-id="d6bf6-p101">Se usa para especificar un idioma para la cadena devuelta por la función. Use 0 (valor predeterminado) para especificar el idioma local. Use 750 para especificar un idioma universal.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d6bf6-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6bf6-118">Return value</span></span>

<span data-ttu-id="d6bf6-119">String</span><span class="sxs-lookup"><span data-stu-id="d6bf6-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d6bf6-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6bf6-120">Remarks</span></span>

<span data-ttu-id="d6bf6-121">Si el código de idioma indicado no es válido, se utiliza el idioma local.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-121">If you pass an illegal language code, the local language is used.</span></span> 
  

