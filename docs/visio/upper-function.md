---
title: UPPER (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251509
localization_priority: Normal
ms.assetid: ef94ee0f-dbb8-a2e1-1805-8a6609830d2a
description: Devuelve una cadena convertida en mayúsculas.
ms.openlocfilehash: b88958526bfb5e08839077217759f7ffb50151b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415148"
---
# <a name="upper-function"></a><span data-ttu-id="2e141-103">Función UPPER</span><span class="sxs-lookup"><span data-stu-id="2e141-103">UPPER Function</span></span>

<span data-ttu-id="2e141-104">Devuelve una cadena convertida en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="2e141-104">Returns a string converted to uppercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2e141-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e141-105">Syntax</span></span>

<span data-ttu-id="2e141-106">UPPER(\*\* *expresión* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2e141-106">UPPER(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2e141-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e141-107">Parameters</span></span>

|<span data-ttu-id="2e141-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2e141-108">**Name**</span></span>|<span data-ttu-id="2e141-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="2e141-109">**Required/Optional**</span></span>|<span data-ttu-id="2e141-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2e141-110">**Data Type**</span></span>|<span data-ttu-id="2e141-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e141-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2e141-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="2e141-112">_expression_</span></span> <br/> |<span data-ttu-id="2e141-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2e141-113">Required</span></span>  <br/> |<span data-ttu-id="2e141-114">**Varía**</span><span class="sxs-lookup"><span data-stu-id="2e141-114">**Varies**</span></span> <br/> | <span data-ttu-id="2e141-115">Una cadena, referencia de celda o expresión; el resultado se convierte en una cadena cuyos caracteres se convierten en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="2e141-115">A string, a cell reference, or an expression; the result is converted to a string, which is then converted to uppercase.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e141-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e141-116">Remarks</span></span>

<span data-ttu-id="2e141-117">La conversión de mayúsculas y minúsculas depende de la configuración regional especificada en la configuración actual del usuario.</span><span class="sxs-lookup"><span data-stu-id="2e141-117">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2e141-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2e141-118">Example</span></span>

<span data-ttu-id="2e141-119">UPPER("MAYÚSCULAS y minúsculas")</span><span class="sxs-lookup"><span data-stu-id="2e141-119">UPPER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="2e141-120">Devuelve "MAYÚSCULAS Y MINÚSCULAS".</span><span class="sxs-lookup"><span data-stu-id="2e141-120">Returns "MIXED CASE".</span></span> 
  

