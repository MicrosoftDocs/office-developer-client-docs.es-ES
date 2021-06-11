---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436576"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="13674-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="13674-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="13674-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13674-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13674-105">Agrega carpetas de mensajes interpersonales estándar (IPM) a un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="13674-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13674-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="13674-106">Header file:</span></span>  <br/> |<span data-ttu-id="13674-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="13674-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="13674-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="13674-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="13674-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="13674-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="13674-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="13674-110">Called by:</span></span>  <br/> |<span data-ttu-id="13674-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="13674-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="13674-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="13674-112">Parameters</span></span>

 <span data-ttu-id="13674-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="13674-113">_lpMDB_</span></span>
  
> <span data-ttu-id="13674-114">[in] Puntero al objeto de almacén de mensajes al que se agregarán las carpetas.</span><span class="sxs-lookup"><span data-stu-id="13674-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="13674-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="13674-115">_ulFlags_</span></span>
  
> <span data-ttu-id="13674-116">[in] Máscara de bits de marcas usadas para controlar cómo se crean las carpetas.</span><span class="sxs-lookup"><span data-stu-id="13674-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="13674-117">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="13674-117">The following flags can be set:</span></span>
    
<span data-ttu-id="13674-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="13674-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="13674-119">Las carpetas deben comprobarse antes de la creación, incluso si las propiedades del almacén de mensajes indican que son válidas.</span><span class="sxs-lookup"><span data-stu-id="13674-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="13674-120">Normalmente, una aplicación cliente establece esta marca cuando un error indica que se ha dañado la estructura de una carpeta existente.</span><span class="sxs-lookup"><span data-stu-id="13674-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="13674-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="13674-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="13674-122">El conjunto completo de carpetas IPM debe crearse en la carpeta raíz del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="13674-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="13674-123">Los títulos de carpeta de la jerarquía son:</span><span class="sxs-lookup"><span data-stu-id="13674-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="13674-124">Vistas de carpeta</span><span class="sxs-lookup"><span data-stu-id="13674-124">Folder Views</span></span>
    
    - <span data-ttu-id="13674-125">Vistas comunes</span><span class="sxs-lookup"><span data-stu-id="13674-125">Common Views</span></span>
    
    - <span data-ttu-id="13674-126">Raíz de búsqueda\*</span><span class="sxs-lookup"><span data-stu-id="13674-126">Search Root\*</span></span>
    
    - <span data-ttu-id="13674-127">Subárbol IPM\*</span><span class="sxs-lookup"><span data-stu-id="13674-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="13674-128">Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="13674-128">Inbox</span></span>
    
    - <span data-ttu-id="13674-129">Bandeja de salida</span><span class="sxs-lookup"><span data-stu-id="13674-129">Outbox</span></span>
    
    - <span data-ttu-id="13674-130">Elementos eliminados\*</span><span class="sxs-lookup"><span data-stu-id="13674-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="13674-131">Elementos enviados</span><span class="sxs-lookup"><span data-stu-id="13674-131">Sent Items</span></span>
    
    <span data-ttu-id="13674-132">donde las tres carpetas marcadas con son el conjunto mínimo creado incluso \* MAPI_FULL_IPM_TREE no se ha establecido la marca.</span><span class="sxs-lookup"><span data-stu-id="13674-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="13674-133">Normalmente, una aplicación cliente establece esta marca cuando el almacén de mensajes en el que se van a crear las carpetas es el almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="13674-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="13674-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="13674-134">_lpcValues_</span></span>
  
> <span data-ttu-id="13674-135">[in, out] Puntero al número de [estructuras SPropValue](spropvalue.md) de la matriz devuelta en el _parámetro lppProps._</span><span class="sxs-lookup"><span data-stu-id="13674-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="13674-136">El valor del parámetro  _lpcValues_ puede ser cero si  _lppProps_ es NULL.</span><span class="sxs-lookup"><span data-stu-id="13674-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="13674-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="13674-137">_lppProps_</span></span>
  
