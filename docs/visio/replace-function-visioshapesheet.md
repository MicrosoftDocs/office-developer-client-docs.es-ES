---
title: Reemplace la función (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Reemplaza parte de una cadena de texto por otra cadena, de acuerdo con el número de caracteres especificado.
ms.openlocfilehash: 4112339d772248ac033674808d97c3f9c55b6f0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822946"
---
# <a name="replace-function-visioshapesheet"></a><span data-ttu-id="ba2ff-103">Reemplace la función (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="ba2ff-103">REPLACE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="ba2ff-104">Reemplaza parte de una cadena de texto por otra cadena, de acuerdo con el número de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-104">Replaces part of a text string, based on the number of characters you specify, with a different text string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ba2ff-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba2ff-105">Syntax</span></span>

<span data-ttu-id="ba2ff-106">Reemplazar (** *texto_anterior* **, ** *número_inicio* **, ** *número_caracteres* **, ** *texto_nuevo* **)</span><span class="sxs-lookup"><span data-stu-id="ba2ff-106">REPLACE (** *old_text* **, ** *start_num* **, ** *num_chars* **, ** *new_text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ba2ff-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba2ff-107">Parameters</span></span>

|<span data-ttu-id="ba2ff-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ba2ff-108">**Name**</span></span>|<span data-ttu-id="ba2ff-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="ba2ff-109">**Required/Optional**</span></span>|<span data-ttu-id="ba2ff-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ba2ff-110">**Data Type**</span></span>|<span data-ttu-id="ba2ff-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba2ff-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ba2ff-112">_texto original_</span><span class="sxs-lookup"><span data-stu-id="ba2ff-112">_old_text_</span></span> <br/> |<span data-ttu-id="ba2ff-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ba2ff-113">Required</span></span>  <br/> |<span data-ttu-id="ba2ff-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ba2ff-114">**String**</span></span> <br/> |<span data-ttu-id="ba2ff-115">El texto en el que desea reemplazar algunos caracteres.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-115">The text in which you want to replace some characters.</span></span>  <br/> |
| <span data-ttu-id="ba2ff-116">_número inicial_</span><span class="sxs-lookup"><span data-stu-id="ba2ff-116">_start_num_</span></span> <br/> |<span data-ttu-id="ba2ff-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ba2ff-117">Required</span></span>  <br/> |<span data-ttu-id="ba2ff-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="ba2ff-118">**Number**</span></span> <br/> |<span data-ttu-id="ba2ff-119">La posición del carácter en _texto_anterior_ que se desea reemplazar por _texto_nuevo_.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-119">The position of the character in  _old_text_ that you want to replace with  _new_text_.</span></span> <span data-ttu-id="ba2ff-120">El primer carácter de la cadena es la posición 1.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-120">The first character in the string is position 1.</span></span>  <br/> |
| <span data-ttu-id="ba2ff-121">_número_caracteres_</span><span class="sxs-lookup"><span data-stu-id="ba2ff-121">_num_chars_</span></span> <br/> |<span data-ttu-id="ba2ff-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ba2ff-122">Required</span></span>  <br/> |<span data-ttu-id="ba2ff-123">**Número**</span><span class="sxs-lookup"><span data-stu-id="ba2ff-123">**Number**</span></span> <br/> |<span data-ttu-id="ba2ff-124">El número de caracteres en _texto_anterior_ que se desea reemplazar</span><span class="sxs-lookup"><span data-stu-id="ba2ff-124">The number of characters in  _old_text_ that you want to replace</span></span>  <br/> |
| <span data-ttu-id="ba2ff-125">_texto_nuevo_</span><span class="sxs-lookup"><span data-stu-id="ba2ff-125">_new_text_</span></span> <br/> |<span data-ttu-id="ba2ff-126">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ba2ff-126">Required</span></span>  <br/> |<span data-ttu-id="ba2ff-127">**String**</span><span class="sxs-lookup"><span data-stu-id="ba2ff-127">**String**</span></span> <br/> |<span data-ttu-id="ba2ff-128">El texto que reemplazará los caracteres en _texto_anterior_.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-128">The text that will replace characters in  _old_text_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ba2ff-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba2ff-129">Return value</span></span>

<span data-ttu-id="ba2ff-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="ba2ff-130">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ba2ff-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba2ff-131">Remarks</span></span>

<span data-ttu-id="ba2ff-p102">Utilice esta función cuando desee reemplazar texto que aparezca en una ubicación concreta de una cadena de texto. Si desea reemplazar un texto específico dentro de una cadena de texto, recurra a la función SUBSTITUTE.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-p102">Use the REPLACE function when you want to replace text that occurs in a specific location in a text string. If you want to replace specific text in a text string, use the SUBSTITUTE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="ba2ff-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba2ff-134">Example</span></span>

<span data-ttu-id="ba2ff-135">REPLACE ("01/03/2002",9,2,"03")</span><span class="sxs-lookup"><span data-stu-id="ba2ff-135">REPLACE ("01/03/2002",9,2,"03")</span></span> 
  
<span data-ttu-id="ba2ff-136">Devuelve 01/03/2003.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-136">Returns 01/03/2003.</span></span> 
  

