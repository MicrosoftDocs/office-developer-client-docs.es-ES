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
ms.openlocfilehash: ca54b749b764e9ea2c7db71d41268303542417f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822784"
---
# <a name="playsound-function"></a><span data-ttu-id="f5ca4-103">PLAYSOUND (función)</span><span class="sxs-lookup"><span data-stu-id="f5ca4-103">PLAYSOUND Function</span></span>

<span data-ttu-id="f5ca4-104">Reproduce un archivo de sonido o un sonido del sistema.</span><span class="sxs-lookup"><span data-stu-id="f5ca4-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f5ca4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5ca4-105">Syntax</span></span>

<span data-ttu-id="f5ca4-106">PLAYSOUND ("** *filename* **" | "** *alias* **", ** *esAlias* **, ** *beep* **, ** *synch* **)</span><span class="sxs-lookup"><span data-stu-id="f5ca4-106">PLAYSOUND(" ** *filename* ** "|" ** *alias* ** ", ** *isAlias* **, ** *beep* **, ** *synch* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f5ca4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5ca4-107">Parameters</span></span>

|<span data-ttu-id="f5ca4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f5ca4-108">**Name**</span></span>|<span data-ttu-id="f5ca4-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="f5ca4-109">**Required/Optional**</span></span>|<span data-ttu-id="f5ca4-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="f5ca4-110">**Data Type**</span></span>|<span data-ttu-id="f5ca4-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f5ca4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f5ca4-112">_nombre de archivo_</span><span class="sxs-lookup"><span data-stu-id="f5ca4-112">_filename_</span></span> <br/> |<span data-ttu-id="f5ca4-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f5ca4-113">Required</span></span>  <br/> |<span data-ttu-id="f5ca4-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f5ca4-114">**String**</span></span> <br/> |<span data-ttu-id="f5ca4-115">El nombre del archivo de sonido que desea reproducir.</span><span class="sxs-lookup"><span data-stu-id="f5ca4-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="f5ca4-116">_alias_</span><span class="sxs-lookup"><span data-stu-id="f5ca4-116">_alias_</span></span> <br/> |<span data-ttu-id="f5ca4-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f5ca4-117">Required</span></span>  <br/> |<span data-ttu-id="f5ca4-118">**String**</span><span class="sxs-lookup"><span data-stu-id="f5ca4-118">**String**</span></span> <br/> | <span data-ttu-id="f5ca4-119">Un sonido del sistema representado por un alias.</span><span class="sxs-lookup"><span data-stu-id="f5ca4-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="f5ca4-120">_esAlias_</span><span class="sxs-lookup"><span data-stu-id="f5ca4-120">_isAlias_</span></span> <br/> |<span data-ttu-id="f5ca4-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f5ca4-121">Required</span></span>  <br/> |<span data-ttu-id="f5ca4-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f5ca4-122">**Boolean**</span></span> <br/> | <span data-ttu-id="f5ca4-123">Especifica si la expresión precedente se trata de un alias o de un nombre de archivo; un valor distinto de cero indica que se trata de un alias.</span><span class="sxs-lookup"><span data-stu-id="f5ca4-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="f5ca4-124">_Bip_</span><span class="sxs-lookup"><span data-stu-id="f5ca4-124">_beep_</span></span> <br/> |<span data-ttu-id="f5ca4-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f5ca4-125">Required</span></span>  <br/> |<span data-ttu-id="f5ca4-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f5ca4-126">**Boolean**</span></span> <br/> |<span data-ttu-id="f5ca4-127">Especifica que Microsoft Visio debe emitir un pitido cuando no se pueda reproducir el sonido seleccionado, para que se oiga el pitido este valor debe ser distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="f5ca4-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="f5ca4-128">_sincronización_</span><span class="sxs-lookup"><span data-stu-id="f5ca4-128">_synch_</span></span> <br/> |<span data-ttu-id="f5ca4-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f5ca4-129">Required</span></span>  <br/> |<span data-ttu-id="f5ca4-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f5ca4-130">**Boolean**</span></span> <br/> |<span data-ttu-id="f5ca4-131">Determina si los sonidos se deben reproducir de forma asincrónica (0) o sincrónica (1).</span><span class="sxs-lookup"><span data-stu-id="f5ca4-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5ca4-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5ca4-132">Remarks</span></span>

<span data-ttu-id="f5ca4-133">Normalmente, debe reproducir sonidos de forma asincrónica para que Visio puede continuar el procesamiento mientras reproduce el sonido.</span><span class="sxs-lookup"><span data-stu-id="f5ca4-133">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound.</span></span> <span data-ttu-id="f5ca4-134">Para encadenar varios sonidos conjuntamente, reproducen ellos sincrónicamente, o es posible que algunas no reproducir.</span><span class="sxs-lookup"><span data-stu-id="f5ca4-134">To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f5ca4-135">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="f5ca4-135">Example 1</span></span>

<span data-ttu-id="f5ca4-136">PLAYSOUND("guitarra.wav"; 0; 0; 0)</span><span class="sxs-lookup"><span data-stu-id="f5ca4-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="f5ca4-137">Reproduce el archivo de audio de ondas guitarra.wav de forma asincrónica y sin pitido de advertencia.</span><span class="sxs-lookup"><span data-stu-id="f5ca4-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f5ca4-138">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="f5ca4-138">Example 2</span></span>

<span data-ttu-id="f5ca4-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="f5ca4-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="f5ca4-140">Reproduce el sonido de exclamación de forma asincrónica y sin pitido de advertencia.</span><span class="sxs-lookup"><span data-stu-id="f5ca4-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

