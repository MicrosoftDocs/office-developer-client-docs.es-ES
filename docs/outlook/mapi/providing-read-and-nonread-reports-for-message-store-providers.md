---
title: Proporcionar informes leídos y no leídos para proveedores de almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432341"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="079e2-103">Proporcionar informes leídos y no leídos para proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="079e2-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="079e2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="079e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="079e2-105">Si un proveedor de almacén de mensajes puede recibir mensajes, es necesario que admita informes de lectura e informes no leídos de los mensajes recibidos por el proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="079e2-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="079e2-106">Si un mensaje recibido contiene la propiedad **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) y el valor de esa propiedad es TRUE, el almacén de mensajes debe enviar un mensaje de notificación al remitente cuando el usuario abra el mensaje, indicando que el mensaje se ha leído.</span><span class="sxs-lookup"><span data-stu-id="079e2-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="079e2-107">Del mismo modo, si el usuario elimina el mensaje antes de abrirlo, el almacén de mensajes debe emitir una respuesta al remitente que indique que el mensaje no se leyó.</span><span class="sxs-lookup"><span data-stu-id="079e2-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="079e2-108">Emitir estos informes es cuestión de crear un objeto [IMessage : IMAPIProp,](imessageimapiprop.md) rellenar las propiedades relevantes del mensaje y enviarlo a la cola MAPI como si el mensaje se hubiera originado con el usuario.</span><span class="sxs-lookup"><span data-stu-id="079e2-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="079e2-109">Para ello, se puede usar el método [IMAPISupport::ReadReceipt.](imapisupport-readreceipt.md)</span><span class="sxs-lookup"><span data-stu-id="079e2-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="079e2-110">Se debe tener especial cuidado cuando un almacén de mensajes hace copias de un mensaje no leído con informes pendientes leídos o no leídos.</span><span class="sxs-lookup"><span data-stu-id="079e2-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="079e2-111">Estos informes no deben generarse cuando los usuarios leen copias de un mensaje para el que se han solicitado informes.</span><span class="sxs-lookup"><span data-stu-id="079e2-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="079e2-112">Al realizar una copia de dicho mensaje, el proveedor del almacén de mensajes debe incluir las marcas CLEAR_RN_PENDING y CLEAR_NRN_PENDING en sus llamadas a [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) e [IMessage::SetReadFlag](imessage-setreadflag.md).</span><span class="sxs-lookup"><span data-stu-id="079e2-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="079e2-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="079e2-113">See also</span></span>



[<span data-ttu-id="079e2-114">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="079e2-114">Message Store Features</span></span>](message-store-features.md)

