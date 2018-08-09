---
title: TRIM (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Quita todo el espacio del texto, excepto los espacios individuales entre palabras.
ms.openlocfilehash: b396572041e880451ceb1ec6f0508528c0807bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823450"
---
# <a name="trim-function"></a><span data-ttu-id="4d99e-103">Función TRIM</span><span class="sxs-lookup"><span data-stu-id="4d99e-103">TRIM Function</span></span>

<span data-ttu-id="4d99e-104">Quita todo el espacio del texto, excepto los espacios individuales entre palabras.</span><span class="sxs-lookup"><span data-stu-id="4d99e-104">Removes all space from text, except for single spaces between words.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4d99e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d99e-105">Syntax</span></span>

<span data-ttu-id="4d99e-106">TRIM (** *texto* **)</span><span class="sxs-lookup"><span data-stu-id="4d99e-106">TRIM (** *text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4d99e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d99e-107">Parameters</span></span>

|<span data-ttu-id="4d99e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4d99e-108">**Name**</span></span>|<span data-ttu-id="4d99e-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="4d99e-109">**Required/Optional**</span></span>|<span data-ttu-id="4d99e-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4d99e-110">**Data Type**</span></span>|<span data-ttu-id="4d99e-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4d99e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4d99e-112">_text_</span><span class="sxs-lookup"><span data-stu-id="4d99e-112">_text_</span></span> <br/> |<span data-ttu-id="4d99e-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4d99e-113">Required</span></span>  <br/> |<span data-ttu-id="4d99e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="4d99e-114">**String**</span></span> <br/> |<span data-ttu-id="4d99e-115">El texto cuyos espacios se desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="4d99e-115">The text from which you want to remove spaces.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4d99e-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d99e-116">Return value</span></span>

<span data-ttu-id="4d99e-117">String</span><span class="sxs-lookup"><span data-stu-id="4d99e-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4d99e-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d99e-118">Remarks</span></span>

<span data-ttu-id="4d99e-119">La función TRIM puede ser útil para tratar el texto proveniente de otra aplicación que presente un espaciado irregular.</span><span class="sxs-lookup"><span data-stu-id="4d99e-119">You can use the TRIM function on text that you have received from another application that may have irregular spacing.</span></span>
  
## <a name="example"></a><span data-ttu-id="4d99e-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d99e-120">Example</span></span>

<span data-ttu-id="4d99e-121">TRIM ("1 de enero de 2003")</span><span class="sxs-lookup"><span data-stu-id="4d99e-121">TRIM ("January 1, 2003 ")</span></span> 
  
<span data-ttu-id="4d99e-122">Devuelve "1 de enero, 2003".</span><span class="sxs-lookup"><span data-stu-id="4d99e-122">Returns "January 1, 2003".</span></span> 
  

