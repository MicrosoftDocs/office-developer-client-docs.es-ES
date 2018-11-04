---
title: Procesamiento de TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: 'Última modificación: 05 de julio de 2012'
ms.openlocfilehash: 066ad3dfb64161e326b92fef7774d5b3b9461d8a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399573"
---
# <a name="tnef-processing"></a><span data-ttu-id="c3451-103">Procesamiento de TNEF</span><span class="sxs-lookup"><span data-stu-id="c3451-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="c3451-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3451-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3451-105">La siguiente serie de acciones describe cómo usar los transportes los métodos TNEF para procesar los mensajes entrantes y salientes.</span><span class="sxs-lookup"><span data-stu-id="c3451-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="c3451-106">**Para enviar un mensaje que incluye una secuencia TNEF**</span><span class="sxs-lookup"><span data-stu-id="c3451-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="c3451-107">Proceso de las propiedades del mensaje que son compatibles con el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="c3451-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="c3451-108">Marcar el mensaje en una implementación específica manera para que el proveedor de transporte receptora puede determinar que el mensaje requiere procesamiento de TNEF.</span><span class="sxs-lookup"><span data-stu-id="c3451-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="c3451-109">Por ejemplo, un proveedor de transporte TNEF envío a un sistema de mensajería SMTP puede agregar un campo de encabezado personalizado como "X-contiene-TNEF" para indicar que el mensaje contiene datos TNEF.</span><span class="sxs-lookup"><span data-stu-id="c3451-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="c3451-110">Obtener un objeto TNEF y usarlo para encapsular las propiedades de mensaje no compatibles con el sistema de mensajería en una secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="c3451-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="c3451-111">Codificar la secuencia TNEF mediante el modelo de datos adjuntos del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="c3451-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="c3451-112">Por ejemplo, si el modelo de datos adjuntos subyacente consiste en datos adjuntos uuencode y agregarlos al texto del mensaje, el proveedor de transporte debe uuencode la secuencia TNEF en otro objeto attachment.</span><span class="sxs-lookup"><span data-stu-id="c3451-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="c3451-113">El proveedor de transporte también debe implementar un método para reconocer qué datos adjuntos contienen la secuencia TNEF codificada cuando recibe un mensaje.</span><span class="sxs-lookup"><span data-stu-id="c3451-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="c3451-114">La forma estándar para marcar estos datos adjuntos es asignarle un nombre de archivo de datos adjuntos de "WINMAIL. RÁPIDO".</span><span class="sxs-lookup"><span data-stu-id="c3451-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="c3451-115">Si su proveedor de transporte para ello, otros proveedores de transporte TNEF habilitado que siguen esta convención podrán interoperar con él.</span><span class="sxs-lookup"><span data-stu-id="c3451-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="c3451-116">Uso [ITnef: IUnknown](itnefiunknown.md) métodos para insertar etiquetas que describe las posiciones de los datos adjuntos del mensaje en el texto del mensaje de interfaz.</span><span class="sxs-lookup"><span data-stu-id="c3451-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="c3451-117">Obtener acceso el texto del mensaje con etiqueta a través de métodos de [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) y enviarlo al sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="c3451-117">Access the tagged message text through [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="c3451-118">**Para recuperar propiedades encapsuladas**</span><span class="sxs-lookup"><span data-stu-id="c3451-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="c3451-119">Escribir las propiedades compatibles con el sistema de mensajería en un mensaje nuevo, incluido el texto del mensaje con etiqueta que contiene las propiedades de encapsulado.</span><span class="sxs-lookup"><span data-stu-id="c3451-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="c3451-120">Descodificar la secuencia TNEF de los datos adjuntos adecuados.</span><span class="sxs-lookup"><span data-stu-id="c3451-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="c3451-121">Descodificar cualquier otros datos adjuntos y escribir nuevos datos adjuntos de MAPI en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="c3451-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="c3451-122">Abra la secuencia TNEF para descodificar el uso de la función [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="c3451-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="c3451-123">Utilice el método [ITnef::ExtractProps](itnef-extractprops.md) para descodificar la secuencia TNEF y escribir las propiedades encapsuladas en el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="c3451-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="c3451-124">Las propiedades codificadas que son duplicados de las propiedades nonencoded sobrescribirán las propiedades nonencoded cuando se descodificación las propiedades codificadas.</span><span class="sxs-lookup"><span data-stu-id="c3451-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="c3451-125">Use el método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) para analizar el texto del mensaje para recuperar las posiciones de los datos adjuntos de las etiquetas en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c3451-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

