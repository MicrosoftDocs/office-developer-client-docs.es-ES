---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350970"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="8012b-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="8012b-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="8012b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8012b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8012b-105">Establece los criterios de búsqueda para el contenedor.</span><span class="sxs-lookup"><span data-stu-id="8012b-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8012b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8012b-106">Parameters</span></span>

 <span data-ttu-id="8012b-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="8012b-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="8012b-108">a Un puntero a una estructura [SRestriction](srestriction.md) que define los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8012b-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="8012b-109">Si se pasa NULL en el parámetro _lpRestriction_ , se vuelven a usar los criterios de búsqueda que se usaron más recientemente para este contenedor.</span><span class="sxs-lookup"><span data-stu-id="8012b-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="8012b-110">No se debe pasar NULL en _lpRestriction_ para la primera búsqueda en un contenedor.</span><span class="sxs-lookup"><span data-stu-id="8012b-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="8012b-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="8012b-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="8012b-112">a Un puntero a una matriz de identificadores de entrada que representan los contenedores que se van a incluir en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8012b-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="8012b-113">Si un cliente pasa NULL en el parámetro _lpContainerList_ , los identificadores de entrada usados más recientemente para buscar en este contenedor se usan para la nueva búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8012b-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="8012b-114">Un cliente no debe pasar NULL en _lpContainerList_ para la primera búsqueda en un contenedor.</span><span class="sxs-lookup"><span data-stu-id="8012b-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="8012b-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="8012b-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="8012b-116">a Una máscara de máscara de marcas que controlan cómo se realiza la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8012b-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="8012b-117">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="8012b-117">The following flags can be set:</span></span>
    
<span data-ttu-id="8012b-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="8012b-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="8012b-119">La búsqueda debe ejecutarse con prioridad normal en relación con otras búsquedas.</span><span class="sxs-lookup"><span data-stu-id="8012b-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="8012b-120">Esta marca no se puede establecer al mismo tiempo que la marca FOREGROUND_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="8012b-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="8012b-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="8012b-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="8012b-122">La búsqueda debe ejecutarse con prioridad alta en relación con otras búsquedas.</span><span class="sxs-lookup"><span data-stu-id="8012b-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="8012b-123">Esta marca no se puede establecer al mismo tiempo que la marca BACKGROUND_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="8012b-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="8012b-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="8012b-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="8012b-125">La búsqueda no debe usar la indización de contenido para buscar entradas coincidentes.</span><span class="sxs-lookup"><span data-stu-id="8012b-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="8012b-126">Esta marca solo es válida para los almacenes de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8012b-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="8012b-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="8012b-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="8012b-128">La búsqueda debe incluir los contenedores especificados en el parámetro _lpContainerList_ y todos sus contenedores secundarios.</span><span class="sxs-lookup"><span data-stu-id="8012b-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="8012b-129">Esta marca no se puede establecer al mismo tiempo que la marca SHALLOW_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="8012b-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="8012b-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="8012b-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="8012b-131">La búsqueda debe iniciarse si esta es la primera llamada a **SetSearchCriteria**, o reiniciarse si la búsqueda está inactiva.</span><span class="sxs-lookup"><span data-stu-id="8012b-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="8012b-132">Esta marca no se puede establecer al mismo tiempo que la marca STOP_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="8012b-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="8012b-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="8012b-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="8012b-134">La búsqueda solo debe buscar en los contenedores especificados en el parámetro _lpContainerList_ para las entradas coincidentes.</span><span class="sxs-lookup"><span data-stu-id="8012b-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="8012b-135">Esta marca no se puede establecer al mismo tiempo que la marca RECURSIVE_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="8012b-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="8012b-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="8012b-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="8012b-137">La búsqueda se debe detener.</span><span class="sxs-lookup"><span data-stu-id="8012b-137">The search should be stopped.</span></span> <span data-ttu-id="8012b-138">Esta marca no se puede establecer al mismo tiempo que la marca RESTART_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="8012b-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8012b-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8012b-139">Return value</span></span>

<span data-ttu-id="8012b-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="8012b-140">S_OK</span></span> 
  
> <span data-ttu-id="8012b-141">Los criterios de búsqueda se establecieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="8012b-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="8012b-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="8012b-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="8012b-143">El proveedor de servicios no admite los criterios de búsqueda especificados.</span><span class="sxs-lookup"><span data-stu-id="8012b-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8012b-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8012b-144">Remarks</span></span>

