---
title: Procesamiento TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: 066ad3dfb64161e326b92fef7774d5b3b9461d8a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339602"
---
# <a name="tnef-processing"></a><span data-ttu-id="5a32b-103">Procesamiento TNEF</span><span class="sxs-lookup"><span data-stu-id="5a32b-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="5a32b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a32b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a32b-105">En la siguiente serie de acciones se describe cómo los transportes usan métodos TNEF para procesar mensajes salientes y entrantes.</span><span class="sxs-lookup"><span data-stu-id="5a32b-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="5a32b-106">**Para enviar un mensaje que incluya una secuencia TNEF**</span><span class="sxs-lookup"><span data-stu-id="5a32b-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="5a32b-107">Procese las propiedades de mensaje admitidas por el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="5a32b-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="5a32b-108">Marque el mensaje de forma específica de implementación para que el proveedor de transporte de recepción pueda determinar que el mensaje requiere el procesamiento de TNEF.</span><span class="sxs-lookup"><span data-stu-id="5a32b-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="5a32b-109">Por ejemplo, un proveedor de transporte TNEF que envía a un sistema de mensajería SMTP puede agregar un campo de encabezado personalizado como "X-CONTAINS-TNEF" para indicar que el mensaje contiene datos TNEF.</span><span class="sxs-lookup"><span data-stu-id="5a32b-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="5a32b-110">Obtenga un objeto TNEF y úselo para encapsular las propiedades de mensaje no admitidas por el sistema de mensajería en una secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="5a32b-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="5a32b-111">Codifica la secuencia TNEF con el modelo de datos adjuntos del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="5a32b-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="5a32b-112">Por ejemplo, si el modelo de datos adjuntos subyacente es uuencode los datos adjuntos y anexarlos al texto del mensaje, el proveedor de transporte debe uuencodificar la secuencia TNEF en otro archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="5a32b-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="5a32b-113">El proveedor de transporte también debe implementar un método para reconocer qué datos adjuntos contiene la secuencia TNEF codificada cuando recibe un mensaje.</span><span class="sxs-lookup"><span data-stu-id="5a32b-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="5a32b-114">La forma estándar de marcar estos datos adjuntos es darle un nombre de archivo adjunto de "WINMAIL. DAT".</span><span class="sxs-lookup"><span data-stu-id="5a32b-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="5a32b-115">Si el proveedor de transporte hace esto, cualquier otro proveedor de transporte habilitado para TNEF que siga esta convención podrá interoperar con ella.</span><span class="sxs-lookup"><span data-stu-id="5a32b-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="5a32b-116">Use métodos de interfaz [ITnef : IUnknown](itnefiunknown.md) para insertar etiquetas que describan las posiciones de los datos adjuntos del mensaje en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="5a32b-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="5a32b-117">Obtenga acceso al texto del mensaje etiquetado a través de los métodos [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) y envíelo al sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="5a32b-117">Access the tagged message text through [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="5a32b-118">**Para recuperar propiedades encapsuladas**</span><span class="sxs-lookup"><span data-stu-id="5a32b-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="5a32b-119">Escriba las propiedades admitidas por el sistema de mensajería en un nuevo mensaje, incluido el texto del mensaje etiquetado que contiene las propiedades encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="5a32b-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="5a32b-120">Descodificar la secuencia TNEF desde los datos adjuntos adecuados.</span><span class="sxs-lookup"><span data-stu-id="5a32b-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="5a32b-121">Descodifica cualquier otro archivo adjunto y escríbalos en nuevos datos adjuntos MAPI en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="5a32b-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="5a32b-122">Abra la secuencia TNEF para la decodificación mediante la [función OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="5a32b-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="5a32b-123">Use el [método ITnef::ExtractProps](itnef-extractprops.md) para descodificar la secuencia TNEF y escribir las propiedades encapsuladas en el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="5a32b-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="5a32b-124">Las propiedades codificadas que sean duplicados de propiedades no codificadas sobrescribirán las propiedades no codificadas cuando se descodifican las propiedades codificadas.</span><span class="sxs-lookup"><span data-stu-id="5a32b-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="5a32b-125">Use el [método ITnef::OpenTaggedBody](itnef-opentaggedbody.md) para analizar el texto del mensaje para recuperar las posiciones de datos adjuntos de las etiquetas del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="5a32b-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

