---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Admite el reajuste de citas en una carpeta de calendario.
ms.openlocfilehash: cf4f7c790a8561f149160c83418a0d5ebd91a455
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321864"
---
# <a name="iolkapptrebaser"></a><span data-ttu-id="68ba1-103">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="68ba1-103">IOlkApptRebaser</span></span>

<span data-ttu-id="68ba1-104">Admite el reajuste de citas en una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="68ba1-104">Supports rebasing appointments in a calendar folder.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="68ba1-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="68ba1-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68ba1-106">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="68ba1-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="68ba1-107">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="68ba1-107">**IUnknown**</span></span> <br/> |
|<span data-ttu-id="68ba1-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="68ba1-108">Header file:</span></span>  <br/> |<span data-ttu-id="68ba1-109">tzmovelib. h</span><span class="sxs-lookup"><span data-stu-id="68ba1-109">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="68ba1-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="68ba1-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="68ba1-111">tzmovelib. dll</span><span class="sxs-lookup"><span data-stu-id="68ba1-111">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="68ba1-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="68ba1-112">Called by:</span></span>  <br/> |<span data-ttu-id="68ba1-113">Aplicaciones cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="68ba1-113">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="68ba1-114">Expuesto el:</span><span class="sxs-lookup"><span data-stu-id="68ba1-114">Exposed on:</span></span>  <br/> |<span data-ttu-id="68ba1-115">Objeto de reajuste de Outlook</span><span class="sxs-lookup"><span data-stu-id="68ba1-115">Outlook rebasing object</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="68ba1-116">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="68ba1-116">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68ba1-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="68ba1-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="68ba1-118">Se inicia una tarea de enumeración de la cita en una carpeta de calendario para buscar las citas que necesitan el reajuste.</span><span class="sxs-lookup"><span data-stu-id="68ba1-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="68ba1-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="68ba1-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="68ba1-120">Espera de enumeración de la cita en una carpeta de calendario para completar y devuelve una lista de citas esa necesidad de reajuste.</span><span class="sxs-lookup"><span data-stu-id="68ba1-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="68ba1-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="68ba1-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="68ba1-122">Comienza una tarea para el reajuste de la cita dada una lista de citas, normalmente obtenida de **EndEnumerateAppointments**.</span><span class="sxs-lookup"><span data-stu-id="68ba1-122">Begins a task for appointment rebasing given a list of appointments, usually obtained from **EndEnumerateAppointments**.</span></span>  <br/> |
|<span data-ttu-id="68ba1-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="68ba1-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="68ba1-124">Espera a que cita el reajuste para completar y recupera los resultados.</span><span class="sxs-lookup"><span data-stu-id="68ba1-124">Waits for appointment rebasing to complete and retrieves the results.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68ba1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="68ba1-125">See also</span></span>

- [<span data-ttu-id="68ba1-126">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="68ba1-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

