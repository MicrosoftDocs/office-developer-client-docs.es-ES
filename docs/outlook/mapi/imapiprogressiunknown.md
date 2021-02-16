---
title: IMAPIProgress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3a3d54ac9485cc3915d3606bb84b4f3191d1ca5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419649"
---
# <a name="imapiprogress--iunknown"></a><span data-ttu-id="50e46-103">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50e46-103">IMAPIProgress : IUnknown</span></span>

  
  
<span data-ttu-id="50e46-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50e46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50e46-105">Implementa un objeto de progreso que proporciona a las aplicaciones cliente un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="50e46-105">Implements a progress object that provides client applications with a progress indicator.</span></span> <span data-ttu-id="50e46-106">Un indicador de progreso es una presentación de interfaz de usuario que muestra el porcentaje de finalización de una operación, como copiar carpetas entre almacenes de mensajes.</span><span class="sxs-lookup"><span data-stu-id="50e46-106">A progress indicator is a user-interface display that shows the percentage of completion of an operation, such as copying folders between message stores.</span></span> <span data-ttu-id="50e46-107">MAPI y las aplicaciones cliente implementan objetos de progreso y los proveedores de servicios los usan.</span><span class="sxs-lookup"><span data-stu-id="50e46-107">MAPI and client applications implement progress objects and service providers use them.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50e46-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="50e46-108">Header file:</span></span>  <br/> |<span data-ttu-id="50e46-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50e46-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="50e46-110">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="50e46-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="50e46-111">Objetos de progreso</span><span class="sxs-lookup"><span data-stu-id="50e46-111">Progress objects</span></span>  <br/> |
|<span data-ttu-id="50e46-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="50e46-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="50e46-113">MAPI y aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="50e46-113">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="50e46-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="50e46-114">Called by:</span></span>  <br/> |<span data-ttu-id="50e46-115">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="50e46-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="50e46-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="50e46-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="50e46-117">IID_IMAPIProgress</span><span class="sxs-lookup"><span data-stu-id="50e46-117">IID_IMAPIProgress</span></span>  <br/> |
|<span data-ttu-id="50e46-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="50e46-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="50e46-119">LPMAPIPROGRESS</span><span class="sxs-lookup"><span data-stu-id="50e46-119">LPMAPIPROGRESS</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="50e46-120">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="50e46-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="50e46-121">Progress</span><span class="sxs-lookup"><span data-stu-id="50e46-121">Progress</span></span>](imapiprogress-progress.md) <br/> |<span data-ttu-id="50e46-122">Actualiza el indicador de progreso con una presentación del progreso a medida que se realiza hacia la finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="50e46-122">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span>  <br/> |
|[<span data-ttu-id="50e46-123">GetFlags</span><span class="sxs-lookup"><span data-stu-id="50e46-123">GetFlags</span></span>](imapiprogress-getflags.md) <br/> |<span data-ttu-id="50e46-124">Devuelve la configuración de marca del objeto de progreso para el nivel de operación en el que se calcula la información de progreso.</span><span class="sxs-lookup"><span data-stu-id="50e46-124">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>  <br/> |
|[<span data-ttu-id="50e46-125">GetMax</span><span class="sxs-lookup"><span data-stu-id="50e46-125">GetMax</span></span>](imapiprogress-getmax.md) <br/> |<span data-ttu-id="50e46-126">Devuelve el número máximo de elementos de la operación para los que se muestra información de progreso.</span><span class="sxs-lookup"><span data-stu-id="50e46-126">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="50e46-127">GetMin</span><span class="sxs-lookup"><span data-stu-id="50e46-127">GetMin</span></span>](imapiprogress-getmin.md) <br/> |<span data-ttu-id="50e46-128">Devuelve el valor mínimo del [método SetLimits](imapiprogress-setlimits.md) para el que se muestra información de progreso.</span><span class="sxs-lookup"><span data-stu-id="50e46-128">Returns the minimum value in the [SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="50e46-129">SetLimits</span><span class="sxs-lookup"><span data-stu-id="50e46-129">SetLimits</span></span>](imapiprogress-setlimits.md) <br/> |<span data-ttu-id="50e46-130">Establece los límites inferior y superior para el número de elementos de la operación y las marcas que controlan cómo se calcula la información de progreso para la operación.</span><span class="sxs-lookup"><span data-stu-id="50e46-130">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50e46-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="50e46-131">Remarks</span></span>

<span data-ttu-id="50e46-132">MAPI incluye un  _parámetro lpProgress_ en muchos de los métodos que realizan operaciones potencialmente largas.</span><span class="sxs-lookup"><span data-stu-id="50e46-132">MAPI includes an  _lpProgress_ parameter in many of the methods that perform potentially lengthy operations.</span></span>  <span data-ttu-id="50e46-133">_lpProgress_ apunta a una implementación de cliente de un objeto de progreso.</span><span class="sxs-lookup"><span data-stu-id="50e46-133">_lpProgress_ points to a client implementation of a progress object.</span></span> <span data-ttu-id="50e46-134">Los clientes que implementan **la interfaz IMAPIProgress** establecen este parámetro para que apunte a su implementación; los clientes que no implementan **IMAPIProgress** establecen el parámetro en NULL.</span><span class="sxs-lookup"><span data-stu-id="50e46-134">Clients that implement the **IMAPIProgress** interface set this parameter to point to their implementation; clients that do not implement **IMAPIProgress** set the parameter to NULL.</span></span> <span data-ttu-id="50e46-135">Para mostrar un indicador de progreso durante el procesamiento de la operación, los proveedores de servicios usan el objeto de progreso proporcionado por el cliente, si está disponible, o una implementación MAPI (que se indica cuando  _lpProgress_ se establece en NULL).</span><span class="sxs-lookup"><span data-stu-id="50e46-135">To display a progress indicator during processing of the operation, service providers use the progress object supplied by the client, if available, or a MAPI implementation (indicated when  _lpProgress_ is set to NULL).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="50e46-136">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="50e46-136">MFCMAPI reference</span></span>

<span data-ttu-id="50e46-137">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="50e46-137">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="50e46-138">**Files**</span><span class="sxs-lookup"><span data-stu-id="50e46-138">**Files**</span></span>|<span data-ttu-id="50e46-139">**Función**</span><span class="sxs-lookup"><span data-stu-id="50e46-139">**Function**</span></span>|<span data-ttu-id="50e46-140">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="50e46-140">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="50e46-141">MapiProgress.h y MapiProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="50e46-141">MapiProgress.h and MapiProgress.cpp</span></span>  <br/> |<span data-ttu-id="50e46-142">No aplicable</span><span class="sxs-lookup"><span data-stu-id="50e46-142">Not applicable</span></span>  <br/> |<span data-ttu-id="50e46-143">Si la configuración IMAPIProgress está habilitada, MFCMAPI pasará una implementación **IMAPIProgress** a todas las funciones que MFCMAPI invoca que aceptan una implementación.</span><span class="sxs-lookup"><span data-stu-id="50e46-143">If the IMAPIProgress setting is enabled, MFCMAPI will pass an **IMAPIProgress** implementation to all functions that MFCMAPI invokes that accept an implementation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50e46-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="50e46-144">See also</span></span>



[<span data-ttu-id="50e46-145">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="50e46-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="50e46-146">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="50e46-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