> <span data-ttu-id="13674-138">[in, out] Puntero a un puntero a una matriz de estructuras **SPropValue** que contiene valores de propiedad para la propiedad **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) y para las propiedades de identificador de entrada de carpeta apropiadas.</span><span class="sxs-lookup"><span data-stu-id="13674-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="13674-139">Si **HrValidateIPMSubtree** crea una Bandeja de entrada en el almacén de mensajes, la matriz **SPropValue** incluye un identificador de entrada de la Bandeja de entrada con una etiqueta de propiedad especial codificada como  `PROP_TAG(PT_BINARY, PROP_ID_NULL)` .</span><span class="sxs-lookup"><span data-stu-id="13674-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="13674-140">El _parámetro lppProps_ puede ser NULL, lo que indica que la implementación de llamada no requiere que se devuelva una matriz **SPropValue.**</span><span class="sxs-lookup"><span data-stu-id="13674-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="13674-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="13674-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="13674-142">[salida] Puntero a un puntero a una [estructura MAPIERROR](mapierror.md) que contiene información de versión, componente y contexto de un error.</span><span class="sxs-lookup"><span data-stu-id="13674-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="13674-143">El _parámetro lppMAPIError_ se establece en NULL si no se devuelve ninguna **estructura MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="13674-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="13674-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13674-144">Return value</span></span>

<span data-ttu-id="13674-145">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="13674-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13674-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13674-146">Remarks</span></span>

<span data-ttu-id="13674-147">MAPI usa la función **HrValidateIPMSubtree** internamente para construir el subárbol IPM estándar en un almacén de mensajes cuando se abre por primera vez el almacén o cuando se crea un almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="13674-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="13674-148">Las aplicaciones cliente también pueden usar esta función para validar o reparar carpetas de mensajes estándar.</span><span class="sxs-lookup"><span data-stu-id="13674-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="13674-149">**HrValidateIPMSubtree** siempre crea las carpetas Raíz de búsqueda e Subárbol IPM en la carpeta raíz del almacén y la carpeta Elementos eliminados en la carpeta Subárbol IPM.</span><span class="sxs-lookup"><span data-stu-id="13674-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="13674-150">La carpeta Subárbol IPM es la raíz de la jerarquía IPM en ese almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="13674-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="13674-151">La carpeta Raíz de búsqueda se puede usar como raíz de un subárbol para carpetas de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="13674-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="13674-152">Los clientes IPM deben mostrar su vista de carpeta a partir de la carpeta raíz del subárbol IPM y mostrar las carpetas secundarias debajo de ella.</span><span class="sxs-lookup"><span data-stu-id="13674-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="13674-153">La información de la carpeta raíz de un almacén de mensajes no debe aparecer en la interfaz de usuario de un cliente.</span><span class="sxs-lookup"><span data-stu-id="13674-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="13674-154">Esta funcionalidad significa que si un cliente debe ocultar información, la información se puede colocar en el directorio raíz del subárbol IPM, donde no es visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="13674-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="13674-155">En cambio, las aplicaciones que no son IPM que requieren que los mensajes y carpetas sean invisibles para el usuario, por ejemplo, en un almacén de mensajes basado en servidor, pueden colocarlos fuera de la jerarquía IPM.</span><span class="sxs-lookup"><span data-stu-id="13674-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="13674-156">**HrValidateIPMSubtree** establece la **propiedad PR_VALID_FOLDER_MASK** para indicar si cada carpeta IPM que crea tiene un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="13674-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="13674-157">Las siguientes propiedades de identificador de entrada del almacén de mensajes se establecen en los identificadores de entrada de las carpetas correspondientes y se devuelven en el parámetro  _lppProps_ junto con **PR_VALID_FOLDER_MASK**:</span><span class="sxs-lookup"><span data-stu-id="13674-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="13674-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13674-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="13674-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13674-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="13674-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13674-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="13674-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13674-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="13674-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13674-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="13674-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13674-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="13674-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13674-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="13674-165">Marcador de [posición PROP_TAG](prop_tag.md) para la Bandeja de entrada IPM (PT_BINARY, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="13674-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="13674-166">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="13674-166">MFCMAPI reference</span></span>

<span data-ttu-id="13674-167">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="13674-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="13674-168">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="13674-168">**File**</span></span>|<span data-ttu-id="13674-169">**Función**</span><span class="sxs-lookup"><span data-stu-id="13674-169">**Function**</span></span>|<span data-ttu-id="13674-170">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="13674-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="13674-171">MstStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="13674-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="13674-172">CMsgStoreDlg::OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="13674-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="13674-173">MFCMAPI usa el **método HrValidateIPMSubtree** para agregar carpetas estándar a un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="13674-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13674-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="13674-174">See also</span></span>



[<span data-ttu-id="13674-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="13674-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="13674-176">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="13674-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

