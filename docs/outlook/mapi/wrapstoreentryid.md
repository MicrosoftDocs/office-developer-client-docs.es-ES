---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 45263396e69852a9ae17ff6fce284663bdf2fb07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585139"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="4ac41-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="4ac41-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="4ac41-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ac41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ac41-105">Convierte el identificador de entrada interno de un almacén de mensajes en un identificador de entrada más utilizable por el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4ac41-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ac41-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4ac41-106">Header file:</span></span>  <br/> |<span data-ttu-id="4ac41-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ac41-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4ac41-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="4ac41-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4ac41-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4ac41-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4ac41-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4ac41-110">Called by:</span></span>  <br/> |<span data-ttu-id="4ac41-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="4ac41-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
WrapStoreEntryID(
  ULONG ulFlags,
  LPSTR szDLLName,
  ULONG cbOrigEntry,
  LPENTRYID lpOrigEntry,
  ULONG * lpcbWrappedEntry,
  LPENTRYID * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="4ac41-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="4ac41-112">Parameters</span></span>

 <span data-ttu-id="4ac41-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4ac41-113">_ulFlags_</span></span>
  
> <span data-ttu-id="4ac41-114">[entrada] Máscara de bits de indicadores.</span><span class="sxs-lookup"><span data-stu-id="4ac41-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="4ac41-115">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="4ac41-115">The following flag can be set:</span></span>
    
<span data-ttu-id="4ac41-116">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4ac41-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4ac41-117">Las cadenas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="4ac41-117">The strings are in Unicode format.</span></span> <span data-ttu-id="4ac41-118">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="4ac41-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="4ac41-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="4ac41-119">_szDLLName_</span></span>
  
> <span data-ttu-id="4ac41-120">[entrada] El nombre del proveedor de almacén de DLL de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4ac41-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="4ac41-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="4ac41-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="4ac41-122">[entrada] Tamaño, en bytes, del identificador de entrada original para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4ac41-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="4ac41-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="4ac41-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="4ac41-124">[entrada] Puntero a una estructura [ENTRYID](entryid.md) que contiene el identificador de entrada original.</span><span class="sxs-lookup"><span data-stu-id="4ac41-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="4ac41-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="4ac41-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="4ac41-126">[out] Puntero al tamaño, en bytes, del nuevo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="4ac41-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="4ac41-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="4ac41-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="4ac41-128">[out] Puntero a un puntero a una estructura **ENTRYID** que contiene el nuevo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="4ac41-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4ac41-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ac41-129">Return value</span></span>

<span data-ttu-id="4ac41-130">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4ac41-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ac41-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ac41-131">Remarks</span></span>

<span data-ttu-id="4ac41-132">Un objeto de almacén de mensajes mantiene un identificador interno de entrada que es significativo sólo a coresident de proveedores de servicio con ese almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4ac41-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="4ac41-133">Para otros componentes de mensajería MAPI proporciona una versión ajustada del identificador de entrada interna que hace que sea reconocible como que pertenecen al almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4ac41-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="4ac41-134">Proveedores de servicios de coresident siempre se deben proporcionar el identificador de entrada de almacén de mensajes no ajustado original; siempre se deben proporcionar a las aplicaciones cliente de la versión ajustada, que es, a continuación, puede utilizar en cualquier lugar en el dominio de mensajería y en otros dominios.</span><span class="sxs-lookup"><span data-stu-id="4ac41-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="4ac41-135">Puede ajustar un identificador de entrada del almacén de mensaje mediante la función **WrapStoreEntryID** o el método [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) , que llama a la función **WrapStoreEntryID** en un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="4ac41-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="4ac41-136">El proveedor debe ajustar el identificador de entrada al exponer de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) del almacén de mensajes (propiedad) o escribir en una sección de perfil y cuando se exponen **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) propiedad.</span><span class="sxs-lookup"><span data-stu-id="4ac41-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="4ac41-137">MAPI ajusta a un identificador de entrada del almacén de mensaje al responder a una llamada de [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="4ac41-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="4ac41-138">Cuando una aplicación cliente pasa un identificador de entrada del almacén de mensaje ajustadas a MAPI, por ejemplo en una llamada [IMAPISession::OpenEntry](imapisession-openentry.md) , MAPI desajusta el identificador de entrada antes de usar para llamar a un método de proveedor, como [IMSProvider::Logon](imsprovider-logon.md) o [ IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span><span class="sxs-lookup"><span data-stu-id="4ac41-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

