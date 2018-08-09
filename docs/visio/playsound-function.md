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
# <a name="playsound-function"></a><span data-ttu-id="2337d-103">Función PLAYSOUND</span><span class="sxs-lookup"><span data-stu-id="2337d-103">PLAYSOUND Function</span></span>

<span data-ttu-id="2337d-104">Reproduce un archivo de sonido o un sonido del sistema.</span><span class="sxs-lookup"><span data-stu-id="2337d-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2337d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2337d-105">Syntax</span></span>

<span data-ttu-id="2337d-106">PLAYSOUND ("** *filename* **" | "** *alias* **", ** *esAlias* **, ** *beep* **, ** *synch* **)</span><span class="sxs-lookup"><span data-stu-id="2337d-106">PLAYSOUND(" ** *filename* ** "|" ** *alias* ** ", ** *isAlias* **, ** *beep* **, ** *synch* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2337d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2337d-107">Parameters</span></span>

|<span data-ttu-id="2337d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2337d-108">**Name**</span></span>|<span data-ttu-id="2337d-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="2337d-109">**Required/Optional**</span></span>|<span data-ttu-id="2337d-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2337d-110">**Data Type**</span></span>|<span data-ttu-id="2337d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2337d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2337d-112">_nombre de archivo_</span><span class="sxs-lookup"><span data-stu-id="2337d-112">_filename_</span></span> <br/> |<span data-ttu-id="2337d-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2337d-113">Required</span></span>  <br/> |<span data-ttu-id="2337d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="2337d-114">**String**</span></span> <br/> |<span data-ttu-id="2337d-115">El nombre del archivo de sonido que desea reproducir.</span><span class="sxs-lookup"><span data-stu-id="2337d-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="2337d-116">_alias_</span><span class="sxs-lookup"><span data-stu-id="2337d-116">_alias_</span></span> <br/> |<span data-ttu-id="2337d-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2337d-117">Required</span></span>  <br/> |<span data-ttu-id="2337d-118">**String**</span><span class="sxs-lookup"><span data-stu-id="2337d-118">**String**</span></span> <br/> | <span data-ttu-id="2337d-119">Un sonido del sistema representado por un alias.</span><span class="sxs-lookup"><span data-stu-id="2337d-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="2337d-120">_esAlias_</span><span class="sxs-lookup"><span data-stu-id="2337d-120">_isAlias_</span></span> <br/> |<span data-ttu-id="2337d-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2337d-121">Required</span></span>  <br/> |<span data-ttu-id="2337d-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2337d-122">**Boolean**</span></span> <br/> | <span data-ttu-id="2337d-123">Especifica si la expresión precedente se trata de un alias o de un nombre de archivo; un valor distinto de cero indica que se trata de un alias.</span><span class="sxs-lookup"><span data-stu-id="2337d-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="2337d-124">_Bip_</span><span class="sxs-lookup"><span data-stu-id="2337d-124">_beep_</span></span> <br/> |<span data-ttu-id="2337d-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2337d-125">Required</span></span>  <br/> |<span data-ttu-id="2337d-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2337d-126">**Boolean**</span></span> <br/> |<span data-ttu-id="2337d-127">Especifica que Microsoft Visio debe emitir un pitido cuando no se pueda reproducir el sonido seleccionado, para que se oiga el pitido este valor debe ser distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="2337d-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="2337d-128">_sincronización_</span><span class="sxs-lookup"><span data-stu-id="2337d-128">_synch_</span></span> <br/> |<span data-ttu-id="2337d-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2337d-129">Required</span></span>  <br/> |<span data-ttu-id="2337d-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2337d-130">**Boolean**</span></span> <br/> |<span data-ttu-id="2337d-131">Determina si los sonidos se deben reproducir de forma asincrónica (0) o sincrónica (1).</span><span class="sxs-lookup"><span data-stu-id="2337d-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2337d-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2337d-132">Remarks</span></span>

<span data-ttu-id="2337d-p101">Debe reproducir los sonidos siempre de forma asincrónica para que Visio se pueda seguir ejecutando mientras se reproduce el sonido. Para encadenar varios sonidos de manera que suenen uno a continuación del otro, debe reproducirlos de forma sincrónica ya que, de lo contrario, algunos podrían no reproducirse.
</span><span class="sxs-lookup"><span data-stu-id="2337d-p101">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound. To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="2337d-135">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="2337d-135">Example 1</span></span>

<span data-ttu-id="2337d-136">PLAYSOUND("guitarra.wav"; 0; 0; 0)</span><span class="sxs-lookup"><span data-stu-id="2337d-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="2337d-137">Reproduce el archivo de audio de ondas guitarra.wav de forma asincrónica y sin pitido de advertencia.</span><span class="sxs-lookup"><span data-stu-id="2337d-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="2337d-138">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="2337d-138">Example 2</span></span>

<span data-ttu-id="2337d-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="2337d-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="2337d-140">Reproduce el sonido de exclamación de forma asincrónica y sin pitido de advertencia.</span><span class="sxs-lookup"><span data-stu-id="2337d-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

