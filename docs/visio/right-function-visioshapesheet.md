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
ms.openlocfilehash: e35cc4918809d5f134f9519c01cb3c93407258e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822986"
---
# <a name="right-function-visioshapesheet"></a><span data-ttu-id="c0873-103">Función RIGHT (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="c0873-103">RIGHT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="c0873-104">Devuelve el último carácter o caracteres de una cadena de texto, en función del número de caracteres que especifique.</span><span class="sxs-lookup"><span data-stu-id="c0873-104">Returns the last character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c0873-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0873-105">Syntax</span></span>

<span data-ttu-id="c0873-106">DERECHA (** *texto* ** [, ** *número_caracteres_opcional* **])</span><span class="sxs-lookup"><span data-stu-id="c0873-106">RIGHT(** *text* ** [, ** *num_chars_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c0873-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0873-107">Parameters</span></span>

|<span data-ttu-id="c0873-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c0873-108">**Name**</span></span>|<span data-ttu-id="c0873-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="c0873-109">**Required/Optional**</span></span>|<span data-ttu-id="c0873-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c0873-110">**Data Type**</span></span>|<span data-ttu-id="c0873-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c0873-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c0873-112">_text_</span><span class="sxs-lookup"><span data-stu-id="c0873-112">_text_</span></span> <br/> |<span data-ttu-id="c0873-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c0873-113">Required</span></span>  <br/> |<span data-ttu-id="c0873-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c0873-114">**String**</span></span> <br/> | <span data-ttu-id="c0873-115">La cadena de texto que contiene los caracteres que se desea extraer.</span><span class="sxs-lookup"><span data-stu-id="c0873-115">The text string containing the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="c0873-116">_número_caracteres_opcional_</span><span class="sxs-lookup"><span data-stu-id="c0873-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="c0873-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="c0873-117">Optional</span></span>  <br/> |<span data-ttu-id="c0873-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="c0873-118">**Number**</span></span> <br/> |<span data-ttu-id="c0873-p101">El número de caracteres que debe extraerse. El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="c0873-p101">The number of characters you want to extract. The default is 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c0873-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0873-121">Return value</span></span>

<span data-ttu-id="c0873-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="c0873-122">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0873-123">Notas</span><span class="sxs-lookup"><span data-stu-id="c0873-123">Remarks</span></span>

<span data-ttu-id="c0873-124">El valor de _número_caracteres_opcional_ debe ser mayor o igual que cero (0).</span><span class="sxs-lookup"><span data-stu-id="c0873-124">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="c0873-125">Si _número_caracteres_opcional_ es mayor que la longitud del texto, derecha devuelve todo el texto.</span><span class="sxs-lookup"><span data-stu-id="c0873-125">If  _num_chars_opt_ is greater than the length of the text, RIGHT returns all of the text.</span></span> <span data-ttu-id="c0873-126">Si se omite _número_caracteres_opcional_ , se supone que es 1.</span><span class="sxs-lookup"><span data-stu-id="c0873-126">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c0873-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0873-127">Example</span></span>

<span data-ttu-id="c0873-128">RIGHT ("1 de enero, 2004", 4)</span><span class="sxs-lookup"><span data-stu-id="c0873-128">RIGHT ("January 1, 2004", 4)</span></span> 
  
<span data-ttu-id="c0873-129">Devuelve el valor 2004.</span><span class="sxs-lookup"><span data-stu-id="c0873-129">Returns the value 2004.</span></span> 
  

