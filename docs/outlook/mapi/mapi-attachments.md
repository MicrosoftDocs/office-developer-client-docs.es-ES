---
title: Datos adjuntos de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e6c6ad9-1e07-4234-a5ef-18020d7ce468
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: fd8075d2fddb7ada6803c869cbbd282c464e75bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585881"
---
# <a name="mapi-attachments"></a><span data-ttu-id="c96bd-103">Datos adjuntos de MAPI</span><span class="sxs-lookup"><span data-stu-id="c96bd-103">MAPI Attachments</span></span>

  
  
<span data-ttu-id="c96bd-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c96bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c96bd-105">Algunos proveedores de almac�n de mensajes que los clientes puedan asociar se agreg� informaci�n en forma de archivos, objetos OLE, los mensajes o datos binarios con los mensajes.</span><span class="sxs-lookup"><span data-stu-id="c96bd-105">Some message store providers enable clients to associate added information in the form of files, OLE objects, messages, or binary data with messages.</span></span> <span data-ttu-id="c96bd-106">Esta informaci�n se ha agregado se denomina datos adjuntos de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="c96bd-106">This added information is called a message's attachment.</span></span> <span data-ttu-id="c96bd-107">Debido a que los datos adjuntos se crean, mantienen y tener acceso s�lo a trav�s de sus mensajes, se consideran subobjetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c96bd-107">Because attachments are created, maintained, and accessed only through their messages, they are considered message subobjects.</span></span> <span data-ttu-id="c96bd-108">En lugar de tener un identificador de entrada para obtener acceso, los datos adjuntos tienen conocidos n�mero secuencial como un n�mero de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c96bd-108">Rather than having an entry identifier for access, attachments have a sequential number known as an attachment number.</span></span> <span data-ttu-id="c96bd-109">Este n�mero identifica de forma exclusiva los datos adjuntos de su mensaje, pero no necesariamente en el almac�n de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c96bd-109">This number uniquely identifies the attachment within its message, but not necessarily within the message store.</span></span> <span data-ttu-id="c96bd-110">Dos mensajes diferentes pueden tener diferentes datos adjuntos con el mismo n�mero de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c96bd-110">Two different messages can have different attachments with the same attachment number.</span></span> <span data-ttu-id="c96bd-111">Los números de los datos adjuntos sólo son válidos mientras el mensaje está abierto y se almacenan en la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c96bd-111">Attachment numbers are only valid as long as the message is open and are stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="c96bd-p102">Para obtener acceso a informaci�n de resumen acerca de todos los datos adjuntos de un mensaje, los clientes recuperar su tabla de datos adjuntos. En la tabla de datos adjuntos se incluye informaci�n que los clientes pueden usar para tener acceso a datos adjuntos directamente, como su n�mero de datos adjuntos y la clave de registro. Los clientes pueden recuperar una tabla de datos adjuntos por:</span><span class="sxs-lookup"><span data-stu-id="c96bd-p102">To access summary information about all of a message's attachments, clients retrieve its attachment table. The attachment table includes information that clients can use to access an attachment directly, such as its attachment number and record key. Clients can retrieve an attachment table by:</span></span>
  
- <span data-ttu-id="c96bd-p103">Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="c96bd-p103">Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
- <span data-ttu-id="c96bd-p104">Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="c96bd-p104">Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="c96bd-119">Message store providers are expected to support both of these approaches.</span><span class="sxs-lookup"><span data-stu-id="c96bd-119">Message store providers are expected to support both of these approaches.</span></span> <span data-ttu-id="c96bd-120">El enfoque **OpenProperty** requiere que el llamador especifique IID_IMAPITable como el identificador de interfaz y **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) como la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c96bd-120">The **OpenProperty** approach requires that the caller specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) as the property tag.</span></span> <span data-ttu-id="c96bd-121">**PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table.</span><span class="sxs-lookup"><span data-stu-id="c96bd-121">**PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table.</span></span> <span data-ttu-id="c96bd-122">Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method.</span><span class="sxs-lookup"><span data-stu-id="c96bd-122">Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method.</span></span> <span data-ttu-id="c96bd-123">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span><span class="sxs-lookup"><span data-stu-id="c96bd-123">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span></span>
  
 <span data-ttu-id="c96bd-124">**PR_MESSAGE_ATTACHMENTS** se pueden usar:</span><span class="sxs-lookup"><span data-stu-id="c96bd-124">**PR_MESSAGE_ATTACHMENTS** can be used:</span></span> 
  
- <span data-ttu-id="c96bd-125">Con **IMAPIProp::OpenProperty** para tener acceso a una tabla de datos adjuntos o un destinatario.</span><span class="sxs-lookup"><span data-stu-id="c96bd-125">With **IMAPIProp::OpenProperty** to access an attachment or recipient table.</span></span> 
    
- <span data-ttu-id="c96bd-p106">With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span><span class="sxs-lookup"><span data-stu-id="c96bd-p106">With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span></span>
    
- <span data-ttu-id="c96bd-128">En una restricci�n de subobjetos para indicar que la restricci�n secundarias debe aplicar a los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c96bd-128">In a subobject restriction to indicate that the child restriction should apply to attachments.</span></span>
    
<span data-ttu-id="c96bd-129">For more information, see [Tablas de datos adjuntos](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c96bd-129">For more information, see [Attachment Tables](attachment-tables.md).</span></span>
  

