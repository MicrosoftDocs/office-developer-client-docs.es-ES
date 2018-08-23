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
ms.openlocfilehash: 42d09fd92edf4dc221b73dac4948e78a7c6898ac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589332"
---
# <a name="imapiprogress--iunknown"></a><span data-ttu-id="9923a-103">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9923a-103">IMAPIProgress : IUnknown</span></span>

  
  
<span data-ttu-id="9923a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9923a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9923a-105">Implementa un objeto de progreso que proporciona a las aplicaciones de cliente con un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="9923a-105">Implements a progress object that provides client applications with a progress indicator.</span></span> <span data-ttu-id="9923a-106">Un indicador de progreso es una presentación de la interfaz de usuario que muestra el porcentaje de finalización de una operación, como copiar carpetas entre almacenes de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9923a-106">A progress indicator is a user-interface display that shows the percentage of completion of an operation, such as copying folders between message stores.</span></span> <span data-ttu-id="9923a-107">Las aplicaciones MAPI y cliente implementan objetos de progreso y proveedores de servicios de usan.</span><span class="sxs-lookup"><span data-stu-id="9923a-107">MAPI and client applications implement progress objects and service providers use them.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9923a-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9923a-108">Header file:</span></span>  <br/> |<span data-ttu-id="9923a-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9923a-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9923a-110">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="9923a-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="9923a-111">Objetos de progreso</span><span class="sxs-lookup"><span data-stu-id="9923a-111">Progress objects</span></span>  <br/> |
|<span data-ttu-id="9923a-112">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="9923a-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="9923a-113">MAPI y las aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="9923a-113">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="9923a-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9923a-114">Called by:</span></span>  <br/> |<span data-ttu-id="9923a-115">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="9923a-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="9923a-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="9923a-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9923a-117">IID_IMAPIProgress</span><span class="sxs-lookup"><span data-stu-id="9923a-117">IID_IMAPIProgress</span></span>  <br/> |
|<span data-ttu-id="9923a-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="9923a-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="9923a-119">LPMAPIPROGRESS</span><span class="sxs-lookup"><span data-stu-id="9923a-119">LPMAPIPROGRESS</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9923a-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="9923a-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9923a-121">Progress</span><span class="sxs-lookup"><span data-stu-id="9923a-121">Progress</span></span>](imapiprogress-progress.md) <br/> |<span data-ttu-id="9923a-122">Actualiza el indicador de progreso con una visualización del progreso de la medida que se realiza hacia la finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="9923a-122">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span>  <br/> |
|[<span data-ttu-id="9923a-123">GetFlags</span><span class="sxs-lookup"><span data-stu-id="9923a-123">GetFlags</span></span>](imapiprogress-getflags.md) <br/> |<span data-ttu-id="9923a-124">Devuelve marca configuración desde el objeto de progreso para el nivel de operación en la que se calcula la información de progreso.</span><span class="sxs-lookup"><span data-stu-id="9923a-124">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>  <br/> |
|[<span data-ttu-id="9923a-125">GetMax</span><span class="sxs-lookup"><span data-stu-id="9923a-125">GetMax</span></span>](imapiprogress-getmax.md) <br/> |<span data-ttu-id="9923a-126">Devuelve el número máximo de elementos en la operación de progreso que se muestra la información.</span><span class="sxs-lookup"><span data-stu-id="9923a-126">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="9923a-127">GetMin</span><span class="sxs-lookup"><span data-stu-id="9923a-127">GetMin</span></span>](imapiprogress-getmin.md) <br/> |<span data-ttu-id="9923a-128">Devuelve el valor mínimo en el método [SetLimits](imapiprogress-setlimits.md) de progreso que se muestra la información.</span><span class="sxs-lookup"><span data-stu-id="9923a-128">Returns the minimum value in the [SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="9923a-129">SetLimits</span><span class="sxs-lookup"><span data-stu-id="9923a-129">SetLimits</span></span>](imapiprogress-setlimits.md) <br/> |<span data-ttu-id="9923a-130">Establece los límites superiores e inferiores para el número de elementos de la operación y los indicadores que controlan cómo se calcula la información de progreso de la operación.</span><span class="sxs-lookup"><span data-stu-id="9923a-130">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9923a-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9923a-131">Remarks</span></span>

<span data-ttu-id="9923a-132">MAPI incluye un parámetro _lpProgress_ en muchos de los métodos que realizan operaciones potencialmente prolongadas.</span><span class="sxs-lookup"><span data-stu-id="9923a-132">MAPI includes an  _lpProgress_ parameter in many of the methods that perform potentially lengthy operations.</span></span>  <span data-ttu-id="9923a-133">_lpProgress_ apunta a una implementación de cliente de un objeto de progreso.</span><span class="sxs-lookup"><span data-stu-id="9923a-133">_lpProgress_ points to a client implementation of a progress object.</span></span> <span data-ttu-id="9923a-134">Los clientes que implementan la interfaz **IMAPIProgress** establezca este parámetro para que apunte a su implementación; los clientes que implementan **IMAPIProgress** establecer el parámetro en NULL.</span><span class="sxs-lookup"><span data-stu-id="9923a-134">Clients that implement the **IMAPIProgress** interface set this parameter to point to their implementation; clients that do not implement **IMAPIProgress** set the parameter to NULL.</span></span> <span data-ttu-id="9923a-135">Para mostrar un indicador de progreso durante el procesamiento de la operación, proveedores de servicios de usar el objeto de progreso proporcionada por el cliente, si está disponible, o una implementación de MAPI (indicado cuando _lpProgress_ se establece en NULL).</span><span class="sxs-lookup"><span data-stu-id="9923a-135">To display a progress indicator during processing of the operation, service providers use the progress object supplied by the client, if available, or a MAPI implementation (indicated when  _lpProgress_ is set to NULL).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9923a-136">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9923a-136">MFCMAPI reference</span></span>

<span data-ttu-id="9923a-137">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="9923a-137">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9923a-138">**Archivos**</span><span class="sxs-lookup"><span data-stu-id="9923a-138">**Files**</span></span>|<span data-ttu-id="9923a-139">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="9923a-139">**Function**</span></span>|<span data-ttu-id="9923a-140">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="9923a-140">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9923a-141">MapiProgress.h y MapiProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="9923a-141">MapiProgress.h and MapiProgress.cpp</span></span>  <br/> |<span data-ttu-id="9923a-142">No disponible</span><span class="sxs-lookup"><span data-stu-id="9923a-142">Not applicable</span></span>  <br/> |<span data-ttu-id="9923a-143">Si está habilitada la configuración de IMAPIProgress, MFCMAPI pasará una implementación de **IMAPIProgress** a todas las funciones que invoca MFCMAPI que aceptan una implementación.</span><span class="sxs-lookup"><span data-stu-id="9923a-143">If the IMAPIProgress setting is enabled, MFCMAPI will pass an **IMAPIProgress** implementation to all functions that MFCMAPI invokes that accept an implementation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9923a-144">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9923a-144">See also</span></span>



[<span data-ttu-id="9923a-145">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="9923a-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="9923a-146">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="9923a-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

