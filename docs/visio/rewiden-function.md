---
title: REWIDEN (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
localization_priority: Normal
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: Convierte una fórmula que genera códigos de caracteres de 16 bits que son códigos ampliados de juego de caracteres de un byte o de varios bytes en una cadena de códigos de caracteres Unicode de 16 bits, utilizando los conjuntos de caracteres especificado.
ms.openlocfilehash: 66dc3e801585077a9521cd93f8ae78c47f8a746b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822993"
---
# <a name="rewiden-function"></a><span data-ttu-id="5c475-103">Función REWIDEN</span><span class="sxs-lookup"><span data-stu-id="5c475-103">REWIDEN Function</span></span>

<span data-ttu-id="5c475-104">Convierte una fórmula que genera códigos de caracteres de 16 bits que son códigos ampliados de juego de caracteres de un byte o de varios bytes en una cadena de códigos de caracteres Unicode de 16 bits, utilizando los conjuntos de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="5c475-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5c475-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c475-105">Syntax</span></span>

<span data-ttu-id="5c475-106">REWIDEN (** *juegoCarOrig* **, ** *juegoCarDest* **, ** *texto* **)</span><span class="sxs-lookup"><span data-stu-id="5c475-106">REWIDEN(** *srcCharSet* **, ** *dstCharSet* **, ** *text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5c475-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c475-107">Parameters</span></span>

|<span data-ttu-id="5c475-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5c475-108">**Name**</span></span>|<span data-ttu-id="5c475-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="5c475-109">**Required/Optional**</span></span>|<span data-ttu-id="5c475-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5c475-110">**Data Type**</span></span>|<span data-ttu-id="5c475-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c475-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5c475-112">_juegoCarOrig_</span><span class="sxs-lookup"><span data-stu-id="5c475-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="5c475-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5c475-113">Required</span></span>  <br/> |<span data-ttu-id="5c475-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5c475-114">**String**</span></span> <br/> |<span data-ttu-id="5c475-115">El juego de caracteres del documento de origen.</span><span class="sxs-lookup"><span data-stu-id="5c475-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="5c475-116">_juegoCarDest_</span><span class="sxs-lookup"><span data-stu-id="5c475-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="5c475-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5c475-117">Required</span></span>  <br/> |<span data-ttu-id="5c475-118">**String**</span><span class="sxs-lookup"><span data-stu-id="5c475-118">**String**</span></span> <br/> | <span data-ttu-id="5c475-119">El juego de caracteres del documento de destino.</span><span class="sxs-lookup"><span data-stu-id="5c475-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="5c475-120">_text_</span><span class="sxs-lookup"><span data-stu-id="5c475-120">_text_</span></span> <br/> |<span data-ttu-id="5c475-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5c475-121">Required</span></span>  <br/> |<span data-ttu-id="5c475-122">**String**</span><span class="sxs-lookup"><span data-stu-id="5c475-122">**String**</span></span> <br/> |<span data-ttu-id="5c475-123">El texto que se debe convertir.</span><span class="sxs-lookup"><span data-stu-id="5c475-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c475-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c475-124">Remarks</span></span>

<span data-ttu-id="5c475-p101">La función REWIDEN se usa en la conversión automática de documentos de Visio 2002 en documentos de Visio 2003 y no se recomienda ningún otro uso.</span><span class="sxs-lookup"><span data-stu-id="5c475-p101">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents. Other use is not recommended.</span></span>
  

