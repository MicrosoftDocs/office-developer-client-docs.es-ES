---
title: Recibir mensajes mediante el procesamiento de datos adJuntos personalizado TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 046b537d41b318fa857ef77f1906edcf2c3aa2bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429323"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="c60e8-103">Recibir mensajes mediante el procesamiento de datos adJuntos personalizado TNEF</span><span class="sxs-lookup"><span data-stu-id="c60e8-103">Receiving Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="c60e8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c60e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c60e8-105">Para recibir un mensaje TNEF con procesamiento de datos adjuntos personalizado:</span><span class="sxs-lookup"><span data-stu-id="c60e8-105">To receive a TNEF message with customized attachment processing:</span></span>
  
1. <span data-ttu-id="c60e8-106">Importe todas las propiedades transmitibles (las que admite el sistema de mensajería) desde el mensaje entrante a un nuevo mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="c60e8-106">Import all the transmittable properties — those that the messaging system supports — from the incoming message into a new MAPI message.</span></span> <span data-ttu-id="c60e8-107">Esto incluye el texto del mensaje, que contiene la secuencia de datos TNEF.</span><span class="sxs-lookup"><span data-stu-id="c60e8-107">This includes the message text, which contains the TNEF data stream.</span></span>
    
2. <span data-ttu-id="c60e8-108">Identificar y descodificar los datos adjuntos especiales que contienen la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="c60e8-108">Identify and decode the special attachment that contains the TNEF stream.</span></span>
    
3. <span data-ttu-id="c60e8-109">Extraiga todos los datos adjuntos del mensaje entrante en datos adjuntos MAPI del nuevo mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="c60e8-109">Extract all the attachments from the incoming message into MAPI attachments on the new MAPI message.</span></span> <span data-ttu-id="c60e8-110">Los nombres de archivo recuperados u otros marcadores de identificación de los datos adjuntos, se deben colocar en la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) de los nuevos datos adjuntos para que el método [ITnef:: ExtractProps](itnef-extractprops.md) más adelante puede asociar los datos adjuntos correctos con las etiquetas de datos adjuntos codificadas en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c60e8-110">The recovered filenames, or other identifying markers on the attachments, should be placed into the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property of the new attachments so that the [ITnef::ExtractProps](itnef-extractprops.md) method can later associate the correct attachment with the attachment tags encoded in the message text.</span></span> 
    
4. <span data-ttu-id="c60e8-111">Cree una interfaz OLE **IStream** para ajustar la secuencia TNEF descodificada y use ese objeto junto con el nuevo mensaje MAPI en una llamada a la función [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="c60e8-111">Create an OLE **IStream** interface to wrap around the decoded TNEF stream and use that object along with the new MAPI message in a call to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="c60e8-112">Llame al método **ITnef:: ExtractProps** para recuperar las propiedades no transmitibles del mensaje desde la secuencia de datos TNEF.</span><span class="sxs-lookup"><span data-stu-id="c60e8-112">Call the **ITnef::ExtractProps** method to recover the nontransmittable properties on the message from the TNEF data stream.</span></span> 
    
6. <span data-ttu-id="c60e8-113">Llame al método [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) con los marcadores MAPI_CREATE y MAPI_MODIFY establecidos.</span><span class="sxs-lookup"><span data-stu-id="c60e8-113">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method with the MAPI_CREATE and MAPI_MODIFY flags set.</span></span> <span data-ttu-id="c60e8-114">Esta llamada quita las etiquetas de datos adjuntos del texto del mensaje y las convierte en información de la posición de los datos adjuntos en el mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="c60e8-114">This call removes the attachment tags from the message text and converts them into attachment position information in the MAPI message.</span></span> 
    
7. <span data-ttu-id="c60e8-115">Entrega el mensaje a través de la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="c60e8-115">Deliver the message through the MAPI spooler.</span></span>
    

