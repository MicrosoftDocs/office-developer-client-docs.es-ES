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
ms.openlocfilehash: 1cfd4afbda5892e96a1d74ca56f4a6d1f98e2268
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817474"
---
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="ef5bf-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="ef5bf-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="ef5bf-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef5bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef5bf-105">Crea un identificador de entrada para una dirección de uso único.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ef5bf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef5bf-106">Parameters</span></span>

 <span data-ttu-id="ef5bf-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="ef5bf-107">_lpszName_</span></span>
  
> <span data-ttu-id="ef5bf-108">[entrada] Un puntero para el nombre para mostrar del destinatario de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ef5bf-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="ef5bf-109">El parámetro _lpszName_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="ef5bf-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="ef5bf-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="ef5bf-111">[entrada] Un puntero para el tipo de dirección (por ejemplo, FAX, SMTP o X500) del destinatario.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="ef5bf-112">El parámetro _lpszAdrType_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="ef5bf-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="ef5bf-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="ef5bf-114">[entrada] Un puntero a la dirección de mensajería del destinatario.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="ef5bf-115">El parámetro _lpszAddress_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="ef5bf-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ef5bf-116">_ulFlags_</span></span>
  
> <span data-ttu-id="ef5bf-117">[entrada] Una máscara de bits de indicadores que influye en el destinatario de uso único.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="ef5bf-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="ef5bf-118">The following flags can be set:</span></span>
    
<span data-ttu-id="ef5bf-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="ef5bf-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="ef5bf-120">El destinatario no puede controlar el contenido del mensaje con formato.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="ef5bf-121">Si se establece MAPI_SEND_NO_RICH_INFO, MAPI establece la propiedad del destinatario **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) en FALSE.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="ef5bf-122">Si MAPI_SEND_NO_RICH_INFO no está establecido, MAPI establece esta propiedad en TRUE, a menos que se interpreta la dirección del destinatario mensajería indicada por _lpszAddress_ para que sea una dirección de Internet.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="ef5bf-123">En este caso, MAPI establece **PR_SEND_RICH_INFO** en FALSE.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="ef5bf-124">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ef5bf-125">El nombre para mostrar, el tipo de dirección y la dirección están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="ef5bf-126">Si no está establecido el indicador MAPI_UNICODE., estas cadenas se encuentran en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ef5bf-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ef5bf-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="ef5bf-128">[out] Un puntero para el número de bytes en el identificador de entrada indicada por el parámetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="ef5bf-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ef5bf-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="ef5bf-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="ef5bf-130">[out] Un puntero a un puntero al identificador de entrada para el destinatario de uso único.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ef5bf-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef5bf-131">Return value</span></span>

<span data-ttu-id="ef5bf-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef5bf-132">S_OK</span></span> 
  
> <span data-ttu-id="ef5bf-133">Se ha creado correctamente el identificador de entrada único.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef5bf-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ef5bf-134">Remarks</span></span>

<span data-ttu-id="ef5bf-135">El método **IMAPISupport::CreateOneOff** se implementa para todos los objetos de soporte técnico de proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="ef5bf-136">Proveedores de servicios de llamar a **CreateOneOff** para crear un identificador de entrada para un destinatario de uso único (un destinatario que no pertenezcan a cualquiera de los contenedores desde cualquiera de los proveedores de la libreta de direcciones cargada actualmente).</span><span class="sxs-lookup"><span data-stu-id="ef5bf-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ef5bf-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ef5bf-137">Notes to callers</span></span>

<span data-ttu-id="ef5bf-138">Cuando haya terminado con el identificador de entrada devuelto por **CreateOneOff**, libere la memoria asignada para el identificador de entrada mediante el uso de la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ef5bf-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="ef5bf-139">Notas para los proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="ef5bf-139">Notes to Transport Providers</span></span>

<span data-ttu-id="ef5bf-140">Admitir el formato de encapsulación neutro de transporte (TNEF) y usar el valor de la propiedad **PR_SEND_RICH_INFO** para determinar si debe usar TNEF al transportar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="ef5bf-141">No se admite la codificación TNEF o no enviar un mensaje con este formato cuando lo solicita puede ser un problema para los clientes basada en formularios o los clientes que requieren las propiedades personalizadas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="ef5bf-142">Esto es debido a que TNEF normalmente se usa para enviar las propiedades personalizadas para las clases de mensaje personalizadas.</span><span class="sxs-lookup"><span data-stu-id="ef5bf-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ef5bf-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef5bf-143">See also</span></span>



[<span data-ttu-id="ef5bf-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ef5bf-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ef5bf-145">Propiedad canónica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="ef5bf-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="ef5bf-146">Propiedad canónica PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="ef5bf-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="ef5bf-147">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef5bf-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