<span data-ttu-id="8012b-145">El método **IMAPIContainer:: SetSearchCriteria** establece criterios de búsqueda para un contenedor que admite búsquedas, normalmente una carpeta de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8012b-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="8012b-146">Una carpeta de resultados de búsqueda contiene vínculos a los mensajes que cumplen los criterios de búsqueda; los mensajes reales todavía se almacenan en sus ubicaciones originales.</span><span class="sxs-lookup"><span data-stu-id="8012b-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="8012b-147">Los únicos datos únicos que contiene una carpeta de resultados de búsqueda son la tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="8012b-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="8012b-148">La tabla de contenido de una carpeta de resultados de búsqueda tiene el contenido combinado del almacén de mensajes después de que se haya aplicado la restricción de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8012b-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="8012b-149">Una operación de búsqueda solo funciona en esta tabla contenido combinado; no busca en otras carpetas de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8012b-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="8012b-150">Los resultados de la búsqueda solo devuelven los mensajes que coinciden con los criterios de búsqueda; no se devuelve la jerarquía de carpetas.</span><span class="sxs-lookup"><span data-stu-id="8012b-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="8012b-151">El control se devuelve al cliente cuando finaliza la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8012b-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8012b-152">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="8012b-152">Notes to implementers</span></span>

<span data-ttu-id="8012b-153">Los contenedores de la libreta de direcciones establecen criterios de búsqueda mediante la aplicación de restricciones a sus tablas de contenido.</span><span class="sxs-lookup"><span data-stu-id="8012b-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="8012b-154">Para obtener más información acerca de los criterios de búsqueda y los contenedores de la libreta de direcciones, consulte [implementación de búsqueda avanzada](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="8012b-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="8012b-155">Debe admitir operaciones de apertura, copia, movimiento y eliminación en los mensajes de las carpetas de resultados de búsqueda, no en la propia carpeta de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8012b-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="8012b-156">No permita que los mensajes se creen dentro o se copien en una carpeta de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8012b-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8012b-157">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="8012b-157">Notes to callers</span></span>

<span data-ttu-id="8012b-158">Para buscar destinatarios de mensajes, establezca _lpRestriction_ para que apunte a una restricción de subobjeto con el miembro **ulSubObject** en la estructura [SSubRestriction](ssubrestriction.md) establecida en **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8012b-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="8012b-159">Para buscar datos adjuntos, establezca el miembro **ulSubObject** en **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8012b-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="8012b-160">Establezca el miembro **lpRes** para que apunte a una restricción de propiedad que describa los criterios de búsqueda de los destinatarios o datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8012b-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="8012b-161">Por ejemplo, para buscar datos adjuntos de archivo con la extensión. MSS, establezca **ulSubObject** en **PR_MESSAGE_ATTACHMENTS** y **lpRes** en una restricción de propiedad que coincida con **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) ) con. MSS.</span><span class="sxs-lookup"><span data-stu-id="8012b-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="8012b-162">Si se establece la marca FOREGROUND_SEARCH en el parámetro _ulSearchFlags_ , se podría producir una disminución del rendimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="8012b-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="8012b-163">Puede usar **SetSearchCriteria** para cambiar los criterios de búsqueda de una búsqueda que ya está en curso.</span><span class="sxs-lookup"><span data-stu-id="8012b-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="8012b-164">Puede especificar nuevas restricciones, nuevas listas de carpetas para buscar y una nueva prioridad de búsqueda, como la actualización de una búsqueda a una prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="8012b-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="8012b-165">Los cambios en la prioridad de búsqueda no provocan que una búsqueda existente se reinicie, pero otros cambios en los criterios de búsqueda pueden.</span><span class="sxs-lookup"><span data-stu-id="8012b-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="8012b-166">Cuando se usa una carpeta de resultados de búsqueda, puede eliminar la carpeta o dejarla abierta para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="8012b-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="8012b-167">Si elimina la carpeta de resultados de búsqueda, sólo se eliminan los vínculos de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8012b-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="8012b-168">Los mensajes reales permanecen en sus carpetas principales.</span><span class="sxs-lookup"><span data-stu-id="8012b-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="8012b-169">Para obtener más información acerca de las carpetas de resultados de búsqueda, consulte [carpetas de búsqueda MAPI](mapi-search-folders.md).</span><span class="sxs-lookup"><span data-stu-id="8012b-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8012b-170">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8012b-170">MFCMAPI reference</span></span>

<span data-ttu-id="8012b-171">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="8012b-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8012b-172">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="8012b-172">**File**</span></span>|<span data-ttu-id="8012b-173">**Función**</span><span class="sxs-lookup"><span data-stu-id="8012b-173">**Function**</span></span>|<span data-ttu-id="8012b-174">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="8012b-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8012b-175">HierarchyTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="8012b-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="8012b-176">CHierarchyTableDlg:: OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="8012b-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="8012b-177">MFCMAPI usa el método **IMAPIContainer:: SetSearchCriteria** para escribir los criterios de búsqueda de una carpeta después de que un usuario la haya editado.</span><span class="sxs-lookup"><span data-stu-id="8012b-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8012b-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="8012b-178">See also</span></span>



[<span data-ttu-id="8012b-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="8012b-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="8012b-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="8012b-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="8012b-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="8012b-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="8012b-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="8012b-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="8012b-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="8012b-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="8012b-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="8012b-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="8012b-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="8012b-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="8012b-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8012b-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="8012b-187">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="8012b-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

