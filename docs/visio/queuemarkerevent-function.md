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
description: Hace que la aplicación desencadene un evento de marcador en el complemento, el código de Microsoft Visual Basic para aplicaciones (VBA) o el complemento COM.
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418809"
---
# <a name="queuemarkerevent-function"></a><span data-ttu-id="554f1-103">Función QUEUEMARKEREVENT</span><span class="sxs-lookup"><span data-stu-id="554f1-103">QUEUEMARKEREVENT Function</span></span>

<span data-ttu-id="554f1-104">Hace que la aplicación desencadene un evento de marcador en el complemento, el código de Microsoft Visual Basic para aplicaciones (VBA) o el complemento COM.</span><span class="sxs-lookup"><span data-stu-id="554f1-104">Causes the application to fire a marker event to your add-on, Microsoft Visual Basic for Applications (VBA) code, or COM add-in.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="554f1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="554f1-105">Syntax</span></span>

<span data-ttu-id="554f1-106">QUEUEMARKEREVENT (\* \* *event_string* \* \*)</span><span class="sxs-lookup"><span data-stu-id="554f1-106">QUEUEMARKEREVENT (\*\* *event_string* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="554f1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="554f1-107">Parameters</span></span>

|<span data-ttu-id="554f1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="554f1-108">**Name**</span></span>|<span data-ttu-id="554f1-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="554f1-109">**Required/Optional**</span></span>|<span data-ttu-id="554f1-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="554f1-110">**Data Type**</span></span>|<span data-ttu-id="554f1-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="554f1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="554f1-112">_event_string_</span><span class="sxs-lookup"><span data-stu-id="554f1-112">_event_string_</span></span> <br/> |<span data-ttu-id="554f1-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="554f1-113">Required</span></span>  <br/> |<span data-ttu-id="554f1-114">**String**</span><span class="sxs-lookup"><span data-stu-id="554f1-114">**String**</span></span> <br/> | <span data-ttu-id="554f1-115">La cadena que se pasa al controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="554f1-115">The string to pass to your event handler.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="554f1-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="554f1-116">Remarks</span></span>

<span data-ttu-id="554f1-117">La función QUEUEMARKEREVENT ofrece a los programadores un método para notificar al código desde una celda de ShapeSheet y pasar información específica de la solución.</span><span class="sxs-lookup"><span data-stu-id="554f1-117">The QUEUEMARKEREVENT function provides developers with a way to notify their code from a ShapeSheet cell, and pass solution-specific information.</span></span> <span data-ttu-id="554f1-118">Cuando se evalúa la celda que contiene la fórmula con la función QUEUEMARKEREVENT, la aplicación desencadena un evento de marcador y pasa _event_string_ a todos los controladores de eventos que están escuchando el evento **MarkerEvent** .</span><span class="sxs-lookup"><span data-stu-id="554f1-118">When the cell containing the formula with the QUEUEMARKEREVENT function is evaluated, the application fires a marker event and passes  _event_string_ to all event handlers that are listening to the **MarkerEvent** event.</span></span> 
  
<span data-ttu-id="554f1-119">Para obtener más información acerca de los eventos de marcador, vea los temas del método **QueueMarkerEvent** y del evento **MarkerEvent** en la referencia de automatización de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="554f1-119">For more information about marker events, see the **QueueMarkerEvent** method and **MarkerEvent** event topics in the Microsoft Visio Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="554f1-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="554f1-120">Example</span></span>

<span data-ttu-id="554f1-121">QUEUEMARKEREVENT ("MiNotificaciónPersonalizada")</span><span class="sxs-lookup"><span data-stu-id="554f1-121">QUEUEMARKEREVENT ("MyCustomNotification")</span></span> 
  
<span data-ttu-id="554f1-122">Hace que la aplicación desencadene un evento de marcador y pasa la cadena "MiNotificaciónPersonalizada" a los controladores de eventos que estén atentos al evento **MarkerEvent**.</span><span class="sxs-lookup"><span data-stu-id="554f1-122">Causes the application to fire a marker event, and passes the string "MyCustomNotification" to event handlers that are listening to the **MarkerEvent** event.</span></span> 
  

