---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 25c04f8dee012f4985db98df7d1b3ae5536ef6b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817556"
---
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="e2fee-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="e2fee-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="e2fee-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2fee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2fee-105">Convierte el identificador de entrada interno de un almacén de mensajes en un identificador de entrada con el formato estándar de MAPI.</span><span class="sxs-lookup"><span data-stu-id="e2fee-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="e2fee-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2fee-106">Parameters</span></span>

 <span data-ttu-id="e2fee-107">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="e2fee-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="e2fee-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpOrigEntry_ .</span><span class="sxs-lookup"><span data-stu-id="e2fee-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="e2fee-109">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="e2fee-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="e2fee-110">[entrada] Un puntero al identificador de entrada privada para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e2fee-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="e2fee-111">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="e2fee-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="e2fee-112">[out] Un puntero para el número de bytes en el identificador de entrada indicado por el parámetro _lppWrappedEntry_ .</span><span class="sxs-lookup"><span data-stu-id="e2fee-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="e2fee-113">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="e2fee-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="e2fee-114">[out] Un puntero a un puntero para el identificador de entrada ajustado.</span><span class="sxs-lookup"><span data-stu-id="e2fee-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2fee-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2fee-115">Return value</span></span>

<span data-ttu-id="e2fee-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2fee-116">S_OK</span></span> 
  
> <span data-ttu-id="e2fee-117">El identificador de entrada correctamente ajustado.</span><span class="sxs-lookup"><span data-stu-id="e2fee-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2fee-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2fee-118">Remarks</span></span>

<span data-ttu-id="e2fee-119">El método **IMAPISupport::WrapStoreEntryID** se implementa para todos los objetos de soporte técnico de proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="e2fee-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="e2fee-120">Proveedores de servicios de usar **WrapStoreEntryID** para que MAPI genera un identificador de entrada para un almacén de mensajes que se ajusta el identificador de entrada interno de la tienda.</span><span class="sxs-lookup"><span data-stu-id="e2fee-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e2fee-121">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="e2fee-121">Notes to callers</span></span>

<span data-ttu-id="e2fee-122">Cuando un cliente llama (método) [IMAPIProp::GetProps](imapiprop-getprops.md) de su almacén de mensajes recuperar su propiedad **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) y el almacén de mensajes usa un identificador de entrada en un formato privado, llamada **WrapStoreEntryID **y devolver el identificador de entrada indicado por el parámetro _lppWrappedEntry_ .</span><span class="sxs-lookup"><span data-stu-id="e2fee-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="e2fee-123">Las llamadas a los métodos [IMSProvider::Logon](imsprovider-logon.md) y [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) siempre obtención el identificador de entrada privada de la tienda; se usa la versión ajustada sólo entre las aplicaciones de cliente y MAPI.</span><span class="sxs-lookup"><span data-stu-id="e2fee-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="e2fee-124">Libere la memoria para el identificador de entrada que apunta el parámetro _lppWrappedEntry_ mediante el uso de la función [MAPIFreeBuffer](mapifreebuffer.md) cuando haya terminado con el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="e2fee-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2fee-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2fee-125">See also</span></span>



[<span data-ttu-id="e2fee-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="e2fee-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="e2fee-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="e2fee-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="e2fee-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="e2fee-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="e2fee-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="e2fee-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="e2fee-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e2fee-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e2fee-131">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2fee-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
