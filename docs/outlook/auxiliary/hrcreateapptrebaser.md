---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Inicializa un objeto IOlkApptRebaser para su uso en la reajuste de citas en los calendarios de Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317615"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="bd68d-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="bd68d-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="bd68d-104">Inicializa un objeto [IOlkApptRebaser](iolkapptrebaser.md) para su uso en la reajuste de citas en los calendarios de Outlook.</span><span class="sxs-lookup"><span data-stu-id="bd68d-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="bd68d-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="bd68d-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd68d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bd68d-106">Header file:</span></span>  <br/> |<span data-ttu-id="bd68d-107">tzmovelib. h</span><span class="sxs-lookup"><span data-stu-id="bd68d-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="bd68d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="bd68d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bd68d-109">tzmovelib. dll</span><span class="sxs-lookup"><span data-stu-id="bd68d-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="bd68d-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="bd68d-110">Called by:</span></span>  <br/> |<span data-ttu-id="bd68d-111">Aplicaciones cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="bd68d-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="bd68d-112">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="bd68d-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="bd68d-113">**LPHRCREATEAPPTREBASER**</span><span class="sxs-lookup"><span data-stu-id="bd68d-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="bd68d-114">Punto de entrada de DLL:</span><span class="sxs-lookup"><span data-stu-id="bd68d-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="bd68d-115">**HrCreateApptRebaser @ 44**</span><span class="sxs-lookup"><span data-stu-id="bd68d-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a><span data-ttu-id="bd68d-116">Parameters</span><span class="sxs-lookup"><span data-stu-id="bd68d-116">Parameters</span></span>

<span data-ttu-id="bd68d-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bd68d-117">_ulFlags_</span></span>
  
> <span data-ttu-id="bd68d-118">[in] Requerido.</span><span class="sxs-lookup"><span data-stu-id="bd68d-118">[in] Required.</span></span> <span data-ttu-id="bd68d-119">Máscara de la máscara usada para controlar cómo se realiza el reajuste.</span><span class="sxs-lookup"><span data-stu-id="bd68d-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="bd68d-120">Se pueden establecer y definir los siguientes indicadores en tzmovelib. h:</span><span class="sxs-lookup"><span data-stu-id="bd68d-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="bd68d-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** : elementos de cita en los que el usuario es el organizador de la reunión en el que se rebasa.</span><span class="sxs-lookup"><span data-stu-id="bd68d-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="bd68d-122">Tenga en cuenta que, de forma predeterminada, Outlook envía actualizaciones de reunión a todos los asistentes de las reuniones que se rebasen.</span><span class="sxs-lookup"><span data-stu-id="bd68d-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="bd68d-123">Puede combinar este indicador con **REBASE_FLAG_FORCE_NO_EX_UPDATES** o **REBASE_FLAG_FORCE_NO_UPDATES** para cambiar la forma en que se administran las actualizaciones de reunión.</span><span class="sxs-lookup"><span data-stu-id="bd68d-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="bd68d-124">**REBASE_FLAG_UPDATE_UNMARKED** : actualizar elementos de cita que no se han marcado con una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="bd68d-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="bd68d-125">Si se especifica este indicador, se usa el valor *pTZMissing* como la zona horaria en la que se crea un elemento para todos los elementos que no tienen datos de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="bd68d-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="bd68d-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** : actualizar solo los elementos de cita periódicos.</span><span class="sxs-lookup"><span data-stu-id="bd68d-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="bd68d-127">**REBASE_FLAG_NO_UI** — no mostrar ninguna interfaz de usuario (UI), incluidos los cuadros de diálogo de inicio de sesión que se suelen mostrar al abrir un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bd68d-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="bd68d-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** : no se rebasen los elementos de cita que se produjeron en el pasado.</span><span class="sxs-lookup"><span data-stu-id="bd68d-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="bd68d-129">**REBASE_FLAG_FORCE_REBASE** : no comprueba el organizador para las decisiones de reajuste, sino que rebase los elementos de cita en los que el usuario es un asistente.</span><span class="sxs-lookup"><span data-stu-id="bd68d-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="bd68d-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** : enviar actualizaciones solo si el usuario es el organizador y el destinatario no está conectado a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="bd68d-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="bd68d-131">**REBASE_FLAG_FORCE_NO_UPDATES** : no enviar nunca actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="bd68d-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="bd68d-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** : sólo se rebasen los elementos de cita de instancia única creados antes de que se aplicara la revisión.</span><span class="sxs-lookup"><span data-stu-id="bd68d-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="bd68d-133">**REBASE_FLAG_REPORTING_MODE** : no se rebasa realmente, solo notificar los elementos de cita que se rebasarían.</span><span class="sxs-lookup"><span data-stu-id="bd68d-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="bd68d-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** : enviar actualizaciones de reunión a los recursos.</span><span class="sxs-lookup"><span data-stu-id="bd68d-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="bd68d-135">_pSession_</span><span class="sxs-lookup"><span data-stu-id="bd68d-135">_pSession_</span></span>
  
