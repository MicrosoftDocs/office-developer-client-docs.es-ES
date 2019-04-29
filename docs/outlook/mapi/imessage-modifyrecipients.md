---
title: IMessageModifyRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.ModifyRecipients
api_type:
- COM
ms.assetid: 2625f29d-325f-417d-bcec-49d580f9cd7e
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 07e1c2104068a6eb242e8ba81f91655edaa92cd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426243"
---
# <a name="imessagemodifyrecipients"></a><span data-ttu-id="cd3a8-103">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="cd3a8-103">IMessage::ModifyRecipients</span></span>

  
  
<span data-ttu-id="cd3a8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd3a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd3a8-105">Agrega, elimina o modifica a los destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-105">Adds, deletes, or modifies message recipients.</span></span>
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a><span data-ttu-id="cd3a8-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd3a8-106">Parameters</span></span>

 <span data-ttu-id="cd3a8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cd3a8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cd3a8-p101">[entrada] M�scara de bits de indicadores que controla los cambios de destinatarios. Si se pasa cero para el par�metro  _ulFlags_, **ModifyRecipients** reemplaza a todos los destinatarios existentes con la lista de destinatarios que apunta el par�metro  _lpMods_. Pueden establecer los siguientes indicadores para  _ulFlags_:</span><span class="sxs-lookup"><span data-stu-id="cd3a8-p101">[in] Bitmask of flags that controls the recipient changes. If zero is passed for the  _ulFlags_ parameter, **ModifyRecipients** replaces all existing recipients with the recipient list pointed to by the  _lpMods_ parameter. The following flags can be set for  _ulFlags_:</span></span>
    
<span data-ttu-id="cd3a8-111">MODRECIP_ADD</span><span class="sxs-lookup"><span data-stu-id="cd3a8-111">MODRECIP_ADD</span></span> 
  
> <span data-ttu-id="cd3a8-112">Los destinatarios que apunta el par�metro  _lpMods_ deben agregarse a la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-112">The recipients pointed to by the  _lpMods_ parameter should be added to the recipient list.</span></span> 
    
<span data-ttu-id="cd3a8-113">MODRECIP_MODIFY</span><span class="sxs-lookup"><span data-stu-id="cd3a8-113">MODRECIP_MODIFY</span></span> 
  
> <span data-ttu-id="cd3a8-p102">Los destinatarios que apunta el par�metro  _lpMods_ deben reemplazar a los destinatarios existentes. Todas las propiedades existentes se reemplazan por las de la estructura [ADRENTRY](adrentry.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-p102">The recipients pointed to by the  _lpMods_ parameter should replace existing recipients. All of the existing properties are replaced by those in the corresponding [ADRENTRY](adrentry.md) structure.</span></span> 
    
<span data-ttu-id="cd3a8-116">MODRECIP_REMOVE</span><span class="sxs-lookup"><span data-stu-id="cd3a8-116">MODRECIP_REMOVE</span></span> 
  
> <span data-ttu-id="cd3a8-117">Los destinatarios existentes deben quitarse de la lista de destinatarios utilizando como índice la propiedad **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) incluida en la matriz de valores de propiedad de cada entrada de destinatario en el parámetro _lpMods_ .</span><span class="sxs-lookup"><span data-stu-id="cd3a8-117">Existing recipients should be removed from the recipient list using as an index the **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) property included in the property value array of each recipient entry in the  _lpMods_ parameter.</span></span> 
    
 <span data-ttu-id="cd3a8-118">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="cd3a8-118">_lpMods_</span></span>
  
> <span data-ttu-id="cd3a8-119">[entrada] Puntero a una estructura [ADRLIST](adrlist.md) que contiene una lista de destinatarios para agregar, eliminar o modificar en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-119">[in] Pointer to an [ADRLIST](adrlist.md) structure that contains a list of recipients to be added, deleted, or modified in the message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cd3a8-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd3a8-120">Return value</span></span>

<span data-ttu-id="cd3a8-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd3a8-121">S_OK</span></span> 
  
> <span data-ttu-id="cd3a8-122">La lista de destinatarios se modific� correctamente.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-122">The recipient list was successfully modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cd3a8-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd3a8-123">Remarks</span></span>

