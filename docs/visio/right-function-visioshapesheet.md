---
title: Función RIGHT (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Devuelve el último carácter o caracteres de una cadena de texto, en función del número de caracteres que especifique.
ms.openlocfilehash: faf14ef55b34e51bac11129d6857e381d07357c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326729"
---
# <a name="right-function-visioshapesheet"></a><span data-ttu-id="e0abc-103">Función RIGHT (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="e0abc-103">RIGHT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="e0abc-104">Devuelve el último carácter o caracteres de una cadena de texto, en función del número de caracteres que especifique.</span><span class="sxs-lookup"><span data-stu-id="e0abc-104">Returns the last character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e0abc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0abc-105">Syntax</span></span>

<span data-ttu-id="e0abc-106">Right (\* \* *Text* \* \* [, \* \* *número_caracteres_opcional* \* \*])</span><span class="sxs-lookup"><span data-stu-id="e0abc-106">RIGHT(\*\* *text* \*\* [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e0abc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0abc-107">Parameters</span></span>

|<span data-ttu-id="e0abc-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e0abc-108">**Name**</span></span>|<span data-ttu-id="e0abc-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e0abc-109">**Required/Optional**</span></span>|<span data-ttu-id="e0abc-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="e0abc-110">**Data Type**</span></span>|<span data-ttu-id="e0abc-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0abc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e0abc-112">_text_</span><span class="sxs-lookup"><span data-stu-id="e0abc-112">_text_</span></span> <br/> |<span data-ttu-id="e0abc-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e0abc-113">Required</span></span>  <br/> |<span data-ttu-id="e0abc-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e0abc-114">**String**</span></span> <br/> | <span data-ttu-id="e0abc-115">La cadena de texto que contiene los caracteres que se desea extraer.</span><span class="sxs-lookup"><span data-stu-id="e0abc-115">The text string containing the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="e0abc-116">_número_caracteres_opcional_</span><span class="sxs-lookup"><span data-stu-id="e0abc-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="e0abc-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="e0abc-117">Optional</span></span>  <br/> |<span data-ttu-id="e0abc-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="e0abc-118">**Number**</span></span> <br/> |<span data-ttu-id="e0abc-119">El número de caracteres que debe extraerse.</span><span class="sxs-lookup"><span data-stu-id="e0abc-119">The number of characters you want to extract.</span></span> <span data-ttu-id="e0abc-120">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="e0abc-120">The default is 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e0abc-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0abc-121">Return value</span></span>

<span data-ttu-id="e0abc-122">String</span><span class="sxs-lookup"><span data-stu-id="e0abc-122">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0abc-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0abc-123">Remarks</span></span>

<span data-ttu-id="e0abc-124">El valor de _número_caracteres_opcional_ debe ser mayor o igual que cero (0).</span><span class="sxs-lookup"><span data-stu-id="e0abc-124">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="e0abc-125">Si _número_caracteres_opcional_ es mayor que la longitud del texto, Right devuelve todo el texto.</span><span class="sxs-lookup"><span data-stu-id="e0abc-125">If  _num_chars_opt_ is greater than the length of the text, RIGHT returns all of the text.</span></span> <span data-ttu-id="e0abc-126">Si se omite _número_caracteres_opcional_ , se supone que es 1.</span><span class="sxs-lookup"><span data-stu-id="e0abc-126">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e0abc-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e0abc-127">Example</span></span>

<span data-ttu-id="e0abc-128">RIGHT ("1 de enero, 2004", 4)</span><span class="sxs-lookup"><span data-stu-id="e0abc-128">RIGHT ("January 1, 2004", 4)</span></span> 
  
<span data-ttu-id="e0abc-129">Devuelve el valor 2004.</span><span class="sxs-lookup"><span data-stu-id="e0abc-129">Returns the value 2004.</span></span> 
  

