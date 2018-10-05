---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Inicializa un objeto IOlkApptRebaser para su uso en reorganización de citas en calendarios de Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397544"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="9edc6-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="9edc6-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="9edc6-104">Inicializa un objeto [IOlkApptRebaser](iolkapptrebaser.md) para su uso en reorganización de citas en calendarios de Outlook.</span><span class="sxs-lookup"><span data-stu-id="9edc6-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9edc6-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="9edc6-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9edc6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9edc6-106">Header file:</span></span>  <br/> |<span data-ttu-id="9edc6-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="9edc6-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="9edc6-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9edc6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9edc6-109">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="9edc6-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="9edc6-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9edc6-110">Called by:</span></span>  <br/> |<span data-ttu-id="9edc6-111">Aplicaciones cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="9edc6-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="9edc6-112">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="9edc6-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="9edc6-113">**LPHRCREATEAPPTREBASER**</span><span class="sxs-lookup"><span data-stu-id="9edc6-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="9edc6-114">Punto de entrada del archivo DLL:</span><span class="sxs-lookup"><span data-stu-id="9edc6-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="9edc6-115">**HrCreateApptRebaser@44**</span><span class="sxs-lookup"><span data-stu-id="9edc6-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="9edc6-116">Par�metros</span><span class="sxs-lookup"><span data-stu-id="9edc6-116">Parameters</span></span>

<span data-ttu-id="9edc6-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9edc6-117">_ulFlags_</span></span>
  
> <span data-ttu-id="9edc6-118">[in] Requerido.</span><span class="sxs-lookup"><span data-stu-id="9edc6-118">[in] Required.</span></span> <span data-ttu-id="9edc6-119">Una máscara de bits de indicadores que se utilizan para controlar cómo se realiza la modificación de la base.</span><span class="sxs-lookup"><span data-stu-id="9edc6-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="9edc6-120">Las siguientes marcas pueden establecerse y se definen en tzmovelib.h:</span><span class="sxs-lookup"><span data-stu-id="9edc6-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="9edc6-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** — se restablecen los elementos de cita en la que el usuario es el organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="9edc6-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="9edc6-122">Tenga en cuenta que de forma predeterminada, esto hace que Outlook enviar actualizaciones de reunión a todos los asistentes a cualquier reunión que se restablecen.</span><span class="sxs-lookup"><span data-stu-id="9edc6-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="9edc6-123">Este indicador se puede combinar con **REBASE_FLAG_FORCE_NO_EX_UPDATES** o **REBASE_FLAG_FORCE_NO_UPDATES** para cambiar cómo se controlan las actualizaciones de la reunión.</span><span class="sxs-lookup"><span data-stu-id="9edc6-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="9edc6-124">**REBASE_FLAG_UPDATE_UNMARKED** — actualización de elementos de cita que no se han marcado con una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9edc6-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="9edc6-125">Si se especifica este indicador, el valor de *pTZMissing* se usa como la zona horaria que se crea un elemento en todos los elementos que no tienen datos de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9edc6-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="9edc6-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** — actualizar sólo los elementos de cita periódica.</span><span class="sxs-lookup"><span data-stu-id="9edc6-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="9edc6-127">**REBASE_FLAG_NO_UI** : no mostrar cualquier interfaz de usuario (UI), incluidos los cuadros de diálogo de inicio de sesión por lo general que se muestra al abrir un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9edc6-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="9edc6-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — no reajustar los elementos de cita que se producen en el pasado.</span><span class="sxs-lookup"><span data-stu-id="9edc6-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="9edc6-129">**REBASE_FLAG_FORCE_REBASE** : no comprobar el Organizador para reajustar las decisiones, pero reajustar los elementos de cita en la que el usuario es un asistente.</span><span class="sxs-lookup"><span data-stu-id="9edc6-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="9edc6-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** : enviar actualizaciones sólo si el usuario es el organizador y el destinatario no está conectado a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9edc6-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="9edc6-131">**REBASE_FLAG_FORCE_NO_UPDATES** : no enviar nunca actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="9edc6-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="9edc6-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** : reajustar sólo los elementos de cita de instancia única creado antes de que se ha aplicado la revisión.</span><span class="sxs-lookup"><span data-stu-id="9edc6-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="9edc6-133">**REBASE_FLAG_REPORTING_MODE** — no realmente reajustar, simplemente informe de elementos de cita que debería establecerse en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="9edc6-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="9edc6-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** : enviar actualizaciones de reunión a los recursos.</span><span class="sxs-lookup"><span data-stu-id="9edc6-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="9edc6-135">_pSession_</span><span class="sxs-lookup"><span data-stu-id="9edc6-135">_pSession_</span></span>
  
