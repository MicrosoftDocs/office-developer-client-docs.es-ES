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
description: Convierte una fórmula que produce códigos de caracteres de 16 bits que son códigos de conjunto de caracteres de un byte o multibyte ampliados en una cadena de códigos de caracteres Unicode de 16 bits, utilizando los juegos de caracteres especificados.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326771"
---
# <a name="rewiden-function"></a><span data-ttu-id="ed5cc-103">Función REWIDEN</span><span class="sxs-lookup"><span data-stu-id="ed5cc-103">REWIDEN Function</span></span>

<span data-ttu-id="ed5cc-104">Convierte una fórmula que produce códigos de caracteres de 16 bits que son códigos de conjunto de caracteres de un byte o multibyte ampliados en una cadena de códigos de caracteres Unicode de 16 bits, utilizando los juegos de caracteres especificados.</span><span class="sxs-lookup"><span data-stu-id="ed5cc-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ed5cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed5cc-105">Syntax</span></span>

<span data-ttu-id="ed5cc-106">ReWIDEn (\* \* *srcCharSet* \* \*, \* \* *dstCharSet* \* \*, \* \* *Text* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ed5cc-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ed5cc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed5cc-107">Parameters</span></span>

|<span data-ttu-id="ed5cc-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ed5cc-108">**Name**</span></span>|<span data-ttu-id="ed5cc-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="ed5cc-109">**Required/Optional**</span></span>|<span data-ttu-id="ed5cc-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ed5cc-110">**Data Type**</span></span>|<span data-ttu-id="ed5cc-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ed5cc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ed5cc-112">_srcCharSet_</span><span class="sxs-lookup"><span data-stu-id="ed5cc-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="ed5cc-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ed5cc-113">Required</span></span>  <br/> |<span data-ttu-id="ed5cc-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ed5cc-114">**String**</span></span> <br/> |<span data-ttu-id="ed5cc-115">El juego de caracteres del documento de origen.</span><span class="sxs-lookup"><span data-stu-id="ed5cc-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="ed5cc-116">_dstCharSet_</span><span class="sxs-lookup"><span data-stu-id="ed5cc-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="ed5cc-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ed5cc-117">Required</span></span>  <br/> |<span data-ttu-id="ed5cc-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ed5cc-118">**String**</span></span> <br/> | <span data-ttu-id="ed5cc-119">El juego de caracteres del documento de destino.</span><span class="sxs-lookup"><span data-stu-id="ed5cc-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="ed5cc-120">_text_</span><span class="sxs-lookup"><span data-stu-id="ed5cc-120">_text_</span></span> <br/> |<span data-ttu-id="ed5cc-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ed5cc-121">Required</span></span>  <br/> |<span data-ttu-id="ed5cc-122">**String**</span><span class="sxs-lookup"><span data-stu-id="ed5cc-122">**String**</span></span> <br/> |<span data-ttu-id="ed5cc-123">El texto que se debe convertir.</span><span class="sxs-lookup"><span data-stu-id="ed5cc-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed5cc-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ed5cc-124">Remarks</span></span>

<span data-ttu-id="ed5cc-p101">La función REWIDEN se usa en la conversión automática de documentos de Visio 2002 en documentos de Visio 2003 y no se recomienda ningún otro uso.</span><span class="sxs-lookup"><span data-stu-id="ed5cc-p101">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents. Other use is not recommended.</span></span>
  