<span data-ttu-id="cd3a8-p103">El m�todo **IMessage::ModifyRecipients** cambia la lista de destinatarios del mensaje. Es en esta lista, que se celebran en una estructura [ADRLIST](adrlist.md) , que se basa la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-p103">The **IMessage::ModifyRecipients** method changes the message's recipient list. It is from this list, held in an [ADRLIST](adrlist.md) structure, that the recipient table is built.</span></span> 
  
<span data-ttu-id="cd3a8-126">La estructura **ADRLIST** contiene una estructura [ADRENTRY](adrentry.md) para cada destinatario y cada estructura **ADRENTRY** contiene una matriz de valores de propiedad que describe las propiedades del destinatario.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-126">The **ADRLIST** structure contains one [ADRENTRY](adrentry.md) structure for each recipient and each **ADRENTRY** structure contains an array of property values describing the recipient properties.</span></span> 
  
<span data-ttu-id="cd3a8-127">Los destinatarios de la estructura **ADRLIST** se pueden resolver o sin resolver.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-127">Recipients in the **ADRLIST** structure can be resolved or unresolved.</span></span> <span data-ttu-id="cd3a8-128">La diferencia est� en el n�mero y tipo de propiedades que se incluyen.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-128">The difference is in the number and type of properties that are included.</span></span> <span data-ttu-id="cd3a8-129">Un destinatario sin resolver contiene solo las propiedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), mientras que un destinatario resuelto contiene esas dos propiedades más \*\*PR_ADDRTYPE \*\*([PidTagAddressType](pidtagaddresstype-canonical-property.md)) y \*\*\*\* [PidTagEntryId](pidtagentryid-canonical-property.md)(en inglés).</span><span class="sxs-lookup"><span data-stu-id="cd3a8-129">An unresolved recipient contains only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) properties while a resolved recipient contains those two properties plus **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span> <span data-ttu-id="cd3a8-130">Si **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) está disponible, también puede incluirse.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-130">If **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is available, it can be included also.</span></span>
  
