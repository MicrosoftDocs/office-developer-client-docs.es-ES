---
title: LOWER (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251459
localization_priority: Normal
ms.assetid: 1d198ea6-49e0-e462-b2cf-b65fbb920b55
description: Devuelve una cadena convertida a minúsculas.
ms.openlocfilehash: da626ee0bb0474fceafcf93ed5c835aacd0034fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822562"
---
# <a name="lower-function"></a><span data-ttu-id="58a61-103">Función LOWER</span><span class="sxs-lookup"><span data-stu-id="58a61-103">LOWER Function</span></span>

<span data-ttu-id="58a61-104">Devuelve una cadena convertida a minúsculas.</span><span class="sxs-lookup"><span data-stu-id="58a61-104">Returns a string converted to lowercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="58a61-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58a61-105">Syntax</span></span>

<span data-ttu-id="58a61-106">INFERIOR (** *expresión* **)</span><span class="sxs-lookup"><span data-stu-id="58a61-106">LOWER(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="58a61-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58a61-107">Parameters</span></span>

|<span data-ttu-id="58a61-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="58a61-108">**Name**</span></span>|<span data-ttu-id="58a61-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="58a61-109">**Required/Optional**</span></span>|<span data-ttu-id="58a61-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="58a61-110">**Data Type**</span></span>|<span data-ttu-id="58a61-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58a61-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="58a61-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="58a61-112">_expression_</span></span> <br/> |<span data-ttu-id="58a61-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="58a61-113">Required</span></span>  <br/> |<span data-ttu-id="58a61-114">**Varies**</span><span class="sxs-lookup"><span data-stu-id="58a61-114">**Varies**</span></span> <br/> | <span data-ttu-id="58a61-115">Cadena, referencia de celda o expresión; el resultado se convierte en una cadena cuyos caracteres se convierten en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="58a61-115">A string, a cell reference, or an expression; the result is converted to a string which is then converted to lowercase.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="58a61-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58a61-116">Return value</span></span>

<span data-ttu-id="58a61-117">String</span><span class="sxs-lookup"><span data-stu-id="58a61-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58a61-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58a61-118">Remarks</span></span>

<span data-ttu-id="58a61-119">La conversión de mayúsculas y minúsculas depende de la configuración regional especificada en la configuración actual del usuario.</span><span class="sxs-lookup"><span data-stu-id="58a61-119">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="58a61-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="58a61-120">Example</span></span>

<span data-ttu-id="58a61-121">LOWER("MAYÚSCULAS y minúsculas")</span><span class="sxs-lookup"><span data-stu-id="58a61-121">LOWER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="58a61-122">Devuelve "mayúsculas y minúsculas".</span><span class="sxs-lookup"><span data-stu-id="58a61-122">Returns "mixed case".</span></span> 
  

