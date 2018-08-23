---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4ca565f97851a2efe2f3279f062f6ea89a4c6326
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579966"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="ccdc4-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="ccdc4-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="ccdc4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccdc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccdc4-105">Obtiene los criterios de búsqueda para el contenedor.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="ccdc4-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ccdc4-106">Parameters</span></span>

 <span data-ttu-id="ccdc4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ccdc4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ccdc4-108">[entrada] Una máscara de bits de indicadores que controla el tipo de las cadenas que se pasan en.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="ccdc4-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="ccdc4-109">The following flag can be set:</span></span>
    
<span data-ttu-id="ccdc4-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ccdc4-111">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ccdc4-112">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ccdc4-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="ccdc4-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="ccdc4-114">[out] Un puntero a un puntero a una estructura [SRestriction](srestriction.md) que define los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="ccdc4-115">Si una aplicación cliente pasa NULL en el parámetro _lppRestriction_ , **es posible GetSearchCriteria** no devuelve una estructura **SRestriction** .</span><span class="sxs-lookup"><span data-stu-id="ccdc4-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="ccdc4-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="ccdc4-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="ccdc4-117">[out] Un puntero a un puntero a una matriz de identificadores de entrada que representan los contenedores que se deben incluir en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="ccdc4-118">Si un cliente pasa NULL en el parámetro _lppContainerList_ , **es posible GetSearchCriteria** no devuelve una matriz de identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="ccdc4-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="ccdc4-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="ccdc4-120">[out] Un puntero a una máscara de bits de indicadores que se utilizan para indicar el estado actual de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="ccdc4-121">Si un cliente pasa NULL en el parámetro _lpulSearchState_ , **es posible GetSearchCriteria** no devuelve marcadores.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="ccdc4-122">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="ccdc4-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="ccdc4-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="ccdc4-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="ccdc4-124">La búsqueda debe ejecutarse con prioridad alta con respecto a otras búsquedas.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="ccdc4-125">Si no se establece este marcador, la búsqueda se ejecuta con prioridad normal con respecto a otras búsquedas.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="ccdc4-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="ccdc4-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="ccdc4-127">La búsqueda está en el modo con uso intensivo de la CPU de su funcionamiento, intenta localizar los mensajes que coinciden con los criterios.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="ccdc4-128">Si no se establece este indicador, el elemento con uso intensivo de la CPU de la operación de búsqueda es a través de.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="ccdc4-129">Esta marca sólo tiene significado si está activa la búsqueda (es decir, si se establece la marca SEARCH_RUNNING).</span><span class="sxs-lookup"><span data-stu-id="ccdc4-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="ccdc4-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="ccdc4-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="ccdc4-131">La búsqueda está buscando en los contenedores especificados y todas sus contenedores secundarios para que coincidan con las entradas.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="ccdc4-132">Si no se establece este marcador, solo los contenedores que incluyen explícitamente en la última llamada al método [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) se está buscando.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="ccdc4-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="ccdc4-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="ccdc4-134">La búsqueda está activa y se está actualizando la tabla de contenido del contenedor para reflejar los cambios en el almacén de mensajes o la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="ccdc4-135">Si no se establece este marcador, la búsqueda está inactiva y la tabla de contenido es estática.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ccdc4-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ccdc4-136">Return value</span></span>

<span data-ttu-id="ccdc4-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="ccdc4-137">S_OK</span></span> 
  
> <span data-ttu-id="ccdc4-138">Se obtuvo correctamente los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="ccdc4-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ccdc4-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ccdc4-140">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="ccdc4-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ccdc4-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="ccdc4-142">Criterios de búsqueda nunca se han establecido para el contenedor.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ccdc4-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ccdc4-143">Remarks</span></span>

<span data-ttu-id="ccdc4-144">El método **IMAPIContainer::GetSearchCriteria** obtiene los criterios de búsqueda para un contenedor que admite búsquedas, normalmente una carpeta de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="ccdc4-145">Para crear criterios de búsqueda, llamar al método **IMAPIContainer::SetSearchCriteria** de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ccdc4-146">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="ccdc4-146">Notes to implementers</span></span>

<span data-ttu-id="ccdc4-147">Contenedores de libretas de direcciones que necesite admitir **es posible GetSearchCriteria** sólo si se proporcionan las capacidades de búsqueda avanzada asociadas con la propiedad **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ccdc4-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="ccdc4-148">Para obtener más información acerca de cómo implementar la característica de búsqueda avanzada para contenedores de la libreta de direcciones, vea [Implementación de búsqueda avanzada](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="ccdc4-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ccdc4-149">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ccdc4-149">Notes to callers</span></span>

<span data-ttu-id="ccdc4-150">Cuando haya terminado con las estructuras de datos indicadas por los parámetros _lppRestriction_ y _lppContainerList_ , llame a [MAPIFreeBuffer](mapifreebuffer.md) una vez para cada estructura que liberar.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ccdc4-151">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ccdc4-151">MFCMAPI reference</span></span>

<span data-ttu-id="ccdc4-152">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ccdc4-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ccdc4-153">**File**</span></span>|<span data-ttu-id="ccdc4-154">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="ccdc4-154">**Function**</span></span>|<span data-ttu-id="ccdc4-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ccdc4-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ccdc4-156">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ccdc4-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="ccdc4-157">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="ccdc4-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="ccdc4-158">MFCMAPI usa el método **IMAPIContainer::GetSearchCriteria** para obtener los criterios de búsqueda de una carpeta para mostrar.</span><span class="sxs-lookup"><span data-stu-id="ccdc4-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccdc4-159">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ccdc4-159">See also</span></span>



[<span data-ttu-id="ccdc4-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="ccdc4-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="ccdc4-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ccdc4-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="ccdc4-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ccdc4-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ccdc4-163">Propiedad canónica PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="ccdc4-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="ccdc4-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ccdc4-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="ccdc4-165">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ccdc4-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

