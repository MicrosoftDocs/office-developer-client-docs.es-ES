---
title: Compatibilidad con texto con formato en responsabilidades de cliente de los mensajes entrantes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 863c95856f3198c74bb9d72881154676386f6a9f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19820800"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="9319a-103">Admitir texto con formato en los mensajes entrantes: responsabilidades del cliente</span><span class="sxs-lookup"><span data-stu-id="9319a-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="9319a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9319a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9319a-105">Como los mensajes se transfieren entre los sistemas de mensajería, la cola MAPI se asegura de que el formato de texto enriquecido permanece sincronizado con el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9319a-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="9319a-106">La cola MAPI llama a la función de [RTFSync](rtfsync.md) desde dentro de una versión del mensaje que se pasa al proveedor de transporte ajustada.</span><span class="sxs-lookup"><span data-stu-id="9319a-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="9319a-107">El proveedor de transporte guarda los cambios realizados en el mensaje llamando al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y, a continuación, enruta al destinatario nuevo.</span><span class="sxs-lookup"><span data-stu-id="9319a-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="9319a-108">Cuando la aplicación de cliente compatible con RTF del destinatario abre el mensaje para mostrar el texto, debe sincronizar el texto con el formato y abra **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , dependiendo de qué propiedad está disponible.</span><span class="sxs-lookup"><span data-stu-id="9319a-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="9319a-109">**Para abrir un mensaje, los clientes de tener en cuenta RTF**</span><span class="sxs-lookup"><span data-stu-id="9319a-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="9319a-110">Llame a **RTFSync** para sincronizar el texto del mensaje con el formato si el almacén de mensajes no es compatible con RTF.</span><span class="sxs-lookup"><span data-stu-id="9319a-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="9319a-111">El indicador RTF_SYNC_BODY_CHANGED debe pasarse en el parámetro _ulFlags_ si la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) falta o se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="9319a-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="9319a-112">Trabajar con almacenes de mensaje RTF compatibles de los clientes no necesitan realizar la llamada **RTFSync** debido a que el almacén de mensajes se ocupa de ella.</span><span class="sxs-lookup"><span data-stu-id="9319a-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="9319a-113">Llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) si se ha actualizado el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9319a-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="9319a-114">Llame a [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="9319a-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="9319a-115">Si **PR_RTF_COMPRESSED** no está disponible, debe abrir en su lugar la propiedad **PR_BODY** para mostrar el contenido del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9319a-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="9319a-116">Llame a la función [WrapCompressedRTFStream](wrapcompressedrtfstream.md) para crear una versión sin comprimir de los datos RTF comprimidos, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="9319a-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="9319a-117">Mostrar los datos RTF sin comprimir o los datos de texto sin formato para el usuario.</span><span class="sxs-lookup"><span data-stu-id="9319a-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="9319a-118">**RTFSync** devuelve un valor booleano que indica si se ha actualizado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9319a-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="9319a-119">Si este valor devuelve el valor TRUE, llame a **SaveChanges** en algún momento para realizar la actualización permanente.</span><span class="sxs-lookup"><span data-stu-id="9319a-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="9319a-120">La llamada no tiene que estar inmediatamente después de que devuelve **RTFSync** .</span><span class="sxs-lookup"><span data-stu-id="9319a-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9319a-121">Debido a que tantos componentes controlan el texto con formato antes de recibirla, hay la posibilidad de daños.</span><span class="sxs-lookup"><span data-stu-id="9319a-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="9319a-122">Este daño podría procedentes del proveedor de almacenamiento de mensajes, una aplicación de terceros, una puerta de enlace o un error de transmisión.</span><span class="sxs-lookup"><span data-stu-id="9319a-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

