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
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="3d210-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="3d210-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="3d210-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d210-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d210-105">Crea un identificador de entrada para una dirección de uso único.</span><span class="sxs-lookup"><span data-stu-id="3d210-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="3d210-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3d210-106">Parameters</span></span>

 <span data-ttu-id="3d210-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="3d210-107">_lpszName_</span></span>
  
> <span data-ttu-id="3d210-108">a Un puntero al valor de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) del destinatario.</span><span class="sxs-lookup"><span data-stu-id="3d210-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="3d210-109">El parámetro _lpszName_ puede ser null.</span><span class="sxs-lookup"><span data-stu-id="3d210-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="3d210-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="3d210-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="3d210-111">a Un puntero al tipo de dirección del destinatario, como FAX o SMTP.</span><span class="sxs-lookup"><span data-stu-id="3d210-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="3d210-112">El parámetro _lpszAdrType_ no puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="3d210-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="3d210-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="3d210-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="3d210-114">a Puntero a la dirección del destinatario.</span><span class="sxs-lookup"><span data-stu-id="3d210-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="3d210-115">El parámetro _lpszAddress_ no puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="3d210-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="3d210-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3d210-116">_ulFlags_</span></span>
  
> <span data-ttu-id="3d210-117">a Máscara de bits de marcas que afecta al destinatario de uso único.</span><span class="sxs-lookup"><span data-stu-id="3d210-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="3d210-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="3d210-118">The following flags can be set:</span></span>
    
<span data-ttu-id="3d210-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="3d210-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="3d210-120">El destinatario no puede controlar el contenido del mensaje con formato.</span><span class="sxs-lookup"><span data-stu-id="3d210-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="3d210-121">Si se establece MAPI_SEND_NO_RICH_INFO, MAPI establece la propiedad **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) del destinatario en false.</span><span class="sxs-lookup"><span data-stu-id="3d210-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="3d210-122">Si no se establece MAPI_SEND_NO_RICH_INFO, MAPI establece esta propiedad en TRUE a menos que la dirección de mensajería del destinatario apuntado por _lpszAddress_ se interprete como una dirección de Internet.</span><span class="sxs-lookup"><span data-stu-id="3d210-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="3d210-123">En este caso, MAPI establece **PR_SEND_RICH_INFO** en false.</span><span class="sxs-lookup"><span data-stu-id="3d210-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="3d210-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3d210-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3d210-125">El nombre para mostrar, el tipo de dirección y la dirección están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="3d210-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="3d210-126">Si no se establece la marca MAPI_UNICODE, estas cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="3d210-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="3d210-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3d210-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="3d210-128">contempla Un puntero al recuento de bytes en el identificador de entrada al que apunta el parámetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="3d210-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="3d210-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="3d210-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="3d210-130">contempla Un puntero a un puntero al identificador de entrada para el destinatario de uso único.</span><span class="sxs-lookup"><span data-stu-id="3d210-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3d210-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d210-131">Return value</span></span>

<span data-ttu-id="3d210-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="3d210-132">S_OK</span></span> 
  
> <span data-ttu-id="3d210-133">El identificador de entrada único se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3d210-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3d210-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d210-134">Remarks</span></span>

<span data-ttu-id="3d210-135">Los clientes llaman al método **CreateOneOff** para crear un identificador de entrada para un destinatario de un solo uso: un destinatario que no pertenece a ninguno de los contenedores de ninguno de los proveedores de libreta de direcciones cargados actualmente.</span><span class="sxs-lookup"><span data-stu-id="3d210-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="3d210-136">Los destinatarios de uso único pueden tener cualquier tipo de dirección compatible con uno de los proveedores de libreta de direcciones activos para la sesión.</span><span class="sxs-lookup"><span data-stu-id="3d210-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="3d210-137">Normalmente, los destinatarios de uso único se crean con una plantilla para su tipo de dirección en particular.</span><span class="sxs-lookup"><span data-stu-id="3d210-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="3d210-138">El proveedor de la libreta de direcciones que admite el tipo de dirección proporciona la plantilla.</span><span class="sxs-lookup"><span data-stu-id="3d210-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="3d210-139">Un usuario de una aplicación cliente introduce la información relevante en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="3d210-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="3d210-140">MAPI admite las cadenas de caracteres Unicode para el nombre para mostrar, el tipo de dirección y los parámetros de dirección de **CreateOneOff**.</span><span class="sxs-lookup"><span data-stu-id="3d210-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="3d210-141">El indicador MAPI_SEND_NO_RICH_INFO controla si se envía texto con formato en formato de texto enriquecido (RTF) junto con cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="3d210-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="3d210-142">La mayoría de los proveedores de transporte envían el formato de encapsulamiento neutro para el transporte (TNEF) (un formato que se usa para transmitir texto con formato), independientemente de cómo el destinatario establezca su propiedad **PR_SEND_RICH_INFO** .</span><span class="sxs-lookup"><span data-stu-id="3d210-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="3d210-143">Esto no es un problema para los clientes de mensajería que funcionan con mensajes interpersonales.</span><span class="sxs-lookup"><span data-stu-id="3d210-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="3d210-144">Sin embargo, dado que TNEF suele usarse para enviar propiedades personalizadas para clases de mensaje personalizadas, no es necesario que el soporte técnico pueda ser un problema para los clientes basados en formularios o clientes que requieran propiedades MAPI personalizadas.</span><span class="sxs-lookup"><span data-stu-id="3d210-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="3d210-145">Para obtener más información, vea [enviar mensajes con TNEF](sending-messages-with-tnef.md).</span><span class="sxs-lookup"><span data-stu-id="3d210-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3d210-146">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3d210-146">MFCMAPI reference</span></span>

<span data-ttu-id="3d210-147">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="3d210-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3d210-148">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="3d210-148">**File**</span></span>|<span data-ttu-id="3d210-149">**Función**</span><span class="sxs-lookup"><span data-stu-id="3d210-149">**Function**</span></span>|<span data-ttu-id="3d210-150">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="3d210-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3d210-151">Mapiabfunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="3d210-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="3d210-152">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="3d210-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="3d210-153">MFCMAPI usa el método **CreateOneOff** para crear un identificador de entrada para una dirección que no se encuentra en ninguna libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3d210-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3d210-154">Ver también</span><span class="sxs-lookup"><span data-stu-id="3d210-154">See also</span></span>



[<span data-ttu-id="3d210-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="3d210-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="3d210-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3d210-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="3d210-157">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="3d210-157">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

