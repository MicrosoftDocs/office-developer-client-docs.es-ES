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
ms.openlocfilehash: a623ef24f76dae93bfc13e6613e885a120f3278e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341289"
---
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="00e78-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="00e78-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="00e78-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00e78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00e78-105">Convierte el identificador de entrada interno de un almacén de mensajes en un identificador de entrada en el formato MAPI estándar.</span><span class="sxs-lookup"><span data-stu-id="00e78-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="00e78-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="00e78-106">Parameters</span></span>

 <span data-ttu-id="00e78-107">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="00e78-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="00e78-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpOrigEntry_ .</span><span class="sxs-lookup"><span data-stu-id="00e78-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="00e78-109">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="00e78-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="00e78-110">a Un puntero al identificador de entrada privada para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="00e78-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="00e78-111">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="00e78-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="00e78-112">contempla Un puntero al recuento de bytes en el identificador de entrada al que apunta el parámetro _lppWrappedEntry_ .</span><span class="sxs-lookup"><span data-stu-id="00e78-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="00e78-113">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="00e78-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="00e78-114">contempla Un puntero a un puntero al identificador de entrada ajustado.</span><span class="sxs-lookup"><span data-stu-id="00e78-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="00e78-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00e78-115">Return value</span></span>

<span data-ttu-id="00e78-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="00e78-116">S_OK</span></span> 
  
> <span data-ttu-id="00e78-117">El identificador de entrada se ha ajustado correctamente.</span><span class="sxs-lookup"><span data-stu-id="00e78-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="00e78-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00e78-118">Remarks</span></span>

<span data-ttu-id="00e78-119">El método **IMAPISupport:: WrapStoreEntryID** se implementa para todos los objetos de compatibilidad del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="00e78-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="00e78-120">Los proveedores de servicios usan **WrapStoreEntryID** para que MAPI genere un identificador de entrada para un almacén de mensajes que ajuste el identificador de entrada interno de la tienda.</span><span class="sxs-lookup"><span data-stu-id="00e78-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="00e78-121">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="00e78-121">Notes to callers</span></span>

<span data-ttu-id="00e78-122">Cuando un cliente llama al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar su propiedad **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) y el almacén de mensajes utiliza un identificador de entrada en un formato privado, llame a \*\*WrapStoreEntryID \*\*y devolver el identificador de entrada al que apunta el parámetro _lppWrappedEntry_ .</span><span class="sxs-lookup"><span data-stu-id="00e78-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="00e78-123">Las llamadas a los métodos [IMSProvider:: Logon](imsprovider-logon.md) y [IMSLogon:: CompareEntryIDs](imslogon-compareentryids.md) siempre obtienen el identificador de entrada privada del almacén; la versión empaquetada solo se usa entre aplicaciones cliente y MAPI.</span><span class="sxs-lookup"><span data-stu-id="00e78-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="00e78-124">Libere la memoria del identificador de entrada al que apunta el parámetro _lppWrappedEntry_ mediante la función [MAPIFreeBuffer](mapifreebuffer.md) cuando termine de usar el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="00e78-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00e78-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="00e78-125">See also</span></span>



[<span data-ttu-id="00e78-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="00e78-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="00e78-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="00e78-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="00e78-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="00e78-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="00e78-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="00e78-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="00e78-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="00e78-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="00e78-131">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="00e78-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

