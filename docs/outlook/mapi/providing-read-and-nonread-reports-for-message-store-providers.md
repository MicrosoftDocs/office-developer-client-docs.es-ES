---
title: Proporcionar informes Nonread y lectura para los proveedores de almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: b082d063cc77be46fcd3d4e07ec6753f78f8f335
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820492"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a><span data-ttu-id="af181-103">Proporcionar informes Nonread y lectura para los proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="af181-103">Providing Read and Nonread Reports for Message Store Providers</span></span>

  
  
<span data-ttu-id="af181-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="af181-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="af181-105">Si un proveedor de almacén de mensajes puede recibir los mensajes, es necesario para admitir la lectura de informes e informes de nonread de los mensajes recibidos por el proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="af181-105">If a message store provider can receive messages, it is required to support read reports and nonread reports of messages received by the message store provider.</span></span> <span data-ttu-id="af181-106">Si un mensaje recibido contiene la propiedad **PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) y el valor de la propiedad es TRUE, el almacén de mensajes debe enviar un mensaje de notificación al remitente cuando el usuario abre el mensaje, que indica que se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="af181-106">If a received message contains the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and that property's value is TRUE, the message store should send a notification message to the sender when the user opens the message, indicating that the message has been read.</span></span> <span data-ttu-id="af181-107">De forma similar, si el usuario elimina el mensaje antes de abrirlo, el almacén de mensajes debe enviar una respuesta al remitente que indica que no se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="af181-107">Similarly, if the user deletes the message before opening it, the message store should issue a reply to the sender indicating that the message was not read.</span></span>
  
<span data-ttu-id="af181-108">Emitir estos informes es una cuestión de creación de un [IMessage: IMAPIProp](imessageimapiprop.md) objeto, rellenar las propiedades relevantes en el mensaje y enviarla a la cola MAPI como si hubiera se originó el mensaje con el usuario.</span><span class="sxs-lookup"><span data-stu-id="af181-108">Issuing these reports is a matter of creating an [IMessage : IMAPIProp](imessageimapiprop.md) object, filling out the relevant properties on the message, and submitting it to the MAPI spooler as if the message had originated with the user.</span></span> <span data-ttu-id="af181-109">El método [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) se puede usar para esto.</span><span class="sxs-lookup"><span data-stu-id="af181-109">The [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) method can be used for this.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="af181-110">Debe prestar especial atención cuando un almacén de mensajes realiza copias de un mensaje no leído con pendientes informes de lectura o nonread.</span><span class="sxs-lookup"><span data-stu-id="af181-110">Special care must be taken when a message store makes copies of an unread message with pending read or nonread reports.</span></span> <span data-ttu-id="af181-111">No se deben generar dichos informes cuando los usuarios leer todas las copias de un mensaje para el que se han solicitado informes.</span><span class="sxs-lookup"><span data-stu-id="af181-111">Such reports should not be generated when users read any copies of a message for which reports have been requested.</span></span> <span data-ttu-id="af181-112">Al realizar una copia de dicho mensaje, el proveedor de almacenamiento de mensaje debe incluir los indicadores CLEAR_RN_PENDING y CLEAR_NRN_PENDING en sus llamadas a [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) y [IMessage::SetReadFlag](imessage-setreadflag.md).</span><span class="sxs-lookup"><span data-stu-id="af181-112">When making a copy of such a message, the message store provider should include the CLEAR_RN_PENDING and CLEAR_NRN_PENDING flags in its calls to [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) and [IMessage::SetReadFlag](imessage-setreadflag.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af181-113">Ver también</span><span class="sxs-lookup"><span data-stu-id="af181-113">See also</span></span>



[<span data-ttu-id="af181-114">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="af181-114">Message Store Features</span></span>](message-store-features.md)