> <span data-ttu-id="bd68d-136">[in] Requerido.</span><span class="sxs-lookup"><span data-stu-id="bd68d-136">[in] Required.</span></span> <span data-ttu-id="bd68d-137">Un puntero a una interfaz de sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="bd68d-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="bd68d-138">_pCalendarMsgStore_</span><span class="sxs-lookup"><span data-stu-id="bd68d-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="bd68d-139">[in] Requerido.</span><span class="sxs-lookup"><span data-stu-id="bd68d-139">[in] Required.</span></span> <span data-ttu-id="bd68d-140">Un puntero a un almacén de mensajes que contiene elementos de cita que se van a rebasar.</span><span class="sxs-lookup"><span data-stu-id="bd68d-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="bd68d-141">_pCalendarFolder_</span><span class="sxs-lookup"><span data-stu-id="bd68d-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="bd68d-142">[in] Requerido.</span><span class="sxs-lookup"><span data-stu-id="bd68d-142">[in] Required.</span></span> <span data-ttu-id="bd68d-143">Un puntero a una carpeta de calendario que contiene los elementos de cita que se van a rebasar.</span><span class="sxs-lookup"><span data-stu-id="bd68d-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="bd68d-144">_pwszUpdatePrefix_</span><span class="sxs-lookup"><span data-stu-id="bd68d-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="bd68d-145">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="bd68d-145">[in] Optional.</span></span> <span data-ttu-id="bd68d-146">Un puntero a una cadena que contiene el prefijo que se va a anteponer a las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="bd68d-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="bd68d-147">Puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="bd68d-147">May be NULL.</span></span>
    
<span data-ttu-id="bd68d-148">_pftInstallDateUTC_</span><span class="sxs-lookup"><span data-stu-id="bd68d-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="bd68d-149">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="bd68d-149">[in] Optional.</span></span> <span data-ttu-id="bd68d-150">Fecha de instalación de la revisión de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="bd68d-150">The time zone patch install date.</span></span> <span data-ttu-id="bd68d-151">Solo se usa si se establece la marca **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** .</span><span class="sxs-lookup"><span data-stu-id="bd68d-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="bd68d-152">_IExpansionDepth_</span><span class="sxs-lookup"><span data-stu-id="bd68d-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="bd68d-153">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="bd68d-153">[in] Optional.</span></span> <span data-ttu-id="bd68d-154">La profundidad de expansión al expandir las listas de distribución para excluir a los destinatarios conectados a Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bd68d-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="bd68d-155">Solo se usa si se establece la marca **REBASE_FLAG_FORCE_NO_EX_UPDATES** .</span><span class="sxs-lookup"><span data-stu-id="bd68d-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="bd68d-156">_pTZTo_</span><span class="sxs-lookup"><span data-stu-id="bd68d-156">_pTZTo_</span></span>
  
> <span data-ttu-id="bd68d-157">[in] Requerido.</span><span class="sxs-lookup"><span data-stu-id="bd68d-157">[in] Required.</span></span> <span data-ttu-id="bd68d-158">Puntero a una estructura **TZDEFINITION** que describe la zona horaria a la que se va a rebasar.</span><span class="sxs-lookup"><span data-stu-id="bd68d-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="bd68d-159">**TZDEFINITION** se define en tzmovelib.</span><span class="sxs-lookup"><span data-stu-id="bd68d-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="bd68d-160">pTZMissing</span><span class="sxs-lookup"><span data-stu-id="bd68d-160">pTZMissing</span></span>
  
> <span data-ttu-id="bd68d-161">[in] Requerido.</span><span class="sxs-lookup"><span data-stu-id="bd68d-161">[in] Required.</span></span> <span data-ttu-id="bd68d-162">Un puntero a una estructura **TZDEFINITION** que describe la zona horaria que se va a asumir si la información de la zona horaria no se marca en un elemento.</span><span class="sxs-lookup"><span data-stu-id="bd68d-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="bd68d-163">No debe ser NULL, pero solo se usa si se ha establecido la marca **REBASE_FLAG_UPDATE_UNMARKED** .</span><span class="sxs-lookup"><span data-stu-id="bd68d-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="bd68d-164">_ppError_</span><span class="sxs-lookup"><span data-stu-id="bd68d-164">_ppError_</span></span>
  
> <span data-ttu-id="bd68d-165">contempla Un puntero a un puntero a una estructura **MAPIERROR** que contiene información de versión, componente y contexto para el error.</span><span class="sxs-lookup"><span data-stu-id="bd68d-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="bd68d-166">Puede ser NULL si no se desea ninguna información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="bd68d-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="bd68d-167">Gratis con [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="bd68d-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="bd68d-168">_ppApptRebase_</span><span class="sxs-lookup"><span data-stu-id="bd68d-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="bd68d-169">contempla Un puntero a un puntero a la interfaz **IOlkApptRebaser** devuelta.</span><span class="sxs-lookup"><span data-stu-id="bd68d-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="bd68d-170">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="bd68d-170">Return values</span></span>

<span data-ttu-id="bd68d-171">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="bd68d-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd68d-172">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bd68d-172">Remarks</span></span>

<span data-ttu-id="bd68d-173">Al utilizar [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) para buscar la dirección de esta función en tzmovelib. dll, especifique **HrCreateApptRebaser @ 44** como nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="bd68d-173">When using [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="bd68d-174">No todas las marcas son válidas en combinación entre sí.</span><span class="sxs-lookup"><span data-stu-id="bd68d-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="bd68d-175">Para obtener más información acerca de las distintas opciones, consulte la sección "Glosario de opciones de línea de comandos para la herramienta de actualizar datos de zona horaria de Outlook" en [KB 931667: Cómo dirigir los cambios de zona horaria mediante la herramienta de actualización de datos de zona horaria para Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span><span class="sxs-lookup"><span data-stu-id="bd68d-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bd68d-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd68d-176">See also</span></span>

- [<span data-ttu-id="bd68d-177">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="bd68d-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

