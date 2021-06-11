---
title: Función LEFT (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Devuelve el carácter o los caracteres más a la izquierda de una cadena de texto, en función del número de caracteres que especifique.
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427524"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="4a951-103">Función LEFT (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="4a951-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="4a951-104">Devuelve el carácter o los caracteres más a la izquierda de una cadena de texto, en función del número de caracteres que especifique.</span><span class="sxs-lookup"><span data-stu-id="4a951-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4a951-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a951-105">Syntax</span></span>

<span data-ttu-id="4a951-106">LEFT(\*\* *text* \*\*, [, \*\* *num_chars_opt* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="4a951-106">LEFT(\*\* *text* \*\*, [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4a951-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a951-107">Parameters</span></span>

|<span data-ttu-id="4a951-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4a951-108">**Name**</span></span>|<span data-ttu-id="4a951-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="4a951-109">**Required/Optional**</span></span>|<span data-ttu-id="4a951-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4a951-110">**Data Type**</span></span>|<span data-ttu-id="4a951-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a951-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4a951-112">_text_</span><span class="sxs-lookup"><span data-stu-id="4a951-112">_text_</span></span> <br/> |<span data-ttu-id="4a951-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4a951-113">Required</span></span>  <br/> |<span data-ttu-id="4a951-114">**String**</span><span class="sxs-lookup"><span data-stu-id="4a951-114">**String**</span></span> <br/> |<span data-ttu-id="4a951-115">La cadena de texto que contiene los caracteres que se desean extraer.</span><span class="sxs-lookup"><span data-stu-id="4a951-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="4a951-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="4a951-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="4a951-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="4a951-117">Optional</span></span>  <br/> |<span data-ttu-id="4a951-118">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="4a951-118">**Numeric**</span></span> <br/> |<span data-ttu-id="4a951-119">El número de caracteres que debe extraerse.</span><span class="sxs-lookup"><span data-stu-id="4a951-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4a951-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a951-120">Return value</span></span>

<span data-ttu-id="4a951-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="4a951-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4a951-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a951-122">Remarks</span></span>

<span data-ttu-id="4a951-123">El valor de  _num_chars_opt_ debe ser mayor o igual que cero (0).</span><span class="sxs-lookup"><span data-stu-id="4a951-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="4a951-124">Si  _num_chars_opt_ es mayor que la longitud del texto, LEFT devuelve todo el texto.</span><span class="sxs-lookup"><span data-stu-id="4a951-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="4a951-125">Si  _num_chars_opt_ se omite, se supone que es 1.</span><span class="sxs-lookup"><span data-stu-id="4a951-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4a951-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a951-126">Example</span></span>

<span data-ttu-id="4a951-127">LEFT ("Enero 1, 2004", 3)</span><span class="sxs-lookup"><span data-stu-id="4a951-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="4a951-128">Devuelve el valor "Ene".</span><span class="sxs-lookup"><span data-stu-id="4a951-128">Returns the value "Jan".</span></span> 
  

