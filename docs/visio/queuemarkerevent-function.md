---
title: QUEUEMARKEREVENT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60107
localization_priority: Normal
ms.assetid: b4671715-4209-7774-c174-c19dc9721a02
description: Hace que la aplicación desencadene un evento de marcador en el complemento, Microsoft Visual Basic para aplicaciones (VBA), o un complemento COM.
ms.openlocfilehash: b9175caf0845530c93f6db15e286f3eae21ea415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822888"
---
# <a name="queuemarkerevent-function"></a><span data-ttu-id="ece9a-103">Función QUEUEMARKEREVENT</span><span class="sxs-lookup"><span data-stu-id="ece9a-103">QUEUEMARKEREVENT Function</span></span>

<span data-ttu-id="ece9a-104">Hace que la aplicación desencadene un evento de marcador en el complemento, Microsoft Visual Basic para aplicaciones (VBA), o un complemento COM.</span><span class="sxs-lookup"><span data-stu-id="ece9a-104">Causes the application to fire a marker event to your add-on, Microsoft Visual Basic for Applications (VBA) code, or COM add-in.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ece9a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ece9a-105">Syntax</span></span>

<span data-ttu-id="ece9a-106">QUEUEMARKEREVENT (** *cadena_evento* **)</span><span class="sxs-lookup"><span data-stu-id="ece9a-106">QUEUEMARKEREVENT (** *event_string* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ece9a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ece9a-107">Parameters</span></span>

|<span data-ttu-id="ece9a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ece9a-108">**Name**</span></span>|<span data-ttu-id="ece9a-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="ece9a-109">**Required/Optional**</span></span>|<span data-ttu-id="ece9a-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ece9a-110">**Data Type**</span></span>|<span data-ttu-id="ece9a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ece9a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ece9a-112">_cadena_evento_</span><span class="sxs-lookup"><span data-stu-id="ece9a-112">_event_string_</span></span> <br/> |<span data-ttu-id="ece9a-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ece9a-113">Required</span></span>  <br/> |<span data-ttu-id="ece9a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ece9a-114">**String**</span></span> <br/> | <span data-ttu-id="ece9a-115">La cadena que se pase a su controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="ece9a-115">The string to pass to your event handler.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ece9a-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ece9a-116">Remarks</span></span>

<span data-ttu-id="ece9a-117">La función QUEUEMARKEREVENT ofrece a los programadores una forma de notificar a su código de una celda de ShapeSheet y pasar información específica de la solución.</span><span class="sxs-lookup"><span data-stu-id="ece9a-117">The QUEUEMARKEREVENT function provides developers with a way to notify their code from a ShapeSheet cell, and pass solution-specific information.</span></span> <span data-ttu-id="ece9a-118">Cuando la celda que contiene la fórmula con la función QUEUEMARKEREVENT se evalúa, la aplicación desencadena un evento de marcador y pasa _cadena_evento_ a todos los controladores de eventos que estén atentos al evento **MarkerEvent** .</span><span class="sxs-lookup"><span data-stu-id="ece9a-118">When the cell containing the formula with the QUEUEMARKEREVENT function is evaluated, the application fires a marker event and passes  _event_string_ to all event handlers that are listening to the **MarkerEvent** event.</span></span> 
  
<span data-ttu-id="ece9a-119">Para obtener más información acerca de los eventos de marcador, vea el método **QueueMarkerEvent** y temas de evento **MarkerEvent** en la referencia de automatización de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="ece9a-119">For more information about marker events, see the **QueueMarkerEvent** method and **MarkerEvent** event topics in the Microsoft Visio Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ece9a-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ece9a-120">Example</span></span>

<span data-ttu-id="ece9a-121">QUEUEMARKEREVENT ("MiNotificaciónPersonalizada")</span><span class="sxs-lookup"><span data-stu-id="ece9a-121">QUEUEMARKEREVENT ("MyCustomNotification")</span></span> 
  
<span data-ttu-id="ece9a-122">Hace que la aplicación desencadene un evento de marcador y pasa la cadena "MiNotificaciónPersonalizada" a los controladores de eventos que estén atentos al evento **MarkerEvent**.</span><span class="sxs-lookup"><span data-stu-id="ece9a-122">Causes the application to fire a marker event, and passes the string "MyCustomNotification" to event handlers that are listening to the **MarkerEvent** event.</span></span> 
  

