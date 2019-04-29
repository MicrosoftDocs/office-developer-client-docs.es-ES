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
ms.openlocfilehash: 7845238722ce81b84210b6f4fc33f9df0abacc07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412026"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="1b99d-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="1b99d-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="1b99d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b99d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b99d-105">Obtiene los criterios de búsqueda del contenedor.</span><span class="sxs-lookup"><span data-stu-id="1b99d-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="1b99d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1b99d-106">Parameters</span></span>

 <span data-ttu-id="1b99d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b99d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1b99d-108">a Una máscara de bits de marcadores que controla el tipo de las cadenas pasadas.</span><span class="sxs-lookup"><span data-stu-id="1b99d-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="1b99d-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="1b99d-109">The following flag can be set:</span></span>
    
<span data-ttu-id="1b99d-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1b99d-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1b99d-111">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1b99d-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="1b99d-112">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1b99d-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="1b99d-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="1b99d-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="1b99d-114">contempla Un puntero a un puntero a una estructura [SRestriction](srestriction.md) que define los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1b99d-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="1b99d-115">Si una aplicación cliente pasa NULL en el parámetro _lppRestriction_ , **GetSearchCriteria** no devuelve una estructura **SRestriction** .</span><span class="sxs-lookup"><span data-stu-id="1b99d-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="1b99d-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="1b99d-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="1b99d-117">contempla Un puntero a un puntero a una matriz de identificadores de entrada que representan los contenedores que se van a incluir en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1b99d-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="1b99d-118">Si un cliente pasa NULL en el parámetro _lppContainerList_ , **GetSearchCriteria** no devuelve una matriz de identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="1b99d-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="1b99d-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="1b99d-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="1b99d-120">contempla Puntero a una máscara de máscara de marcas usada para indicar el estado actual de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1b99d-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="1b99d-121">Si un cliente pasa NULL en el parámetro _lpulSearchState_ , **GetSearchCriteria** no devuelve ningún marcador.</span><span class="sxs-lookup"><span data-stu-id="1b99d-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="1b99d-122">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="1b99d-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="1b99d-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="1b99d-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="1b99d-124">La búsqueda debe ejecutarse con prioridad alta en relación con otras búsquedas.</span><span class="sxs-lookup"><span data-stu-id="1b99d-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="1b99d-125">Si no se establece esta marca, la búsqueda se ejecuta con prioridad normal en relación con otras búsquedas.</span><span class="sxs-lookup"><span data-stu-id="1b99d-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="1b99d-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="1b99d-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="1b99d-127">La búsqueda está en el modo de uso intensivo de la CPU de su funcionamiento, lo que intenta encontrar los mensajes que coinciden con los criterios.</span><span class="sxs-lookup"><span data-stu-id="1b99d-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="1b99d-128">Si no se establece esta marca, la parte que consume mucha CPU de la operación de búsqueda ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="1b99d-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="1b99d-129">Este indicador solo tiene significado si la búsqueda está activa (es decir, si se ha establecido la marca SEARCH_RUNNING).</span><span class="sxs-lookup"><span data-stu-id="1b99d-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="1b99d-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="1b99d-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="1b99d-131">La búsqueda está buscando en los contenedores especificados y en todos sus contenedores secundarios para las entradas coincidentes.</span><span class="sxs-lookup"><span data-stu-id="1b99d-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="1b99d-132">Si no se establece esta marca, solo se busca en los contenedores incluidos explícitamente en la última llamada al método [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="1b99d-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="1b99d-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="1b99d-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="1b99d-134">La búsqueda está activa y la tabla de contenido del contenedor se está actualizando para reflejar los cambios en el almacén de mensajes o la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="1b99d-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="1b99d-135">Si no se establece esta marca, la búsqueda está inactiva y la tabla de contenido es estática.</span><span class="sxs-lookup"><span data-stu-id="1b99d-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b99d-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b99d-136">Return value</span></span>

<span data-ttu-id="1b99d-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b99d-137">S_OK</span></span> 
  
> <span data-ttu-id="1b99d-138">Los criterios de búsqueda se obtuvieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="1b99d-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="1b99d-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="1b99d-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="1b99d-140">Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="1b99d-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="1b99d-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="1b99d-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="1b99d-142">Los criterios de búsqueda nunca se establecieron para el contenedor.</span><span class="sxs-lookup"><span data-stu-id="1b99d-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b99d-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b99d-143">Remarks</span></span>

<span data-ttu-id="1b99d-144">El método **IMAPIContainer:: GetSearchCriteria** obtiene los criterios de búsqueda de un contenedor que admite búsquedas, normalmente una carpeta de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1b99d-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="1b99d-145">Los criterios de búsqueda se crean llamando al método **IMAPIContainer:: SetSearchCriteria** del contenedor.</span><span class="sxs-lookup"><span data-stu-id="1b99d-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1b99d-146">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="1b99d-146">Notes to implementers</span></span>

<span data-ttu-id="1b99d-147">Es posible que los contenedores de la libreta de direcciones solo deban admitir **GetSearchCriteria** si proporcionan las capacidades de búsqueda avanzada asociadas con la propiedad **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1b99d-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="1b99d-148">Para obtener más información acerca de cómo implementar la característica de búsqueda avanzada para los contenedores de la libreta de direcciones, consulte [implementación de búsqueda avanzada](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="1b99d-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1b99d-149">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="1b99d-149">Notes to callers</span></span>

<span data-ttu-id="1b99d-150">Cuando termine con las estructuras de datos a las que apuntan los parámetros _lppRestriction_ y _lppContainerList_ , llame a [MAPIFreeBuffer](mapifreebuffer.md) una vez para cada estructura que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="1b99d-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1b99d-151">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1b99d-151">MFCMAPI reference</span></span>

<span data-ttu-id="1b99d-152">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1b99d-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1b99d-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="1b99d-153">**File**</span></span>|<span data-ttu-id="1b99d-154">**Función**</span><span class="sxs-lookup"><span data-stu-id="1b99d-154">**Function**</span></span>|<span data-ttu-id="1b99d-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1b99d-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1b99d-156">HierarchyTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="1b99d-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="1b99d-157">CHierarchyTableDlg:: OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="1b99d-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="1b99d-158">MFCMAPI usa el método **IMAPIContainer:: GetSearchCriteria** para obtener los criterios de búsqueda de la carpeta que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="1b99d-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b99d-159">Ver también</span><span class="sxs-lookup"><span data-stu-id="1b99d-159">See also</span></span>



[<span data-ttu-id="1b99d-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="1b99d-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="1b99d-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="1b99d-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="1b99d-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1b99d-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1b99d-163">Propiedad canónica PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="1b99d-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="1b99d-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1b99d-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="1b99d-165">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="1b99d-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