> <span data-ttu-id="9edc6-136">[in] Requerido.</span><span class="sxs-lookup"><span data-stu-id="9edc6-136">[in] Required.</span></span> <span data-ttu-id="9edc6-137">Un puntero a una interfaz de sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="9edc6-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="9edc6-138">_pCalendarMsgStore_</span><span class="sxs-lookup"><span data-stu-id="9edc6-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="9edc6-139">[in] Requerido.</span><span class="sxs-lookup"><span data-stu-id="9edc6-139">[in] Required.</span></span> <span data-ttu-id="9edc6-140">Un puntero a un almacén de mensajes que contiene los elementos de cita se restablecen.</span><span class="sxs-lookup"><span data-stu-id="9edc6-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="9edc6-141">_pCalendarFolder_</span><span class="sxs-lookup"><span data-stu-id="9edc6-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="9edc6-142">[in] Requerido.</span><span class="sxs-lookup"><span data-stu-id="9edc6-142">[in] Required.</span></span> <span data-ttu-id="9edc6-143">Un puntero a una carpeta de calendario que contiene los elementos de cita se restablecen.</span><span class="sxs-lookup"><span data-stu-id="9edc6-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="9edc6-144">_pwszUpdatePrefix_</span><span class="sxs-lookup"><span data-stu-id="9edc6-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="9edc6-145">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="9edc6-145">[in] Optional.</span></span> <span data-ttu-id="9edc6-146">Un puntero a una cadena que contiene el prefijo que se antepone en las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="9edc6-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="9edc6-147">Puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="9edc6-147">May be NULL.</span></span>
    
<span data-ttu-id="9edc6-148">_pftInstallDateUTC_</span><span class="sxs-lookup"><span data-stu-id="9edc6-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="9edc6-149">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="9edc6-149">[in] Optional.</span></span> <span data-ttu-id="9edc6-150">Fecha de instalación de la revisión de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9edc6-150">The time zone patch install date.</span></span> <span data-ttu-id="9edc6-151">Se usa únicamente si se establece la marca **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** .</span><span class="sxs-lookup"><span data-stu-id="9edc6-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="9edc6-152">_IExpansionDepth_</span><span class="sxs-lookup"><span data-stu-id="9edc6-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="9edc6-153">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="9edc6-153">[in] Optional.</span></span> <span data-ttu-id="9edc6-154">La profundidad de expansión al expandir listas de distribución para excluir a los destinatarios conectado al servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9edc6-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="9edc6-155">Sólo se utiliza si se establece la marca **REBASE_FLAG_FORCE_NO_EX_UPDATES** .</span><span class="sxs-lookup"><span data-stu-id="9edc6-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="9edc6-156">_pTZTo_</span><span class="sxs-lookup"><span data-stu-id="9edc6-156">_pTZTo_</span></span>
  
> <span data-ttu-id="9edc6-157">[in] Requerido.</span><span class="sxs-lookup"><span data-stu-id="9edc6-157">[in] Required.</span></span> <span data-ttu-id="9edc6-158">Un puntero a una estructura **TZDEFINITION** que describe la zona horaria que se restablecen a.</span><span class="sxs-lookup"><span data-stu-id="9edc6-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="9edc6-159">**TZDEFINITION** se define en tzmovelib.</span><span class="sxs-lookup"><span data-stu-id="9edc6-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="9edc6-160">pTZMissing</span><span class="sxs-lookup"><span data-stu-id="9edc6-160">pTZMissing</span></span>
  
> <span data-ttu-id="9edc6-161">[in] Requerido.</span><span class="sxs-lookup"><span data-stu-id="9edc6-161">[in] Required.</span></span> <span data-ttu-id="9edc6-162">Un puntero a una estructura **TZDEFINITION** que describe la zona horaria para se supone si no se ha marcado información de zona horaria en un elemento.</span><span class="sxs-lookup"><span data-stu-id="9edc6-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="9edc6-163">No debe ser NULL, pero sólo utiliza si se establece la marca **REBASE_FLAG_UPDATE_UNMARKED** .</span><span class="sxs-lookup"><span data-stu-id="9edc6-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="9edc6-164">_ppError_</span><span class="sxs-lookup"><span data-stu-id="9edc6-164">_ppError_</span></span>
  
> <span data-ttu-id="9edc6-165">[out] Un puntero a un puntero a una estructura **MAPIERROR** que contiene información de versión, el componente y el contexto para el error.</span><span class="sxs-lookup"><span data-stu-id="9edc6-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="9edc6-166">Puede ser NULL si no hay información de error extendidos se desea obtener.</span><span class="sxs-lookup"><span data-stu-id="9edc6-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="9edc6-167">Gratis con [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9edc6-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="9edc6-168">_ppApptRebase_</span><span class="sxs-lookup"><span data-stu-id="9edc6-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="9edc6-169">[out] Un puntero a un puntero a la interfaz devuelta de **IOlkApptRebaser** .</span><span class="sxs-lookup"><span data-stu-id="9edc6-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="9edc6-170">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="9edc6-170">Return values</span></span>

<span data-ttu-id="9edc6-171">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="9edc6-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9edc6-172">Notas</span><span class="sxs-lookup"><span data-stu-id="9edc6-172">Remarks</span></span>

<span data-ttu-id="9edc6-173">Cuando se usa [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) para buscar la dirección de esta función en tzmovelib.dll, especifique **HrCreateApptRebaser@44** como el nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="9edc6-173">When using [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="9edc6-174">No todas las marcas son válidos en combinación con cada una de las demás.</span><span class="sxs-lookup"><span data-stu-id="9edc6-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="9edc6-175">Para obtener más información acerca de las distintas opciones, consulte la sección "Glosario de opciones de línea de comandos para la herramienta de actualización de datos de zona horaria de Outlook" en [KB 931667: cómo los cambios de zona horaria de direcciones mediante la herramienta de actualización de datos de zona horaria para Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span><span class="sxs-lookup"><span data-stu-id="9edc6-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9edc6-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="9edc6-176">See also</span></span>

- [<span data-ttu-id="9edc6-177">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="9edc6-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

