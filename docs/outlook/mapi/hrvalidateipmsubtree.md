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
ms.openlocfilehash: 8b6d4fa1d9ffa6ab5f800bad9f02ac5aa9abd8c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817073"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="f49a6-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="f49a6-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="f49a6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f49a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f49a6-105">Agrega las carpetas estándar de mensajes interpersonales (IPM) a un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f49a6-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f49a6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f49a6-106">Header file:</span></span>  <br/> |<span data-ttu-id="f49a6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f49a6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f49a6-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="f49a6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f49a6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f49a6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f49a6-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f49a6-110">Called by:</span></span>  <br/> |<span data-ttu-id="f49a6-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="f49a6-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="f49a6-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f49a6-112">Parameters</span></span>

 <span data-ttu-id="f49a6-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="f49a6-113">_lpMDB_</span></span>
  
> <span data-ttu-id="f49a6-114">[entrada] Puntero al mensaje almacena el objeto que se va a agregar las carpetas.</span><span class="sxs-lookup"><span data-stu-id="f49a6-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="f49a6-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f49a6-115">_ulFlags_</span></span>
  
> <span data-ttu-id="f49a6-116">[entrada] Máscara de bits de indicadores que se utilizan para controlar cómo se crean las carpetas.</span><span class="sxs-lookup"><span data-stu-id="f49a6-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="f49a6-117">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="f49a6-117">The following flags can be set:</span></span>
    
<span data-ttu-id="f49a6-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="f49a6-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="f49a6-119">Las carpetas deben comprobarse antes de la creación, incluso si las propiedades del almacén de mensajes indican que son válidos.</span><span class="sxs-lookup"><span data-stu-id="f49a6-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="f49a6-120">Normalmente, una aplicación cliente establece esta marca cuando un error indica que se ha dañado la estructura de una carpeta existente.</span><span class="sxs-lookup"><span data-stu-id="f49a6-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="f49a6-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="f49a6-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="f49a6-122">El conjunto completo de carpetas IPM debe crearse en la carpeta raíz del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f49a6-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="f49a6-123">Los títulos de la carpeta en la jerarquía son:</span><span class="sxs-lookup"><span data-stu-id="f49a6-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="f49a6-124">Vistas de carpeta</span><span class="sxs-lookup"><span data-stu-id="f49a6-124">Folder Views</span></span>
    
    - <span data-ttu-id="f49a6-125">Vistas comunes</span><span class="sxs-lookup"><span data-stu-id="f49a6-125">Common Views</span></span>
    
    - <span data-ttu-id="f49a6-126">Raíz de la búsqueda\*</span><span class="sxs-lookup"><span data-stu-id="f49a6-126">Search Root\*</span></span>
    
    - <span data-ttu-id="f49a6-127">Subárbol IPM\*</span><span class="sxs-lookup"><span data-stu-id="f49a6-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="f49a6-128">Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="f49a6-128">Inbox</span></span>
    
    - <span data-ttu-id="f49a6-129">Bandeja de salida</span><span class="sxs-lookup"><span data-stu-id="f49a6-129">Outbox</span></span>
    
    - <span data-ttu-id="f49a6-130">Elementos eliminados\*</span><span class="sxs-lookup"><span data-stu-id="f49a6-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="f49a6-131">Elementos enviados</span><span class="sxs-lookup"><span data-stu-id="f49a6-131">Sent Items</span></span>
    
    <span data-ttu-id="f49a6-132">donde las tres carpetas marcan con \* son el conjunto mínimo creado incluso cuando no se ha establecido el indicador MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="f49a6-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="f49a6-133">Normalmente, una aplicación cliente establece esta marca cuando el almacén de mensajes en el que son las carpetas que se creará es el almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f49a6-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="f49a6-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="f49a6-134">_lpcValues_</span></span>
  
> <span data-ttu-id="f49a6-135">[entrada, salida] Puntero al número de estructuras de [SPropValue](spropvalue.md) en la matriz devuelta en el parámetro _lppProps_ .</span><span class="sxs-lookup"><span data-stu-id="f49a6-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="f49a6-136">El valor del parámetro _lpcValues_ puede ser cero si _lppProps_ es NULL.</span><span class="sxs-lookup"><span data-stu-id="f49a6-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="f49a6-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="f49a6-137">_lppProps_</span></span>
  
