---
title: MID (función) (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Devuelve un número específico de caracteres de una cadena de texto, empezando por la posición que especifique, en función del número de caracteres que especifique.
ms.openlocfilehash: 96e697211ebf6ea61ddf0b749d8e1259f2a1e53d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822657"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="6e051-103">MID (función) (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="6e051-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="6e051-104">Devuelve un número específico de caracteres de una cadena de texto, empezando por la posición que especifique, en función del número de caracteres que especifique.</span><span class="sxs-lookup"><span data-stu-id="6e051-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6e051-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e051-105">Syntax</span></span>

<span data-ttu-id="6e051-106">MID (** *texto* **, ** *número_inicio* **, ** *número_caracteres* **)</span><span class="sxs-lookup"><span data-stu-id="6e051-106">MID (** *text* **, ** *start_num* **, ** *num_chars* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6e051-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e051-107">Parameters</span></span>

|<span data-ttu-id="6e051-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6e051-108">**Name**</span></span>|<span data-ttu-id="6e051-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="6e051-109">**Required/Optional**</span></span>|<span data-ttu-id="6e051-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="6e051-110">**Data Type**</span></span>|<span data-ttu-id="6e051-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6e051-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6e051-112">_text_</span><span class="sxs-lookup"><span data-stu-id="6e051-112">_text_</span></span> <br/> |<span data-ttu-id="6e051-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e051-113">Required</span></span>  <br/> |<span data-ttu-id="6e051-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6e051-114">**String**</span></span> <br/> |<span data-ttu-id="6e051-115">La cadena de texto que contiene los caracteres que se desean extraer.</span><span class="sxs-lookup"><span data-stu-id="6e051-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="6e051-116">_número inicial_</span><span class="sxs-lookup"><span data-stu-id="6e051-116">_start_num_</span></span> <br/> |<span data-ttu-id="6e051-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e051-117">Required</span></span>  <br/> |<span data-ttu-id="6e051-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="6e051-118">**Number**</span></span> <br/> |<span data-ttu-id="6e051-p101">La posición del primer carácter que se desea extraer. El primer carácter de la cadena de texto ocupa la posición 1.</span><span class="sxs-lookup"><span data-stu-id="6e051-p101">The position of the first character you want to extract. The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="6e051-121">_número_caracteres_</span><span class="sxs-lookup"><span data-stu-id="6e051-121">_num_chars_</span></span> <br/> |<span data-ttu-id="6e051-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e051-122">Required</span></span>  <br/> |<span data-ttu-id="6e051-123">**Número**</span><span class="sxs-lookup"><span data-stu-id="6e051-123">**Number**</span></span> <br/> |<span data-ttu-id="6e051-124">Número de caracteres que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="6e051-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6e051-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e051-125">Return value</span></span>

<span data-ttu-id="6e051-126">String</span><span class="sxs-lookup"><span data-stu-id="6e051-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6e051-127">Notas</span><span class="sxs-lookup"><span data-stu-id="6e051-127">Remarks</span></span>

<span data-ttu-id="6e051-128">Si *número_inicio* es:</span><span class="sxs-lookup"><span data-stu-id="6e051-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="6e051-129">Mayor que la longitud del *texto* , MID devuelve "" (texto vacío).</span><span class="sxs-lookup"><span data-stu-id="6e051-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="6e051-130">Menor que la longitud del *texto* , pero la *suma de número_inicio* y *número_caracteres* excede la longitud del *texto* , MID devuelve los caracteres hasta el final del *texto* .</span><span class="sxs-lookup"><span data-stu-id="6e051-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="6e051-p102">Menor que 1, MID devuelve el error #VALUE!</span><span class="sxs-lookup"><span data-stu-id="6e051-p102">Less than 1, MID returns the #VALUE! error value.</span></span> 
    
<span data-ttu-id="6e051-133">¡Si *número_caracteres* es negativo, MID devuelve #VALUE!</span><span class="sxs-lookup"><span data-stu-id="6e051-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="6e051-134">valor de error.</span><span class="sxs-lookup"><span data-stu-id="6e051-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6e051-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e051-135">Example</span></span>

<span data-ttu-id="6e051-136">MID ("SSN 999-99-9999",5,11)</span><span class="sxs-lookup"><span data-stu-id="6e051-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="6e051-137">Devuelve 999-99-9999.</span><span class="sxs-lookup"><span data-stu-id="6e051-137">Returns 999-99-9999.</span></span> 
  

