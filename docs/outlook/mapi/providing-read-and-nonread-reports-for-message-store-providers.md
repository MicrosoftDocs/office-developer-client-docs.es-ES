---
title: Suministro de informes leídos y no leídos para proveedores de almacenamiento de mensajes
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
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="4f08e-103">Suministro de informes leídos y no leídos para proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="4f08e-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="4f08e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f08e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f08e-105">Si un proveedor de almacenamiento de mensajes puede recibir mensajes, es necesario que admita informes de lectura y informes no leídos de mensajes recibidos por el proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4f08e-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="4f08e-106">Si un mensaje recibido contiene la propiedad **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) y el valor de dicha propiedad es true, el almacén de mensajes debería enviar un mensaje de notificación al remitente cuando el usuario abra el mensaje, que indica que se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4f08e-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="4f08e-107">De forma similar, si el usuario elimina el mensaje antes de abrirlo, el almacén de mensajes debe emitir una respuesta al remitente que indica que no se leyó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4f08e-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="4f08e-108">La emisión de estos informes es una cuestión de crear un objeto [IMessage: IMAPIProp](imessageimapiprop.md) , rellenar las propiedades relevantes del mensaje y enviarlo a la cola de espera de MAPI como si el mensaje se hubiera originado con el usuario.</span><span class="sxs-lookup"><span data-stu-id="4f08e-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="4f08e-109">Se puede usar el método [IMAPISupport:: ReadReceipt](imapisupport-readreceipt.md) para esto.</span><span class="sxs-lookup"><span data-stu-id="4f08e-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4f08e-110">Debe tener especial cuidado cuando un almacén de mensajes realice copias de un mensaje no leído con informes de lectura o no leídos pendientes.</span><span class="sxs-lookup"><span data-stu-id="4f08e-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="4f08e-111">Estos informes no deben generarse cuando los usuarios lean copias de un mensaje para el que se han solicitado informes.</span><span class="sxs-lookup"><span data-stu-id="4f08e-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="4f08e-112">Al realizar una copia de este tipo de mensajes, el proveedor de almacenamiento de mensajes debe incluir las marcas CLEAR_RN_PENDING y CLEAR_NRN_PENDING en sus llamadas a [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) y [IMessage:: SetReadFlag](imessage-setreadflag.md).</span><span class="sxs-lookup"><span data-stu-id="4f08e-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f08e-113">Ver también</span><span class="sxs-lookup"><span data-stu-id="4f08e-113">See also</span></span>



[<span data-ttu-id="4f08e-114">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="4f08e-114">Message Store Features</span></span>](message-store-features.md)

