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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327331"
---
# <a name="upper-function"></a><span data-ttu-id="1813d-103">Función UPPER</span><span class="sxs-lookup"><span data-stu-id="1813d-103">UPPER Function</span></span>

<span data-ttu-id="1813d-104">Devuelve una cadena convertida en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="1813d-104">Returns a string converted to uppercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1813d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1813d-105">Syntax</span></span>

<span data-ttu-id="1813d-106">UPPER (\* \* *expresión* \* \*)</span><span class="sxs-lookup"><span data-stu-id="1813d-106">UPPER(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1813d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1813d-107">Parameters</span></span>

|<span data-ttu-id="1813d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1813d-108">**Name**</span></span>|<span data-ttu-id="1813d-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="1813d-109">**Required/Optional**</span></span>|<span data-ttu-id="1813d-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="1813d-110">**Data Type**</span></span>|<span data-ttu-id="1813d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1813d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1813d-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="1813d-112">_expression_</span></span> <br/> |<span data-ttu-id="1813d-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1813d-113">Required</span></span>  <br/> |<span data-ttu-id="1813d-114">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="1813d-114">**Varies**</span></span> <br/> | <span data-ttu-id="1813d-115">Una cadena, referencia de celda o expresión; el resultado se convierte en una cadena cuyos caracteres se convierten en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="1813d-115">A string, a cell reference, or an expression; the result is converted to a string, which is then converted to uppercase.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1813d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1813d-116">Remarks</span></span>

<span data-ttu-id="1813d-117">La conversión de mayúsculas y minúsculas depende de la configuración regional especificada en la configuración actual del usuario.</span><span class="sxs-lookup"><span data-stu-id="1813d-117">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1813d-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1813d-118">Example</span></span>

<span data-ttu-id="1813d-119">UPPER("MAYÚSCULAS y minúsculas")</span><span class="sxs-lookup"><span data-stu-id="1813d-119">UPPER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="1813d-120">Devuelve "MAYÚSCULAS Y MINÚSCULAS".</span><span class="sxs-lookup"><span data-stu-id="1813d-120">Returns "MIXED CASE".</span></span> 
  

