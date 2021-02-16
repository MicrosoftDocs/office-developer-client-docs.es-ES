---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 980ac82c6f7fcb5771a6013b3fb033b0bdfd05e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427384"
---
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="1ca48-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="1ca48-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="1ca48-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ca48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ca48-105">Crea un identificador de entrada para una dirección de uso único.</span><span class="sxs-lookup"><span data-stu-id="1ca48-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1ca48-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ca48-106">Parameters</span></span>

 <span data-ttu-id="1ca48-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="1ca48-107">_lpszName_</span></span>
  
> <span data-ttu-id="1ca48-108">[entrada] Puntero al valor de la propiedad PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) del destinatario.</span><span class="sxs-lookup"><span data-stu-id="1ca48-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="1ca48-109">El  _parámetro lpszName_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="1ca48-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="1ca48-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="1ca48-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="1ca48-111">[entrada] Puntero al tipo de dirección del destinatario, como FAX o SMTP.</span><span class="sxs-lookup"><span data-stu-id="1ca48-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="1ca48-112">El  _parámetro lpszAdrType_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="1ca48-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="1ca48-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="1ca48-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="1ca48-114">[entrada] Puntero a la dirección del destinatario.</span><span class="sxs-lookup"><span data-stu-id="1ca48-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="1ca48-115">El  _parámetro lpszAddress_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="1ca48-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="1ca48-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1ca48-116">_ulFlags_</span></span>
  
> <span data-ttu-id="1ca48-117">[entrada] Máscara de bits de marcas que afecta al destinatario de uso único.</span><span class="sxs-lookup"><span data-stu-id="1ca48-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="1ca48-118">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="1ca48-118">The following flags can be set:</span></span>
    
<span data-ttu-id="1ca48-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="1ca48-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="1ca48-120">El destinatario no puede controlar el contenido del mensaje con formato.</span><span class="sxs-lookup"><span data-stu-id="1ca48-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="1ca48-121">Si MAPI_SEND_NO_RICH_INFO se establece, MAPI establece la propiedad PR_SEND_RICH_INFO **del** destinatario ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) en FALSE.</span><span class="sxs-lookup"><span data-stu-id="1ca48-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="1ca48-122">Si MAPI_SEND_NO_RICH_INFO no se establece, MAPI establece esta propiedad en TRUE a menos que la dirección de mensajería del destinatario a la que apunta  _lpszAddress_ se interprete como una dirección de Internet.</span><span class="sxs-lookup"><span data-stu-id="1ca48-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="1ca48-123">En este caso, MAPI establece **PR_SEND_RICH_INFO** en FALSE.</span><span class="sxs-lookup"><span data-stu-id="1ca48-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="1ca48-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1ca48-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1ca48-125">El nombre para mostrar, el tipo de dirección y la dirección están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1ca48-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="1ca48-126">Si no MAPI_UNICODE marca, estas cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1ca48-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="1ca48-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1ca48-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="1ca48-128">[salida] Puntero al recuento de bytes en el identificador de entrada al que apunta el _parámetro lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="1ca48-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1ca48-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="1ca48-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="1ca48-130">[salida] Puntero a un puntero al identificador de entrada del destinatario de uso único.</span><span class="sxs-lookup"><span data-stu-id="1ca48-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1ca48-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ca48-131">Return value</span></span>

<span data-ttu-id="1ca48-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ca48-132">S_OK</span></span> 
  
> <span data-ttu-id="1ca48-133">El identificador de entrada único se creó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1ca48-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ca48-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ca48-134">Remarks</span></span>

<span data-ttu-id="1ca48-135">Los clientes llaman al **método CreateOneOff** para crear un identificador de entrada para un destinatario de uso único, un destinatario que no pertenece a ninguno de los contenedores de ninguno de los proveedores de libretas de direcciones cargados actualmente.</span><span class="sxs-lookup"><span data-stu-id="1ca48-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="1ca48-136">Los destinatarios de uso único pueden tener cualquier tipo de dirección compatible con uno de los proveedores de libretas de direcciones activas para la sesión.</span><span class="sxs-lookup"><span data-stu-id="1ca48-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="1ca48-137">Los destinatarios de uso único suelen crearse con una plantilla para su tipo de dirección particular.</span><span class="sxs-lookup"><span data-stu-id="1ca48-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="1ca48-138">El proveedor de libreta de direcciones que admite el tipo de dirección proporciona la plantilla.</span><span class="sxs-lookup"><span data-stu-id="1ca48-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="1ca48-139">Un usuario de una aplicación cliente escribe la información relevante en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="1ca48-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="1ca48-140">MAPI admite cadenas de caracteres Unicode para el nombre para mostrar, el tipo de dirección y los parámetros de dirección **de CreateOneOff**.</span><span class="sxs-lookup"><span data-stu-id="1ca48-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="1ca48-141">La MAPI_SEND_NO_RICH_INFO marca controla si el texto con formato en formato de texto enriquecido (RTF) se envía junto con cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="1ca48-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="1ca48-142">La mayoría de los proveedores de transporte envían el formato de encapsulamiento neutro de transporte (TNEF), un formato que se usa para transmitir texto con formato, independientemente de cómo el destinatario establece su **propiedad PR_SEND_RICH_INFO** transporte.</span><span class="sxs-lookup"><span data-stu-id="1ca48-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="1ca48-143">Esto no es un problema para los clientes de mensajería que trabajan con mensajes interpersonales.</span><span class="sxs-lookup"><span data-stu-id="1ca48-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="1ca48-144">Sin embargo, dado que TNEF se usa normalmente para enviar propiedades personalizadas para clases de mensajes personalizadas, no admitirlo puede ser un problema para clientes basados en formularios o clientes que requieren propiedades MAPI personalizadas.</span><span class="sxs-lookup"><span data-stu-id="1ca48-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="1ca48-145">Para obtener más información, vea [Enviar mensajes con TNEF](sending-messages-with-tnef.md).</span><span class="sxs-lookup"><span data-stu-id="1ca48-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1ca48-146">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1ca48-146">MFCMAPI reference</span></span>

<span data-ttu-id="1ca48-147">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1ca48-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1ca48-148">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="1ca48-148">**File**</span></span>|<span data-ttu-id="1ca48-149">**Función**</span><span class="sxs-lookup"><span data-stu-id="1ca48-149">**Function**</span></span>|<span data-ttu-id="1ca48-150">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1ca48-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ca48-151">Mapiabfunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1ca48-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="1ca48-152">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="1ca48-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="1ca48-153">MFCMAPI usa el **método CreateOneOff** para crear un identificador de entrada para una dirección que no se encuentra en ninguna libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="1ca48-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ca48-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1ca48-154">See also</span></span>



[<span data-ttu-id="1ca48-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="1ca48-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="1ca48-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1ca48-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="1ca48-157">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="1ca48-157">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

