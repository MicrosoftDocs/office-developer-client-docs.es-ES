---
title: Tipos de eventos (referencia de escritorio de la base de datos de Access)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ffb3bd48db4d8071e56553f4ea5bf79b83952466
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484998"
---
# <a name="types-of-events"></a><span data-ttu-id="23413-102">Tipos de eventos</span><span class="sxs-lookup"><span data-stu-id="23413-102">Types of Events</span></span>


<span data-ttu-id="23413-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="23413-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="23413-p101">Hay dos tipos básicos de eventos. Los "eventos Will", a los que se llama antes de iniciarse una operación, normalmente incluyen "Will" en su nombre; por ejemplo, **WillChangeRecordset** o **WillConnect**. Los eventos a los que se llama después de finalizar un evento suelen incluir "Complete" en su nombre; por ejemplo, **RecordChangeComplete** o **ConnectComplete**. Hay excepciones, como **InfoMessage**, pero éstas se producen después de finalizar la operación asociada.</span><span class="sxs-lookup"><span data-stu-id="23413-p101">There are two basic types of events. "Will Events," which are called before an operation starts, usually include "Will" in their names — for example, **WillChangeRecordset** or **WillConnect**. Events that are called after an event has been completed usually include "Complete" in their names — for example, **RecordChangeComplete** or **ConnectComplete**. Exceptions exist — such as **InfoMessage** — but these occur after the associated operation has completed.</span></span>

## <a name="will-events"></a><span data-ttu-id="23413-108">Eventos Will</span><span class="sxs-lookup"><span data-stu-id="23413-108">Will Events</span></span>

<span data-ttu-id="23413-109">Los controladores de eventos a los que se llama antes de iniciarse la operación permiten examinar o modificar los parámetros de la operación y, a continuación, cancelar la operación o permitir que finalice.</span><span class="sxs-lookup"><span data-stu-id="23413-109">Event handlers called before the operation starts offer you the opportunity to examine or modify the operation parameters, and then either cancel the operation or allow it to complete.</span></span> <span data-ttu-id="23413-110">Estas rutinas de controlador de eventos suele tener nombres de la forma \* evento \*\*\*\*será\*.</span><span class="sxs-lookup"><span data-stu-id="23413-110">These event-handler routines usually have names of the form \**Will*Event\*\*\*.</span></span>

## <a name="complete-events"></a><span data-ttu-id="23413-111">Eventos Complete</span><span class="sxs-lookup"><span data-stu-id="23413-111">Complete Events</span></span>

<span data-ttu-id="23413-112">Los controladores de eventos a los que se llama después de finalizar una operación pueden notificar a la aplicación la finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="23413-112">Event handlers called after an operation completes can notify your application that an operation has concluded.</span></span> <span data-ttu-id="23413-113">Estos controladores de eventos también reciben una notificación cuando un controlador de eventos Will cancela una operación pendiente.</span><span class="sxs-lookup"><span data-stu-id="23413-113">Such an event handler is also notified when a Will event handler cancels a pending operation.</span></span> <span data-ttu-id="23413-114">Estas rutinas de controlador de eventos suele tener nombres de la forma \***evento \* completo**.</span><span class="sxs-lookup"><span data-stu-id="23413-114">These event-handler routines usually have names of the form \***Event\*Complete**.</span></span>

<span data-ttu-id="23413-115">Los eventos Will y Complete suelen utilizarse emparejados.</span><span class="sxs-lookup"><span data-stu-id="23413-115">Will and Complete events are typically used in pairs.</span></span>

## <a name="other-events"></a><span data-ttu-id="23413-116">Otros eventos</span><span class="sxs-lookup"><span data-stu-id="23413-116">Other Events</span></span>

<span data-ttu-id="23413-117">Los otros controladores de eventos, es decir, los eventos cuyos nombres no tienen el formato **va a \* (evento)**\* o \***(evento) \* completo:** se llama sólo una vez que finaliza una operación.</span><span class="sxs-lookup"><span data-stu-id="23413-117">The other event handlers — that is, events whose names are not of the form **Will\*Event**\* or \***Event\*Complete —** are called only after an operation completes.</span></span> <span data-ttu-id="23413-118">Estos eventos son **Disconnect**, **EndOfRecordset** e **InfoMessage**.</span><span class="sxs-lookup"><span data-stu-id="23413-118">These events are **Disconnect**, **EndOfRecordset**, and **InfoMessage**.</span></span>

