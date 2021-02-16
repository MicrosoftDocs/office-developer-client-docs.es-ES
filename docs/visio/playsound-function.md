---
title: PLAYSOUND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251479
localization_priority: Normal
ms.assetid: 098d216f-e699-0e74-f702-ccfa7809c19b
description: Reproduce un archivo de sonido o un sonido del sistema.
ms.openlocfilehash: 752412aab6584d2b01235fe88644e3ec3fa5daee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435842"
---
# <a name="playsound-function"></a><span data-ttu-id="c64b7-103">Función PLAYSOUND</span><span class="sxs-lookup"><span data-stu-id="c64b7-103">PLAYSOUND Function</span></span>

<span data-ttu-id="c64b7-104">Reproduce un archivo de sonido o un sonido del sistema.</span><span class="sxs-lookup"><span data-stu-id="c64b7-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c64b7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c64b7-105">Syntax</span></span>

<span data-ttu-id="c64b7-106">PLAYSOUND(" \*\* *filename* \*\* "|" \*\* *alias* \*\* ", \*\* *isAlias* \*\*, \*\* *beep* \*\*, \*\* *synch* \*\* )</span><span class="sxs-lookup"><span data-stu-id="c64b7-106">PLAYSOUND(" \*\* *filename* \*\* "|" \*\* *alias* \*\* ", \*\* *isAlias* \*\*, \*\* *beep* \*\*, \*\* *synch* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c64b7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c64b7-107">Parameters</span></span>

|<span data-ttu-id="c64b7-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c64b7-108">**Name**</span></span>|<span data-ttu-id="c64b7-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="c64b7-109">**Required/Optional**</span></span>|<span data-ttu-id="c64b7-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c64b7-110">**Data Type**</span></span>|<span data-ttu-id="c64b7-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c64b7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c64b7-112">_filename_</span><span class="sxs-lookup"><span data-stu-id="c64b7-112">_filename_</span></span> <br/> |<span data-ttu-id="c64b7-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c64b7-113">Required</span></span>  <br/> |<span data-ttu-id="c64b7-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c64b7-114">**String**</span></span> <br/> |<span data-ttu-id="c64b7-115">El nombre del archivo de sonido que desea reproducir.</span><span class="sxs-lookup"><span data-stu-id="c64b7-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="c64b7-116">_alias_</span><span class="sxs-lookup"><span data-stu-id="c64b7-116">_alias_</span></span> <br/> |<span data-ttu-id="c64b7-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c64b7-117">Required</span></span>  <br/> |<span data-ttu-id="c64b7-118">**String**</span><span class="sxs-lookup"><span data-stu-id="c64b7-118">**String**</span></span> <br/> | <span data-ttu-id="c64b7-119">Un sonido del sistema representado por un alias.</span><span class="sxs-lookup"><span data-stu-id="c64b7-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="c64b7-120">_isAlias_</span><span class="sxs-lookup"><span data-stu-id="c64b7-120">_isAlias_</span></span> <br/> |<span data-ttu-id="c64b7-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c64b7-121">Required</span></span>  <br/> |<span data-ttu-id="c64b7-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c64b7-122">**Boolean**</span></span> <br/> | <span data-ttu-id="c64b7-123">Especifica si la expresión precedente se trata de un alias o de un nombre de archivo; un valor distinto de cero indica que se trata de un alias.</span><span class="sxs-lookup"><span data-stu-id="c64b7-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="c64b7-124">_bip_</span><span class="sxs-lookup"><span data-stu-id="c64b7-124">_beep_</span></span> <br/> |<span data-ttu-id="c64b7-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c64b7-125">Required</span></span>  <br/> |<span data-ttu-id="c64b7-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c64b7-126">**Boolean**</span></span> <br/> |<span data-ttu-id="c64b7-127">Especifica que Microsoft Visio debe emitir un pitido cuando no se pueda reproducir el sonido seleccionado, para que se oiga el pitido este valor debe ser distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="c64b7-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="c64b7-128">_synch_</span><span class="sxs-lookup"><span data-stu-id="c64b7-128">_synch_</span></span> <br/> |<span data-ttu-id="c64b7-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c64b7-129">Required</span></span>  <br/> |<span data-ttu-id="c64b7-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c64b7-130">**Boolean**</span></span> <br/> |<span data-ttu-id="c64b7-131">Determina si los sonidos se deben reproducir de forma asincrónica (0) o sincrónica (1).</span><span class="sxs-lookup"><span data-stu-id="c64b7-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c64b7-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c64b7-132">Remarks</span></span>

<span data-ttu-id="c64b7-133">Debe reproducir los sonidos siempre de forma asincrónica para que Visio se pueda seguir ejecutando mientras se reproduce el sonido.</span><span class="sxs-lookup"><span data-stu-id="c64b7-133">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound.</span></span> <span data-ttu-id="c64b7-134">Para encadenar varios sonidos de manera que suenen uno a continuación del otro, debe reproducirlos de forma sincrónica ya que, de lo contrario, algunos podrían no reproducirse.</span><span class="sxs-lookup"><span data-stu-id="c64b7-134">To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c64b7-135">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="c64b7-135">Example 1</span></span>

<span data-ttu-id="c64b7-136">PLAYSOUND("guitarra.wav"; 0; 0; 0)</span><span class="sxs-lookup"><span data-stu-id="c64b7-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="c64b7-137">Reproduce el archivo de audio de ondas guitarra.wav de forma asincrónica y sin pitido de advertencia.</span><span class="sxs-lookup"><span data-stu-id="c64b7-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c64b7-138">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="c64b7-138">Example 2</span></span>

<span data-ttu-id="c64b7-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="c64b7-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="c64b7-140">Reproduce el sonido de exclamación de forma asincrónica y sin pitido de advertencia.</span><span class="sxs-lookup"><span data-stu-id="c64b7-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

