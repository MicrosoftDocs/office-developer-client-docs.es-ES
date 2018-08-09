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
ms.openlocfilehash: fefd81a7d6cdfda24df93ec928cd3305cb8ef8be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817129"
---
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="36d46-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="36d46-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="36d46-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="36d46-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="36d46-105">Crea un identificador de entrada para una dirección de uso único.</span><span class="sxs-lookup"><span data-stu-id="36d46-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="36d46-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36d46-106">Parameters</span></span>

 <span data-ttu-id="36d46-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="36d46-107">_lpszName_</span></span>
  
> <span data-ttu-id="36d46-108">[entrada] Un puntero al valor de la propiedad del destinatario **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="36d46-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="36d46-109">El parámetro _lpszName_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="36d46-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="36d46-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="36d46-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="36d46-111">[entrada] Un puntero para el tipo de dirección del destinatario, como FAX o SMTP.</span><span class="sxs-lookup"><span data-stu-id="36d46-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="36d46-112">El parámetro _lpszAdrType_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="36d46-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="36d46-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="36d46-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="36d46-114">[entrada] Un puntero a la dirección del destinatario.</span><span class="sxs-lookup"><span data-stu-id="36d46-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="36d46-115">El parámetro _lpszAddress_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="36d46-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="36d46-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36d46-116">_ulFlags_</span></span>
  
> <span data-ttu-id="36d46-117">[entrada] Una máscara de bits de indicadores que influye en el destinatario de uso único.</span><span class="sxs-lookup"><span data-stu-id="36d46-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="36d46-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="36d46-118">The following flags can be set:</span></span>
    
<span data-ttu-id="36d46-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="36d46-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="36d46-120">El destinatario no puede controlar el contenido del mensaje con formato.</span><span class="sxs-lookup"><span data-stu-id="36d46-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="36d46-121">Si se establece MAPI_SEND_NO_RICH_INFO, MAPI establece la propiedad del destinatario **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) en FALSE.</span><span class="sxs-lookup"><span data-stu-id="36d46-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="36d46-122">Si MAPI_SEND_NO_RICH_INFO no está establecido, MAPI establece esta propiedad en TRUE, a menos que se interpreta la dirección del destinatario mensajería indicada por _lpszAddress_ para que sea una dirección de Internet.</span><span class="sxs-lookup"><span data-stu-id="36d46-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="36d46-123">En este caso, MAPI establece **PR_SEND_RICH_INFO** en FALSE.</span><span class="sxs-lookup"><span data-stu-id="36d46-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="36d46-124">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="36d46-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="36d46-125">El nombre para mostrar, el tipo de dirección y la dirección están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="36d46-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="36d46-126">Si no está establecido el indicador MAPI_UNICODE., estas cadenas se encuentran en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="36d46-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="36d46-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="36d46-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="36d46-128">[out] Un puntero para el número de bytes en el identificador de entrada indicado por el parámetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="36d46-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="36d46-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="36d46-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="36d46-130">[out] Un puntero a un puntero al identificador de entrada para el destinatario de uso único.</span><span class="sxs-lookup"><span data-stu-id="36d46-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36d46-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36d46-131">Return value</span></span>

<span data-ttu-id="36d46-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="36d46-132">S_OK</span></span> 
  
> <span data-ttu-id="36d46-133">El identificador de entrada único se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="36d46-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36d46-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="36d46-134">Remarks</span></span>

<span data-ttu-id="36d46-135">Los clientes llaman al método **CreateOneOff** para crear un identificador de entrada para un destinatario de uso único, un destinatario que no pertenezcan a cualquiera de los contenedores desde cualquiera de los proveedores de la libreta de direcciones cargada actualmente.</span><span class="sxs-lookup"><span data-stu-id="36d46-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="36d46-136">Destinatarios de uso único pueden tener cualquier tipo de dirección que es compatible con uno de los proveedores de la libreta de direcciones activa para la sesión.</span><span class="sxs-lookup"><span data-stu-id="36d46-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="36d46-137">Los destinatarios de este tipo normalmente se crean con una plantilla para su tipo de dirección concreto.</span><span class="sxs-lookup"><span data-stu-id="36d46-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="36d46-138">El proveedor de libreta de direcciones que admite el tipo de dirección proporciona la plantilla.</span><span class="sxs-lookup"><span data-stu-id="36d46-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="36d46-139">Un usuario de una aplicación cliente escribe la información relevante en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="36d46-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="36d46-140">MAPI admite cadenas de caracteres Unicode para el nombre para mostrar, el tipo de dirección y los parámetros de la dirección de **CreateOneOff**.</span><span class="sxs-lookup"><span data-stu-id="36d46-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="36d46-141">El indicador MAPI_SEND_NO_RICH_INFO controla si el texto con formato en el formato de texto enriquecido (RTF) se envía junto con cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="36d46-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="36d46-142">El formato de transporte de encapsulación neutro (TNEF): un formato que se utiliza para transmitir con formato de texto, se envía por la mayoría de los proveedores de transporte, independientemente de cómo el destinatario establece su propiedad **PR_SEND_RICH_INFO** .</span><span class="sxs-lookup"><span data-stu-id="36d46-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="36d46-143">No es un problema para los clientes que funcionan con mensajes interpersonales de mensajería.</span><span class="sxs-lookup"><span data-stu-id="36d46-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="36d46-144">Sin embargo, debido a que TNEF normalmente se usa para enviar las propiedades personalizadas para las clases de mensaje personalizadas, no se admite puede ser un problema para los clientes basada en formularios o los clientes que requieren las propiedades personalizadas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="36d46-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="36d46-145">Para obtener más información, consulte [Envío de mensajes con TNEF](sending-messages-with-tnef.md).</span><span class="sxs-lookup"><span data-stu-id="36d46-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="36d46-146">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="36d46-146">MFCMAPI reference</span></span>

<span data-ttu-id="36d46-147">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="36d46-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="36d46-148">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="36d46-148">**File**</span></span>|<span data-ttu-id="36d46-149">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="36d46-149">**Function**</span></span>|<span data-ttu-id="36d46-150">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="36d46-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36d46-151">Mapiabfunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="36d46-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="36d46-152">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="36d46-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="36d46-153">MFCMAPI usa el método **CreateOneOff** para crear un identificador de entrada para una dirección que no se encuentra en cualquier libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="36d46-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36d46-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="36d46-154">See also</span></span>



[<span data-ttu-id="36d46-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="36d46-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="36d46-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="36d46-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="36d46-157">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="36d46-157">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

