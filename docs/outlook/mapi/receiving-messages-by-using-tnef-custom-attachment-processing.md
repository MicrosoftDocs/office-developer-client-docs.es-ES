---
title: Recibir mensajes a través del procesamiento de datos adjuntos personalizado TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 67c202e5130bd35e1277c5260bc1702043eadd95
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588030"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="f9c65-103">Recibir mensajes a través del procesamiento de datos adjuntos personalizado TNEF</span><span class="sxs-lookup"><span data-stu-id="f9c65-103">Receiving Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="f9c65-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9c65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9c65-105">Para recibir un mensaje TNEF con procesamiento de datos adjuntos personalizado:</span><span class="sxs-lookup"><span data-stu-id="f9c65-105">To receive a TNEF message with customized attachment processing:</span></span>
  
1. <span data-ttu-id="f9c65-106">Importar todas las propiedades transmisible: aquellos que admite el sistema de mensajería, desde el mensaje entrante en un nuevo mensaje de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f9c65-106">Import all the transmittable properties — those that the messaging system supports — from the incoming message into a new MAPI message.</span></span> <span data-ttu-id="f9c65-107">Esto incluye el texto del mensaje, que contiene la secuencia de datos TNEF.</span><span class="sxs-lookup"><span data-stu-id="f9c65-107">This includes the message text, which contains the TNEF data stream.</span></span>
    
2. <span data-ttu-id="f9c65-108">Identificar y descodificar los datos adjuntos especial que contiene la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="f9c65-108">Identify and decode the special attachment that contains the TNEF stream.</span></span>
    
3. <span data-ttu-id="f9c65-109">Extraiga todos los datos adjuntos del mensaje entrante en datos adjuntos de MAPI en el nuevo mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="f9c65-109">Extract all the attachments from the incoming message into MAPI attachments on the new MAPI message.</span></span> <span data-ttu-id="f9c65-110">Los nombres de archivo recuperado, u otros marcadores de identificación en los datos adjuntos, deben colocarse en la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) de los nuevos datos adjuntos por lo que el método [ITnef::ExtractProps](itnef-extractprops.md) más adelante se puede asociar los datos adjuntos correcto con las etiquetas de datos adjuntos codificadas en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f9c65-110">The recovered filenames, or other identifying markers on the attachments, should be placed into the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property of the new attachments so that the [ITnef::ExtractProps](itnef-extractprops.md) method can later associate the correct attachment with the attachment tags encoded in the message text.</span></span> 
    
4. <span data-ttu-id="f9c65-111">Crear una interfaz **IStream** OLE para ajuste alrededor de la secuencia TNEF descodificada y usar ese objeto junto con el nuevo mensaje MAPI en una llamada a la función [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="f9c65-111">Create an OLE **IStream** interface to wrap around the decoded TNEF stream and use that object along with the new MAPI message in a call to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="f9c65-112">Llame al método **ITnef::ExtractProps** para recuperar las propiedades de nontransmittable en el mensaje de la secuencia de datos TNEF.</span><span class="sxs-lookup"><span data-stu-id="f9c65-112">Call the **ITnef::ExtractProps** method to recover the nontransmittable properties on the message from the TNEF data stream.</span></span> 
    
6. <span data-ttu-id="f9c65-113">Llame al método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) con el conjunto de indicadores MAPI_CREATE y MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="f9c65-113">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method with the MAPI_CREATE and MAPI_MODIFY flags set.</span></span> <span data-ttu-id="f9c65-114">Esta llamada quita las etiquetas de datos adjuntos desde el texto del mensaje y los convierte en información de posición de datos adjuntos en el mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="f9c65-114">This call removes the attachment tags from the message text and converts them into attachment position information in the MAPI message.</span></span> 
    
7. <span data-ttu-id="f9c65-115">Entregar el mensaje a través de la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f9c65-115">Deliver the message through the MAPI spooler.</span></span>
    

