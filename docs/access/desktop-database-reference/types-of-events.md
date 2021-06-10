---
title: Tipos de eventos (referencia de base de datos de escritorio de Access)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3bcf631ffc6c9b4b847af3f973114d6b271d26f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314157"
---
# <a name="types-of-events"></a><span data-ttu-id="1d4ee-102">Tipos de eventos</span><span class="sxs-lookup"><span data-stu-id="1d4ee-102">Types of events</span></span>


<span data-ttu-id="1d4ee-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d4ee-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="1d4ee-p101">Hay dos tipos básicos de eventos. Los "eventos Will", a los que se llama antes de iniciarse una operación, normalmente incluyen "Will" en su nombre; por ejemplo, **WillChangeRecordset** o **WillConnect**. Los eventos a los que se llama después de finalizar un evento suelen incluir "Complete" en su nombre; por ejemplo, **RecordChangeComplete** o **ConnectComplete**. Hay excepciones, como **InfoMessage**, pero éstas se producen después de finalizar la operación asociada.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-p101">There are two basic types of events. "Will Events," which are called before an operation starts, usually include "Will" in their names — for example, **WillChangeRecordset** or **WillConnect**. Events that are called after an event has been completed usually include "Complete" in their names — for example, **RecordChangeComplete** or **ConnectComplete**. Exceptions exist — such as **InfoMessage** — but these occur after the associated operation has completed.</span></span>

## <a name="will-events"></a><span data-ttu-id="1d4ee-108">Eventos Will</span><span class="sxs-lookup"><span data-stu-id="1d4ee-108">Will Events</span></span>

<span data-ttu-id="1d4ee-109">Los controladores de eventos a los que se llama antes de iniciarse la operación permiten examinar o modificar los parámetros de la operación y, a continuación, cancelar la operación o permitir que finalice.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-109">Event handlers called before the operation starts offer you the opportunity to examine or modify the operation parameters, and then either cancel the operation or allow it to complete.</span></span> <span data-ttu-id="1d4ee-110">Estas rutinas de controlador de eventos suelen tener nombres del formulario \**Will* Event\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-110">These event-handler routines usually have names of the form \**Will* Event\*\*\*.</span></span>

## <a name="complete-events"></a><span data-ttu-id="1d4ee-111">Eventos Complete</span><span class="sxs-lookup"><span data-stu-id="1d4ee-111">Complete Events</span></span>

<span data-ttu-id="1d4ee-112">Los controladores de eventos a los que se llama después de finalizar una operación pueden notificar a la aplicación la finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-112">Event handlers called after an operation completes can notify your application that an operation has concluded.</span></span> <span data-ttu-id="1d4ee-113">Estos controladores de eventos también reciben una notificación cuando un controlador de eventos Will cancela una operación pendiente.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-113">Such an event handler is also notified when a Will event handler cancels a pending operation.</span></span> <span data-ttu-id="1d4ee-114">Estas rutinas de controlador de eventos suelen tener nombres del formulario \***Event\*Complete**.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-114">These event-handler routines usually have names of the form \***Event\*Complete**.</span></span>

<span data-ttu-id="1d4ee-115">Los eventos Will y Complete suelen utilizarse emparejados.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-115">Will and Complete events are typically used in pairs.</span></span>

## <a name="other-events"></a><span data-ttu-id="1d4ee-116">Otros eventos</span><span class="sxs-lookup"><span data-stu-id="1d4ee-116">Other Events</span></span>

<span data-ttu-id="1d4ee-117">Los demás controladores de eventos, es decir, los eventos cuyos nombres no tienen el formato **Will\*Event**\* o \***Event\*Complete,** solo se llaman una vez completada una operación.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-117">The other event handlers — that is, events whose names are not of the form **Will\*Event**\* or \***Event\*Complete —** are called only after an operation completes.</span></span> <span data-ttu-id="1d4ee-118">Estos eventos son **Disconnect**, **EndOfRecordset** e **InfoMessage**.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-118">These events are **Disconnect**, **EndOfRecordset**, and **InfoMessage**.</span></span>

