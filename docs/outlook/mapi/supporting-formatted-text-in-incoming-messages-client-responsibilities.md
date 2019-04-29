---
title: Admitir texto con formato en los mensajes entrantes responsabilidades del cliente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434504"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="1c030-103">Admitir texto con formato en los mensajes entrantes: responsabilidades del cliente</span><span class="sxs-lookup"><span data-stu-id="1c030-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="1c030-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c030-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c030-105">A medida que los mensajes se transfieren entre sistemas de mensajería, la cola MAPI se asegura de que el formato de texto enriquecido permanezca sincronizado con el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1c030-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="1c030-106">La cola MAPI llama a la función [RTFSync](rtfsync.md) desde una versión ajustada del mensaje que pasa al proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1c030-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="1c030-107">El proveedor de transporte guarda los cambios realizados en el mensaje mediante una llamada al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) y, a continuación, lo enruta al nuevo destinatario.</span><span class="sxs-lookup"><span data-stu-id="1c030-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="1c030-108">Cuando la aplicación cliente de RTF del destinatario abre el mensaje para mostrar el texto, debe sincronizar el texto con el formato y abrir **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). , en función de la propiedad que esté disponible.</span><span class="sxs-lookup"><span data-stu-id="1c030-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="1c030-109">**Para abrir un mensaje, los clientes que reconocen RTF**</span><span class="sxs-lookup"><span data-stu-id="1c030-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="1c030-110">Llamar a **RTFSync** para sincronizar el texto del mensaje con el formato si el almacén de mensajes no es compatible con RTF.</span><span class="sxs-lookup"><span data-stu-id="1c030-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="1c030-111">La marca RTF_SYNC_BODY_CHANGED debe pasarse en el parámetro _ulFlags_ si falta la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) o si se establece en false.</span><span class="sxs-lookup"><span data-stu-id="1c030-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="1c030-112">Los clientes que trabajan con almacenes de mensajes conscientes de RTF no tienen que realizar la llamada de **RTFSync** porque el almacén de mensajes se encarga de ello.</span><span class="sxs-lookup"><span data-stu-id="1c030-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="1c030-113">Llame a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) si se ha actualizado el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1c030-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="1c030-114">Llame a [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="1c030-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="1c030-115">Si **PR_RTF_COMPRESSED** no está disponible, debe abrir la propiedad **PR_BODY** en su lugar para mostrar el contenido del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1c030-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="1c030-116">Llame a la función [WrapCompressedRTFStream](wrapcompressedrtfstream.md) para crear una versión sin comprimir de los datos RTF comprimidos, si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="1c030-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="1c030-117">Mostrar los datos RTF sin comprimir o los datos de texto sin formato al usuario.</span><span class="sxs-lookup"><span data-stu-id="1c030-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="1c030-118">**RTFSync** devuelve un valor booleano que indica si el mensaje se ha actualizado o no.</span><span class="sxs-lookup"><span data-stu-id="1c030-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="1c030-119">Si este valor devuelve TRUE, llame a **SaveChanges** en algún momento para que la actualización sea permanente.</span><span class="sxs-lookup"><span data-stu-id="1c030-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="1c030-120">La llamada no tiene que realizarse inmediatamente después de **RTFSync** devuelve.</span><span class="sxs-lookup"><span data-stu-id="1c030-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1c030-121">Debido a que muchos componentes manejan el texto con formato antes de recibirlo, existe la posibilidad de que se dañen.</span><span class="sxs-lookup"><span data-stu-id="1c030-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="1c030-122">Este daño puede provenir del proveedor de almacenamiento de mensajes, una aplicación de terceros, una puerta de enlace o un error de transmisión.</span><span class="sxs-lookup"><span data-stu-id="1c030-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

