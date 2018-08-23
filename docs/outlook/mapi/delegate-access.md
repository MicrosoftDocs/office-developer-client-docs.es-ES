---
title: Acceso delegado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a863494f-0071-4d97-a6c4-26707ee00e04
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 69945bc03d9183ea18a436186523741ce534b71e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568493"
---
# <a name="delegate-access"></a><span data-ttu-id="fb21e-103">Acceso delegado</span><span class="sxs-lookup"><span data-stu-id="fb21e-103">Delegate Access</span></span>

  
  
<span data-ttu-id="fb21e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb21e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb21e-p101">Acceso delegado hace referencia a la capacidad del usuario para enviar un mensaje como otro usuario o recibir un mensaje de otro usuario. Acceso delegado es una caracter�stica independiente del proveedor de servicio de MAPI que admiten los proveedores de transporte si eligen. Sin embargo, ning�n proveedor es necesario para hacerlo. Acceso delegado es valioso cuando sea necesario para un usuario enviar mensajes como o filtrar los mensajes entrantes de otro usuario o al usuario debe tener acceso al almac�n de mensajes de otro usuario. Antes de permitir que un usuario delegado conectar al almac�n de otro usuario, el proveedor de almacenamiento de mensaje debe comprobar que el usuario delegado tiene la autoridad apropiada.</span><span class="sxs-lookup"><span data-stu-id="fb21e-p101">Delegate access refers to the user's ability to send a message as another user or receive a message for another user. Delegate access is a service provider-independent feature of MAPI that transport providers can support if they choose. However, no provider is required to do so. Delegate access is valuable when it is necessary for a user to send messages as, or filter incoming messages for, another user or when a user must access another user's message store. Before allowing a delegate user to connect to another user's store, the message store provider must verify that the delegate user has the proper authority.</span></span> 
  
<span data-ttu-id="fb21e-110">Hay dos grupos de propiedades que se usan para admitir el acceso de delegado:</span><span class="sxs-lookup"><span data-stu-id="fb21e-110">There are two groups of properties that are used to support delegate access:</span></span>
  
 <span data-ttu-id="fb21e-111">**PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fb21e-111">**PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="fb21e-112">**PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fb21e-112">**PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md))</span></span> 
  
 <span data-ttu-id="fb21e-113">**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fb21e-113">**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="fb21e-114">**PR_SENT_REPRESENTING_NAME de MAPI** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fb21e-114">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span> 
  
 <span data-ttu-id="fb21e-115">**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fb21e-115">**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))</span></span> 
  
 <span data-ttu-id="fb21e-116">**PR_RCVD_REPRESENTING_ADDRTYPE** ([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fb21e-116">**PR_RCVD_REPRESENTING_ADDRTYPE** ([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="fb21e-117">**PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fb21e-117">**PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md))</span></span> 
  
 <span data-ttu-id="fb21e-118">**PR_RCVD_REPRESENTING_ENTRYID de MAPI** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fb21e-118">**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="fb21e-119">**PR_RCVD_REPRESENTING_NAME de MAPI** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fb21e-119">**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))</span></span> 
  
 <span data-ttu-id="fb21e-120">**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fb21e-120">**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))</span></span> 
  
<span data-ttu-id="fb21e-p102">En los mensajes salientes, las propiedades de **PR_SENT_REPRESENTING** identifican al usuario de mensajer�a que debe actuar como el remitente. Los clientes pueden establecer estas propiedades como una opci�n. Si no se establecen las propiedades de **PR_SENT_REPRESENTING** con el tiempo el mensaje llega a un proveedor de transporte que admite el acceso delegado, es responsabilidad del proveedor para establecerlas junto con las propiedades de **PR_SENDER**.</span><span class="sxs-lookup"><span data-stu-id="fb21e-p102">On outgoing messages, the **PR_SENT_REPRESENTING** properties identify the messaging user that should act as the sender. Clients can set these properties as an option. If the **PR_SENT_REPRESENTING** properties are not set by the time the message reaches a transport provider that supports delegate access, it is the provider's responsibility to set them along with the **PR_SENDER** properties.</span></span> 
  