<span data-ttu-id="cd3a8-p105">En el momento en que se env�a un mensaje, deben incluir s�lo los destinatarios resueltos en su lista de destinatarios. Destinatarios sin resolver dar lugar a informes de entrega que se crea y se env�a al remitente del mensaje original. Para obtener m�s informaci�n acerca del proceso de resoluci�n de nombres desde la perspectiva del cliente, vea la [resoluci�n de un nombre](resolving-a-recipient-name.md). Para obtener m�s informaci�n desde la perspectiva de la libreta de direcciones, vea [Implementaci�n de resoluci�n de nombres](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="cd3a8-p105">By the time a message is submitted, it must include only resolved recipients in its recipient list. Unresolved recipients cause nondelivery reports to be created and sent to the original sender of the message. For more information about the name resolution process from the client perspective, see [Resolving a Name](resolving-a-recipient-name.md). For more information from the perspective of the address book provider, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="cd3a8-p106">Adem�s de los destinatarios resueltos y no resueltos, un destinatario puede ser NULL. El miembro **cValues** de la estructura de **ADRENTRY** para el destinatario se establece en cero y el miembro **rgPropVals** se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-p106">In addition to resolved and unresolved recipients, a recipient can be NULL. The **cValues** member of the **ADRENTRY** structure for the recipient is set to zero and the **rgPropVals** member is set to NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cd3a8-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="cd3a8-137">Notes to callers</span></span>

<span data-ttu-id="cd3a8-p107">Puede crear una lista de destinatarios mediante una llamada a [IAddrBook::Address](imapisupport-address.md) para mostrar el cuadro de di�logo com�n y pedir al usuario que seleccione entradas. La lista de direcciones que apunta el par�metro  _lppAdrList_ a **Address** se pueden pasar a **ModifyRecipients** como el par�metro  _lpMods_.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-p107">You can create a recipient list by calling [IAddrBook::Address](imapisupport-address.md) to display the common dialog box and prompt the user to select entries. The address list pointed to by the  _lppAdrList_ parameter to **Address** can be passed to **ModifyRecipients** as the  _lpMods_ parameter.</span></span> 
  
<span data-ttu-id="cd3a8-p108">Al especificar las propiedades para un destinatario de la estructura [ADRLIST](adrlist.md) , incluye todas las propiedades del destinatario, no s�lo los nuevos o modificados. Cuando se modifica un destinatario, se eliminan todas las propiedades que no se incluyen en la estructura de **ADRLIST**. Para recuperar el conjunto actual de propiedades para todos los destinatarios de un mensaje, llame [GetRecipientTable](imessage-getrecipienttable.md) y recuperar todas las filas. Dado que es id�ntico en estructura a un **ADRLIST**un **SRowSet**, puede utilizar indistintamente ellos.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-p108">When you specify properties for a recipient in the [ADRLIST](adrlist.md) structure, include all of the recipient's properties, not only the new or changed ones. When a recipient is modified, any properties not included in the **ADRLIST** structure are deleted. To retrieve the current set of properties for all of a message's recipients, call [GetRecipientTable](imessage-getrecipienttable.md) and retrieve all of the rows. Because an **SRowSet** is identical in structure to an **ADRLIST**, you can use them interchangeably.</span></span>
  
 <span data-ttu-id="cd3a8-144">**ModifyRecipients** reemplaza todas las entradas en la lista de destinatarios actual con la informaci�n que se�ala  _lpMods_ cuando ninguno de los indicadores se establecen en el par�metro  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-144">**ModifyRecipients** replaces all of the entries in the current recipient list with the information pointed to by  _lpMods_ when none of the flags are set in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cd3a8-145">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="cd3a8-145">Notes to callers</span></span>

<span data-ttu-id="cd3a8-p109">Cuando se establece la marca MODRECIP_MODIFY, **ModifyRecipients** reemplaza cada destinatario toda la fila con la fila asociada en la estructura [ADRLIST](adrlist.md) pasada en  _lpMods_. Tenga cuidado especificar todas las propiedades que debe tener un destinatario independientemente de si han cambiado para impedir que se va a eliminar accidentalmente.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-p109">When you set the MODRECIP_MODIFY flag, **ModifyRecipients** replaces each entire recipient row with the associated row in the [ADRLIST](adrlist.md) structure passed in  _lpMods_. Be careful to specify all of the properties that a recipient should have regardless of whether they have changed to prevent them from being unintentionally deleted.</span></span>
  
<span data-ttu-id="cd3a8-148">A continuaci�n se muestran algunas reglas para establecer las propiedades de los destinatarios en la estructura de **ADRLIST**:</span><span class="sxs-lookup"><span data-stu-id="cd3a8-148">Following are some rules for setting the properties of the recipients in the **ADRLIST** structure:</span></span> 
  
- <span data-ttu-id="cd3a8-p110">No use PT_NULL como un tipo de propiedad. **ModifyRecipients** devuelve un error al encontrar este valor.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-p110">Do not use PT_NULL as a property type. **ModifyRecipients** returns an error when encountering this value.</span></span> 
    
- <span data-ttu-id="cd3a8-p111">No use PT_ERROR como un tipo de propiedad. **ModifyRecipients** pasa por alto este valor.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-p111">Do not use PT_ERROR as a property type. **ModifyRecipients** ignores this value.</span></span> 
    
- <span data-ttu-id="cd3a8-153">Incluir la propiedad **PR_ROWID** para todos los destinatarios cuando se establece la marca de la MODRECIP_REMOVE o MODRECIP_MODIFY en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-153">Include the **PR_ROWID** property for all recipients when you set either the MODRECIP_REMOVE or MODRECIP_MODIFY flag in  _ulFlags_.</span></span> 
    
- <span data-ttu-id="cd3a8-154">No incluya la propiedad **PR_ROWID** para cualquiera de los destinatarios cuando se establece la marca MODRECIP_ADD en  _ulFlags_ o cuando se pasa cero en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-154">Do not include the **PR_ROWID** property for any of the recipients when you set the MODRECIP_ADD flag in  _ulFlags_ or when you pass zero in  _ulFlags_.</span></span>
    
<span data-ttu-id="cd3a8-p112">Si se incluye la propiedad **PR_ADDRTYPE** o **PR_EMAIL_ADDRESS** (propiedad) para un destinatario y uno o ambos de estas propiedades no son coherentes con el tipo de direcci�n y la direcci�n del destinatario como identificado por **PR_ENTRYID**, los resultados se definen. Es decir, hay tres posibilidades, seg�n el proveedor de servicio:</span><span class="sxs-lookup"><span data-stu-id="cd3a8-p112">If you include either the **PR_ADDRTYPE** property or **PR_EMAIL_ADDRESS** property for a recipient and one or both of these properties are inconsistent with the address type and address of the recipient as identified by **PR_ENTRYID**, the results are undefined. That is, there are three possibilities, depending on the service provider:</span></span>
  
- <span data-ttu-id="cd3a8-157">El mensaje se entregar� en la direcci�n descrita por las propiedades **PR_ADDRTYPE** y **PR_EMAIL_ADDRESS**.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-157">The message will be delivered to the address described by the **PR_ADDRTYPE** and **PR_EMAIL_ADDRESS** properties.</span></span> 
    
- <span data-ttu-id="cd3a8-158">El mensaje se entregar� al destinatario identificado por **PR_ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-158">The message will be delivered to the recipient identified by **PR_ENTRYID**.</span></span>
    
- <span data-ttu-id="cd3a8-159">El mensaje se va a declarar no se puede entregar debido a la ambig�edad de la informaci�n de direcci�n.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-159">The message will be declared undeliverable due to the ambiguity of the address information.</span></span>
    
<span data-ttu-id="cd3a8-p113">Use las reglas de asignaci�n descritas en [Administraci�n de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md) asignar memoria para la lista de destinatarios. **ModifyRecipients** no libere la estructura **ADRLIST** ni ninguna de sus subestructuras. La estructura de **ADRLIST** y cada estructura [SPropValue](spropvalue.md) deben asignarse por separado mediante el uso de la funci�n [MAPIAllocateBuffer](mapiallocatebuffer.md) tal que cada uno de ellos se puede liberar individualmente. Si el m�todo requiere espacio adicional para cualquier estructura **SPropValue**, puede reemplazar la estructura de **SPropValue** con una nueva que m�s adelante se puede liberar mediante [MAPIFreeBuffer](mapifreebuffer.md). La estructura **SPropValue** original tambi�n debe liberarse mediante **MAPIFreeBuffer**.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-p113">Use the allocation rules outlined in [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md) to allocate memory for the recipient list. **ModifyRecipients** does not free the **ADRLIST** structure nor any of its substructures. The **ADRLIST** structure and each [SPropValue](spropvalue.md) structure must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function such that each can be freed individually. If the method requires additional space for any **SPropValue** structure, it can replace the **SPropValue** structure with a new one that can later be freed using [MAPIFreeBuffer](mapifreebuffer.md). The original **SPropValue** structure should also be freed using **MAPIFreeBuffer**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cd3a8-165">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cd3a8-165">MFCMAPI reference</span></span>

<span data-ttu-id="cd3a8-166">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-166">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cd3a8-167">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="cd3a8-167">**File**</span></span>|<span data-ttu-id="cd3a8-168">**Función**</span><span class="sxs-lookup"><span data-stu-id="cd3a8-168">**Function**</span></span>|<span data-ttu-id="cd3a8-169">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="cd3a8-169">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cd3a8-170">MAPIABFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="cd3a8-170">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="cd3a8-171">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="cd3a8-171">AddRecipient</span></span>  <br/> |<span data-ttu-id="cd3a8-172">MFCMAPI, utiliza el m�todo **IMessage::ModifyRecipients** para agregar a un nuevo destinatario a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="cd3a8-172">MFCMAPI uses the **IMessage::ModifyRecipients** method to add a new recipient to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd3a8-173">Ver también</span><span class="sxs-lookup"><span data-stu-id="cd3a8-173">See also</span></span>



[<span data-ttu-id="cd3a8-174">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="cd3a8-174">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="cd3a8-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="cd3a8-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="cd3a8-176">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="cd3a8-176">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="cd3a8-177">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="cd3a8-177">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="cd3a8-178">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="cd3a8-178">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="cd3a8-179">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="cd3a8-179">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="cd3a8-180">SPropValue</span><span class="sxs-lookup"><span data-stu-id="cd3a8-180">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="cd3a8-181">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cd3a8-181">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="cd3a8-182">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="cd3a8-182">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

