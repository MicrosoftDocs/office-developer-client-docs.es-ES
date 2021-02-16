---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9571d51e01c2d58d9b8a9a913ba2c210ae0bd44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411998"
---
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="99a11-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="99a11-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="99a11-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99a11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99a11-105">Crea un identificador de entrada para una dirección de uso único.</span><span class="sxs-lookup"><span data-stu-id="99a11-105">Creates an entry identifier for a one-off address.</span></span>
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="99a11-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99a11-106">Parameters</span></span>

 <span data-ttu-id="99a11-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="99a11-107">_lpszName_</span></span>
  
> <span data-ttu-id="99a11-108">[entrada] Puntero al nombre para mostrar del destinatario de la **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="99a11-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="99a11-109">El  _parámetro lpszName_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="99a11-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="99a11-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="99a11-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="99a11-111">[entrada] Puntero al tipo de dirección (como FAX, SMTP o X500) del destinatario.</span><span class="sxs-lookup"><span data-stu-id="99a11-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="99a11-112">El  _parámetro lpszAdrType_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="99a11-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="99a11-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="99a11-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="99a11-114">[entrada] Puntero a la dirección de mensajería del destinatario.</span><span class="sxs-lookup"><span data-stu-id="99a11-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="99a11-115">El  _parámetro lpszAddress_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="99a11-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="99a11-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99a11-116">_ulFlags_</span></span>
  
> <span data-ttu-id="99a11-117">[entrada] Máscara de bits de marcas que afecta al destinatario de uso único.</span><span class="sxs-lookup"><span data-stu-id="99a11-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="99a11-118">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="99a11-118">The following flags can be set:</span></span>
    
<span data-ttu-id="99a11-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="99a11-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="99a11-120">El destinatario no puede controlar el contenido del mensaje con formato.</span><span class="sxs-lookup"><span data-stu-id="99a11-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="99a11-121">Si MAPI_SEND_NO_RICH_INFO se establece, MAPI establece la propiedad PR_SEND_RICH_INFO **del** destinatario ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) en FALSE.</span><span class="sxs-lookup"><span data-stu-id="99a11-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="99a11-122">Si MAPI_SEND_NO_RICH_INFO no se establece, MAPI establece esta propiedad en TRUE a menos que la dirección de mensajería del destinatario a la que apunta  _lpszAddress_ se interprete como una dirección de Internet.</span><span class="sxs-lookup"><span data-stu-id="99a11-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="99a11-123">En este caso, MAPI establece **PR_SEND_RICH_INFO** en FALSE.</span><span class="sxs-lookup"><span data-stu-id="99a11-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="99a11-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="99a11-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="99a11-125">El nombre para mostrar, el tipo de dirección y la dirección están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="99a11-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="99a11-126">Si no MAPI_UNICODE marca, estas cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="99a11-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="99a11-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="99a11-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="99a11-128">[salida] Puntero al recuento de bytes en el identificador de entrada al que apunta el _parámetro lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="99a11-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="99a11-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="99a11-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="99a11-130">[salida] Puntero a un puntero al identificador de entrada del destinatario de uso único.</span><span class="sxs-lookup"><span data-stu-id="99a11-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="99a11-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99a11-131">Return value</span></span>

<span data-ttu-id="99a11-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="99a11-132">S_OK</span></span> 
  
> <span data-ttu-id="99a11-133">El identificador de entrada único se creó correctamente.</span><span class="sxs-lookup"><span data-stu-id="99a11-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99a11-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99a11-134">Remarks</span></span>

<span data-ttu-id="99a11-135">El **método IMAPISupport::CreateOneOff** se implementa para todos los objetos de compatibilidad del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="99a11-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="99a11-136">Los proveedores de servicios llaman a **CreateOneOff** para crear un identificador de entrada para un destinatario de uso único (un destinatario que no pertenece a ninguno de los contenedores de ninguno de los proveedores de libretas de direcciones cargados actualmente).</span><span class="sxs-lookup"><span data-stu-id="99a11-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="99a11-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="99a11-137">Notes to callers</span></span>

<span data-ttu-id="99a11-138">Cuando haya terminado de usar el identificador de entrada devuelto por **CreateOneOff**, liberar la memoria asignada para el identificador de entrada mediante la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="99a11-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="99a11-139">Notas para proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="99a11-139">Notes to Transport Providers</span></span>

<span data-ttu-id="99a11-140">Admite el formato de encapsulamiento neutro para el transporte (TNEF) y usa el valor de la propiedad PR_SEND_RICH_INFO para determinar si se va **a** usar TNEF al transportar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a11-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="99a11-141">No admitir TNEF o no enviar un mensaje en este formato cuando se solicita puede ser un problema para clientes basados en formularios o clientes que requieren propiedades MAPI personalizadas.</span><span class="sxs-lookup"><span data-stu-id="99a11-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="99a11-142">Esto se debe a que TNEF se usa normalmente para enviar propiedades personalizadas para clases de mensajes personalizadas.</span><span class="sxs-lookup"><span data-stu-id="99a11-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99a11-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="99a11-143">See also</span></span>



[<span data-ttu-id="99a11-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="99a11-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="99a11-145">Propiedad canónica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="99a11-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="99a11-146">Propiedad canónica PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="99a11-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="99a11-147">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="99a11-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