<span data-ttu-id="fb21e-p103">En los mensajes entrantes, las propiedades de **PR_RCVD_REPRESENTING** identifican al usuario que debe actuar como el destinatario. Los proveedores de transporte responsable de entregar los mensajes de delegado deben establecer las propiedades de los **PR_RCVD_REPRESENTING** y **PR_RECEIVED_BY**. Los clientes de recibir un mensaje de delegado deben copiar los valores de las propiedades **PR_SENT_REPRESENTING** a las propiedades de **PR_RCVD_REPRESENTING** correspondientes.</span><span class="sxs-lookup"><span data-stu-id="fb21e-p103">On incoming messages, the **PR_RCVD_REPRESENTING** properties identify the user that should act as the recipient. Transport providers responsible for delivering delegate messages must set both the **PR_RCVD_REPRESENTING** and **PR_RECEIVED_BY** properties. Clients receiving a delegate message should copy the values of the **PR_SENT_REPRESENTING** properties to the corresponding **PR_RCVD_REPRESENTING** properties.</span></span> 
  
<span data-ttu-id="fb21e-p104">Por ejemplo, suponga que John est� recibiendo mensajes de Mar�a mientras Mar�a est� de vacaciones. Las propiedades de **PR_RCVD_REPRESENTING** identifican John como el destinatario de delegado. Cuando Juan env�a una respuesta a un mensaje que ha recibido para Mar�a, las propiedades del mensaje **PR_SENDER** identifican John como el remitente. Debido a que John representa a Mar�a, las propiedades de **PR_SENT_REPRESENTING** identifican Mar�a.</span><span class="sxs-lookup"><span data-stu-id="fb21e-p104">For example, suppose John is receiving Sally's messages while Sally is on vacation. The **PR_RCVD_REPRESENTING** properties identify John as the delegate recipient. When John sends a reply to a message that he has received for Sally, the message's **PR_SENDER** properties identify John as the sender. Because John is representing Sally, the **PR_SENT_REPRESENTING** properties identify Sally.</span></span> 
  
<span data-ttu-id="fb21e-p105">Los mensajes entrantes de delegado de tratamiento normalmente deben enviar estos mensajes como el usuario de mensajer�a identificado por las propiedades **PR_SENT_REPRESENTING** en lugar de como el usuario identificado por las propiedades de **PR_SENDER** los proveedores de transporte. La excepci�n a esta regla es cuando sea necesario para que coincida con los tipos de privilegio y transporte de access. En este caso, un proveedor de transporte puede elegir una identidad de env�a.</span><span class="sxs-lookup"><span data-stu-id="fb21e-p105">Transport providers handling incoming delegate messages should usually deliver these messages as the messaging user identified by the **PR_SENT_REPRESENTING** properties rather than as the user identified by the **PR_SENDER** properties. The exception to this rule is when it is necessary to match access privilege and transport types. In this case, a transport provider can choose a sending identity.</span></span> 
  
<span data-ttu-id="fb21e-p106">Si las propiedades de **PR_SENT_REPRESENTING** est�n disponibles para un mensaje entrante de delegado, el proveedor de transporte controlar entrega debe establecer, con los valores de las propiedades correspondientes de **PR_SENDER**. Si las propiedades de **PR_SENT_REPRESENTING** est�n disponibles, pero el proveedor de transporte no admite el acceso de delegado, puede usar las propiedades de **PR_SENDER** para la entrega.</span><span class="sxs-lookup"><span data-stu-id="fb21e-p106">If the **PR_SENT_REPRESENTING** properties are unavailable for an incoming delegate message, the transport provider handling delivery must set them, using the values of the corresponding **PR_SENDER** properties. If the **PR_SENT_REPRESENTING** properties are available but the transport provider does not support delegate access, it can use the **PR_SENDER** properties for delivery.</span></span> 
  

