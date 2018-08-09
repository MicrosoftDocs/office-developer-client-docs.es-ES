---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Admite reorganización de citas en una carpeta de calendario.
ms.openlocfilehash: 57ca59121f74c7b64a84282c7493e4aed3179f7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816246"
---
# <a name="iolkapptrebaser"></a><span data-ttu-id="17eae-103">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="17eae-103">IOlkApptRebaser</span></span>

<span data-ttu-id="17eae-104">Admite reorganización de citas en una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="17eae-104">Supports rebasing appointments in a calendar folder.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="17eae-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="17eae-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17eae-106">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="17eae-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="17eae-107">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="17eae-107">**IUnknown**</span></span> <br/> |
|<span data-ttu-id="17eae-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="17eae-108">Header file:</span></span>  <br/> |<span data-ttu-id="17eae-109">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="17eae-109">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="17eae-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="17eae-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="17eae-111">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="17eae-111">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="17eae-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="17eae-112">Called by:</span></span>  <br/> |<span data-ttu-id="17eae-113">Aplicaciones cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="17eae-113">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="17eae-114">Expuesto en:</span><span class="sxs-lookup"><span data-stu-id="17eae-114">Exposed on:</span></span>  <br/> |<span data-ttu-id="17eae-115">Objeto de reajuste de Outlook</span><span class="sxs-lookup"><span data-stu-id="17eae-115">Outlook rebasing object</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="17eae-116">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="17eae-116">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17eae-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="17eae-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="17eae-118">Se inicia una tarea de enumeración de la cita en una carpeta de calendario para buscar las citas que necesitan el reajuste.</span><span class="sxs-lookup"><span data-stu-id="17eae-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="17eae-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="17eae-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="17eae-120">Espera de enumeración de la cita en una carpeta de calendario para completar y devuelve una lista de citas esa necesidad de reajuste.</span><span class="sxs-lookup"><span data-stu-id="17eae-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="17eae-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="17eae-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="17eae-122">Inicia una tarea para modificar la cita base recibe una lista de citas, que generalmente se obtiene de **EndEnumerateAppointments**.</span><span class="sxs-lookup"><span data-stu-id="17eae-122">Begins a task for appointment rebasing given a list of appointments, usually obtained from **EndEnumerateAppointments**.</span></span>  <br/> |
|<span data-ttu-id="17eae-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="17eae-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="17eae-124">Espera a que cita el reajuste para completar y recupera los resultados.</span><span class="sxs-lookup"><span data-stu-id="17eae-124">Waits for appointment rebasing to complete and retrieves the results.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17eae-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="17eae-125">See also</span></span>

- [<span data-ttu-id="17eae-126">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="17eae-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

