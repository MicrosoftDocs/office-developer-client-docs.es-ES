---
title: Función de la izquierda (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Devuelve el carácter más a la izquierda o caracteres de una cadena de texto, en función del número de caracteres que especifique.
ms.openlocfilehash: 4e8deb3098ce6d217dcce0cae23d07ed723d9fb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822440"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="c2eef-103">Función de la izquierda (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="c2eef-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="c2eef-104">Devuelve el carácter más a la izquierda o caracteres de una cadena de texto, en función del número de caracteres que especifique.</span><span class="sxs-lookup"><span data-stu-id="c2eef-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c2eef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2eef-105">Syntax</span></span>

<span data-ttu-id="c2eef-106">IZQUIERDA (** *texto* **, [, ** *número_caracteres_opcional* **])</span><span class="sxs-lookup"><span data-stu-id="c2eef-106">LEFT(** *text* **, [, ** *num_chars_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c2eef-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2eef-107">Parameters</span></span>

|<span data-ttu-id="c2eef-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c2eef-108">**Name**</span></span>|<span data-ttu-id="c2eef-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="c2eef-109">**Required/Optional**</span></span>|<span data-ttu-id="c2eef-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c2eef-110">**Data Type**</span></span>|<span data-ttu-id="c2eef-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2eef-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c2eef-112">_text_</span><span class="sxs-lookup"><span data-stu-id="c2eef-112">_text_</span></span> <br/> |<span data-ttu-id="c2eef-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c2eef-113">Required</span></span>  <br/> |<span data-ttu-id="c2eef-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c2eef-114">**String**</span></span> <br/> |<span data-ttu-id="c2eef-115">La cadena de texto que contiene los caracteres que se desean extraer.</span><span class="sxs-lookup"><span data-stu-id="c2eef-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="c2eef-116">_número_caracteres_opcional_</span><span class="sxs-lookup"><span data-stu-id="c2eef-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="c2eef-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="c2eef-117">Optional</span></span>  <br/> |<span data-ttu-id="c2eef-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="c2eef-118">**Numeric**</span></span> <br/> |<span data-ttu-id="c2eef-119">Número de caracteres que se desean extraer.</span><span class="sxs-lookup"><span data-stu-id="c2eef-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c2eef-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2eef-120">Return value</span></span>

<span data-ttu-id="c2eef-121">String</span><span class="sxs-lookup"><span data-stu-id="c2eef-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c2eef-122">Notas</span><span class="sxs-lookup"><span data-stu-id="c2eef-122">Remarks</span></span>

<span data-ttu-id="c2eef-123">El valor de _número_caracteres_opcional_ debe ser mayor o igual que cero (0).</span><span class="sxs-lookup"><span data-stu-id="c2eef-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="c2eef-124">Si _número_caracteres_opcional_ es mayor que la longitud del texto, LEFT devuelve todo el texto.</span><span class="sxs-lookup"><span data-stu-id="c2eef-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="c2eef-125">Si se omite _número_caracteres_opcional_ , se supone que es 1.</span><span class="sxs-lookup"><span data-stu-id="c2eef-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c2eef-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2eef-126">Example</span></span>

<span data-ttu-id="c2eef-127">LEFT ("Enero 1, 2004", 3)</span><span class="sxs-lookup"><span data-stu-id="c2eef-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="c2eef-128">Devuelve el valor "Ene".</span><span class="sxs-lookup"><span data-stu-id="c2eef-128">Returns the value "Jan".</span></span> 
  

