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
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409212"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="71e0f-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="71e0f-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="71e0f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71e0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71e0f-105">Convierte el identificador de entrada interna de un almacén de mensajes en un identificador de entrada más utilizable por el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="71e0f-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71e0f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="71e0f-106">Header file:</span></span>  <br/> |<span data-ttu-id="71e0f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71e0f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="71e0f-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="71e0f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="71e0f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="71e0f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="71e0f-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="71e0f-110">Called by:</span></span>  <br/> |<span data-ttu-id="71e0f-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="71e0f-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="71e0f-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="71e0f-112">Parameters</span></span>

 <span data-ttu-id="71e0f-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="71e0f-113">_ulFlags_</span></span>
  
> <span data-ttu-id="71e0f-114">[in] Máscara de bits de marcas.</span><span class="sxs-lookup"><span data-stu-id="71e0f-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="71e0f-115">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="71e0f-115">The following flag can be set:</span></span>
    
<span data-ttu-id="71e0f-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="71e0f-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="71e0f-117">Las cadenas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="71e0f-117">The strings are in Unicode format.</span></span> <span data-ttu-id="71e0f-118">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="71e0f-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="71e0f-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="71e0f-119">_szDLLName_</span></span>
  
> <span data-ttu-id="71e0f-120">[in] Nombre de la DLL del proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="71e0f-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="71e0f-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="71e0f-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="71e0f-122">[in] Tamaño, en bytes, del identificador de entrada original del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="71e0f-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="71e0f-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="71e0f-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="71e0f-124">[in] Puntero a una [estructura ENTRYID](entryid.md) que contiene el identificador de entrada original.</span><span class="sxs-lookup"><span data-stu-id="71e0f-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="71e0f-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="71e0f-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="71e0f-126">[salida] Puntero al tamaño, en bytes, del nuevo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="71e0f-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="71e0f-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="71e0f-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="71e0f-128">[salida] Puntero a un puntero a una **estructura ENTRYID** que contiene el nuevo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="71e0f-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="71e0f-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71e0f-129">Return value</span></span>

<span data-ttu-id="71e0f-130">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="71e0f-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="71e0f-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="71e0f-131">Remarks</span></span>

<span data-ttu-id="71e0f-132">Un objeto de almacén de mensajes conserva un identificador de entrada interno que solo es significativo para los proveedores de servicios que se alojó en ese almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="71e0f-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="71e0f-133">Para otros componentes de mensajería, MAPI proporciona una versión ajustada del identificador de entrada interna que la hace reconocible como que pertenece al almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="71e0f-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="71e0f-134">Los proveedores de servicios coresident siempre deben tener el identificador de entrada original del almacén de mensajes sin envolver; Las aplicaciones cliente siempre deben tener la versión ajustada, que luego se puede usar en cualquier lugar del dominio de mensajería y en otros dominios.</span><span class="sxs-lookup"><span data-stu-id="71e0f-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="71e0f-135">Un proveedor de servicios puede ajustar un identificador de entrada del almacén de mensajes mediante la función **WrapStoreEntryID** o el método [IMAPISupport::WrapStoreEntryID,](imapisupport-wrapstoreentryid.md) que llama a la **función WrapStoreEntryID.**</span><span class="sxs-lookup"><span data-stu-id="71e0f-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="71e0f-136">El proveedor debe ajustar el identificador de entrada al exponer la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) del almacén de mensajes o escribirlo en una sección de perfil y al exponer la propiedad **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="71e0f-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="71e0f-137">MAPI ajusta un identificador de entrada del almacén de mensajes al responder a una [llamada IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md)</span><span class="sxs-lookup"><span data-stu-id="71e0f-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="71e0f-138">Cuando una aplicación cliente pasa un identificador de entrada de almacén de mensajes ajustado a MAPI, por ejemplo, en una llamada [IMAPISession::OpenEntry,](imapisession-openentry.md) MAPI desenvuelve el identificador de entrada antes de usarlo para llamar a un método de proveedor como [IMSProvider::Logon](imsprovider-logon.md) o [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span><span class="sxs-lookup"><span data-stu-id="71e0f-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