> <span data-ttu-id="f49a6-138">[entrada, salida] Puntero a un puntero a una matriz de estructuras **SPropValue** que contiene los valores de propiedad para la propiedad **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) y de las propiedades de identificador de entrada de carpeta correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f49a6-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="f49a6-139">Si **HrValidateIPMSubtree** crea una bandeja de entrada en el almacén de mensajes, la matriz **SPropValue** incluye un identificador de entrada de la Bandeja de entrada con una etiqueta de propiedad especial de forma rígida como `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span><span class="sxs-lookup"><span data-stu-id="f49a6-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="f49a6-140">El parámetro _lppProps_ puede ser NULL, que indica que la implementación de la llamada no requiere que se devuelve una matriz de **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="f49a6-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="f49a6-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="f49a6-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="f49a6-142">[out] Puntero a un puntero a una estructura [MAPIERROR](mapierror.md) que contiene información de versión, el componente y el contexto de un error.</span><span class="sxs-lookup"><span data-stu-id="f49a6-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="f49a6-143">El parámetro _lppMAPIError_ se establece en NULL si no hay estructura **MAPIERROR** se devuelve.</span><span class="sxs-lookup"><span data-stu-id="f49a6-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f49a6-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f49a6-144">Return value</span></span>

<span data-ttu-id="f49a6-145">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f49a6-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f49a6-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f49a6-146">Remarks</span></span>

<span data-ttu-id="f49a6-147">MAPI utiliza la función **HrValidateIPMSubtree** internamente para construir el subárbol IPM estándar en un almacén de mensajes cuando se abre el almacén por primera vez o cuando un almacén se realiza almacenar el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f49a6-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="f49a6-148">Esta función también puede utilizarse por las aplicaciones cliente para validar o reparar carpetas de mensajes estándar.</span><span class="sxs-lookup"><span data-stu-id="f49a6-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="f49a6-149">**HrValidateIPMSubtree** siempre crea las carpetas raíz de la búsqueda y subárbol IPM en la carpeta del almacén raíz y la carpeta Elementos eliminados en la carpeta subárbol IPM.</span><span class="sxs-lookup"><span data-stu-id="f49a6-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="f49a6-150">La carpeta subárbol IPM es la raíz de la jerarquía de IPM de ese almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f49a6-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="f49a6-151">La carpeta raíz de la búsqueda se puede usar como la raíz de un subárbol de carpetas de resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f49a6-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="f49a6-152">Los clientes IPM deben mostrar su vista de carpeta empezando en la carpeta raíz del subárbol IPM y mostrar a secundarios las carpetas por debajo de ella.</span><span class="sxs-lookup"><span data-stu-id="f49a6-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="f49a6-153">Información de la carpeta raíz de un almacén de mensajes no debe aparecer en la interfaz de usuario de un cliente.</span><span class="sxs-lookup"><span data-stu-id="f49a6-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="f49a6-154">Esta funcionalidad significa que si un cliente debe ocultar información, la información se puede poner en el directorio de raíz del subárbol IPM, donde no es visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="f49a6-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="f49a6-155">Por el contrario, las aplicaciones que no sean IPM que requieren los mensajes y carpetas para ser invisibles para el usuario, por ejemplo en un almacén de mensajes basado en servidor, pueden ponerlos fuera de la jerarquía IPM.</span><span class="sxs-lookup"><span data-stu-id="f49a6-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="f49a6-156">**HrValidateIPMSubtree** establece la propiedad **PR_VALID_FOLDER_MASK** para indicar si cada carpeta IPM crea tiene un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="f49a6-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="f49a6-157">Las siguientes propiedades de identificador de entrada del almacén de mensajes se establece en los identificadores de entrada de las carpetas correspondientes y devuelven en el parámetro _lppProps_ junto con **PR_VALID_FOLDER_MASK**:</span><span class="sxs-lookup"><span data-stu-id="f49a6-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="f49a6-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f49a6-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f49a6-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f49a6-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f49a6-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f49a6-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f49a6-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f49a6-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f49a6-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f49a6-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f49a6-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f49a6-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f49a6-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f49a6-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f49a6-165">Un marcador de posición [PROP_TAG](prop_tag.md) para la Bandeja de entrada IPM (PT_BINARY, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="f49a6-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="f49a6-166">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f49a6-166">MFCMAPI reference</span></span>

<span data-ttu-id="f49a6-167">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f49a6-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f49a6-168">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="f49a6-168">**File**</span></span>|<span data-ttu-id="f49a6-169">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="f49a6-169">**Function**</span></span>|<span data-ttu-id="f49a6-170">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="f49a6-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f49a6-171">MstStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f49a6-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="f49a6-172">CMsgStoreDlg::OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="f49a6-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="f49a6-173">MFCMAPI utiliza el método **HrValidateIPMSubtree** para agregar carpetas estándar a un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f49a6-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f49a6-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="f49a6-174">See also</span></span>



[<span data-ttu-id="f49a6-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="f49a6-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="f49a6-176">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="f49a6-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

