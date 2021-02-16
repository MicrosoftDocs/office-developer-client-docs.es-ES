---
title: Función REPLACE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Reemplaza parte de una cadena de texto por otra cadena, de acuerdo con el número de caracteres especificado.
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414357"
---
# <a name="replace-function-visioshapesheet"></a><span data-ttu-id="53f89-103">Función REPLACE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="53f89-103">REPLACE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="53f89-104">Reemplaza parte de una cadena de texto por otra cadena, de acuerdo con el número de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="53f89-104">Replaces part of a text string, based on the number of characters you specify, with a different text string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="53f89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53f89-105">Syntax</span></span>

<span data-ttu-id="53f89-106">REPLACE (\*\* *old_text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\*, \*\* *new_text* \*\* )</span><span class="sxs-lookup"><span data-stu-id="53f89-106">REPLACE (\*\* *old_text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\*, \*\* *new_text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="53f89-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53f89-107">Parameters</span></span>

|<span data-ttu-id="53f89-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="53f89-108">**Name**</span></span>|<span data-ttu-id="53f89-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="53f89-109">**Required/Optional**</span></span>|<span data-ttu-id="53f89-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="53f89-110">**Data Type**</span></span>|<span data-ttu-id="53f89-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53f89-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="53f89-112">_old_text_</span><span class="sxs-lookup"><span data-stu-id="53f89-112">_old_text_</span></span> <br/> |<span data-ttu-id="53f89-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="53f89-113">Required</span></span>  <br/> |<span data-ttu-id="53f89-114">**String**</span><span class="sxs-lookup"><span data-stu-id="53f89-114">**String**</span></span> <br/> |<span data-ttu-id="53f89-115">El texto en el que desea reemplazar algunos caracteres.</span><span class="sxs-lookup"><span data-stu-id="53f89-115">The text in which you want to replace some characters.</span></span>  <br/> |
| <span data-ttu-id="53f89-116">_start_num_</span><span class="sxs-lookup"><span data-stu-id="53f89-116">_start_num_</span></span> <br/> |<span data-ttu-id="53f89-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="53f89-117">Required</span></span>  <br/> |<span data-ttu-id="53f89-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="53f89-118">**Number**</span></span> <br/> |<span data-ttu-id="53f89-119">La posición del carácter en  _old_text_ que desea reemplazar por  _new_text_.</span><span class="sxs-lookup"><span data-stu-id="53f89-119">The position of the character in  _old_text_ that you want to replace with  _new_text_.</span></span> <span data-ttu-id="53f89-120">El primer carácter de la cadena ocupa la posición 1.</span><span class="sxs-lookup"><span data-stu-id="53f89-120">The first character in the string is position 1.</span></span>  <br/> |
| <span data-ttu-id="53f89-121">_num_chars_</span><span class="sxs-lookup"><span data-stu-id="53f89-121">_num_chars_</span></span> <br/> |<span data-ttu-id="53f89-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="53f89-122">Required</span></span>  <br/> |<span data-ttu-id="53f89-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="53f89-123">**Number**</span></span> <br/> |<span data-ttu-id="53f89-124">El número de caracteres  _old_text_ caracteres que desea reemplazar</span><span class="sxs-lookup"><span data-stu-id="53f89-124">The number of characters in  _old_text_ that you want to replace</span></span>  <br/> |
| <span data-ttu-id="53f89-125">_new_text_</span><span class="sxs-lookup"><span data-stu-id="53f89-125">_new_text_</span></span> <br/> |<span data-ttu-id="53f89-126">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="53f89-126">Required</span></span>  <br/> |<span data-ttu-id="53f89-127">**String**</span><span class="sxs-lookup"><span data-stu-id="53f89-127">**String**</span></span> <br/> |<span data-ttu-id="53f89-128">Texto que reemplazará los caracteres de  _old_text_.</span><span class="sxs-lookup"><span data-stu-id="53f89-128">The text that will replace characters in  _old_text_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="53f89-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53f89-129">Return value</span></span>

<span data-ttu-id="53f89-130">String</span><span class="sxs-lookup"><span data-stu-id="53f89-130">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="53f89-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53f89-131">Remarks</span></span>

<span data-ttu-id="53f89-p102">Utilice esta función cuando desee reemplazar texto que aparezca en una ubicación concreta de una cadena de texto. Si desea reemplazar un texto específico dentro de una cadena de texto, recurra a la función SUBSTITUTE.</span><span class="sxs-lookup"><span data-stu-id="53f89-p102">Use the REPLACE function when you want to replace text that occurs in a specific location in a text string. If you want to replace specific text in a text string, use the SUBSTITUTE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="53f89-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53f89-134">Example</span></span>

<span data-ttu-id="53f89-135">REPLACE ("01/03/2002",9,2,"03")</span><span class="sxs-lookup"><span data-stu-id="53f89-135">REPLACE ("01/03/2002",9,2,"03")</span></span> 
  
<span data-ttu-id="53f89-136">Devuelve 01/03/2003.</span><span class="sxs-lookup"><span data-stu-id="53f89-136">Returns 01/03/2003.</span></span> 
  

