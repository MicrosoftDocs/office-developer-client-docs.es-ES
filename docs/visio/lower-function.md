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
ms.openlocfilehash: 275e5cc40bed5c3ca7d6f40b0882f523334611c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421245"
---
# <a name="lower-function"></a><span data-ttu-id="ead25-103">Función LOWER</span><span class="sxs-lookup"><span data-stu-id="ead25-103">LOWER Function</span></span>

<span data-ttu-id="ead25-104">Devuelve una cadena convertida a minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ead25-104">Returns a string converted to lowercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ead25-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ead25-105">Syntax</span></span>

<span data-ttu-id="ead25-106">LOWER(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ead25-106">LOWER(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ead25-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ead25-107">Parameters</span></span>

|<span data-ttu-id="ead25-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ead25-108">**Name**</span></span>|<span data-ttu-id="ead25-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="ead25-109">**Required/Optional**</span></span>|<span data-ttu-id="ead25-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ead25-110">**Data Type**</span></span>|<span data-ttu-id="ead25-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ead25-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ead25-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="ead25-112">_expression_</span></span> <br/> |<span data-ttu-id="ead25-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ead25-113">Required</span></span>  <br/> |<span data-ttu-id="ead25-114">**Varía**</span><span class="sxs-lookup"><span data-stu-id="ead25-114">**Varies**</span></span> <br/> | <span data-ttu-id="ead25-115">Cadena, referencia de celda o expresión; el resultado se convierte en una cadena cuyos caracteres se convierten en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ead25-115">A string, a cell reference, or an expression; the result is converted to a string which is then converted to lowercase.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ead25-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ead25-116">Return value</span></span>

<span data-ttu-id="ead25-117">String</span><span class="sxs-lookup"><span data-stu-id="ead25-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ead25-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ead25-118">Remarks</span></span>

<span data-ttu-id="ead25-119">La conversión de mayúsculas y minúsculas depende de la configuración regional especificada en la configuración actual del usuario.</span><span class="sxs-lookup"><span data-stu-id="ead25-119">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ead25-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ead25-120">Example</span></span>

<span data-ttu-id="ead25-121">LOWER("MAYÚSCULAS y minúsculas")</span><span class="sxs-lookup"><span data-stu-id="ead25-121">LOWER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="ead25-122">Devuelve "mayúsculas y minúsculas".</span><span class="sxs-lookup"><span data-stu-id="ead25-122">Returns "mixed case".</span></span> 
  

