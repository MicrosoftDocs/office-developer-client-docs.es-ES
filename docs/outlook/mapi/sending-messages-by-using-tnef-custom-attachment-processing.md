---
title: Enviar mensajes a través del procesamiento de datos adjuntos personalizado TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 0c7cdf754b2a4b38516b1ac06074fdba9d2227f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577747"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="ccad3-103">Enviar mensajes a través del procesamiento de datos adjuntos personalizado TNEF</span><span class="sxs-lookup"><span data-stu-id="ccad3-103">Sending Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="ccad3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccad3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccad3-105">Para personalizar el procesamiento de datos adjuntos al enviar un mensaje:</span><span class="sxs-lookup"><span data-stu-id="ccad3-105">To customize attachment processing when sending a message:</span></span>
  
1. <span data-ttu-id="ccad3-106">Obtener un objeto TNEF pasando una interfaz **IStream** y un mensaje en la función [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="ccad3-106">Obtain a TNEF object by passing an **IStream** interface and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="ccad3-107">Para obtener una lista de todas las propiedades definidas para el mensaje llamando al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="ccad3-107">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="ccad3-108">Utilizar los métodos [IMAPIProp](imapipropiunknown.md) para excluir todas las propiedades compatibles con el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ccad3-108">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="ccad3-109">En un momento adecuado escribir esas propiedades en el sistema de mensajería en el formato requerido por el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ccad3-109">At an appropriate time write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="ccad3-110">Llame al método [ITnef::AddProps](itnef-addprops.md) para agregar sólo las propiedades en el mensaje, es decir, ninguna de las propiedades en los datos adjuntos: estableciendo el indicador TNEF_PROP_MESSAGE_ONLY.</span><span class="sxs-lookup"><span data-stu-id="ccad3-110">Call the [ITnef::AddProps](itnef-addprops.md) method to add only the properties on the message — that is, none of the properties on the attachments — by setting the TNEF_PROP_MESSAGE_ONLY flag.</span></span> 
    
5. <span data-ttu-id="ccad3-111">Llame al método [ITnef::AddProps](itnef-addprops.md) con estos elementos: la marca TNEF_PROP_EXCLUDE, una matriz de etiqueta de propiedad que contiene el **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) o **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) propiedad y un identificador de datos adjuntos que especifica los datos adjuntos que va a procesar.</span><span class="sxs-lookup"><span data-stu-id="ccad3-111">Call [ITnef::AddProps](itnef-addprops.md) with these items: the TNEF_PROP_EXCLUDE flag, a property tag array that contains the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property, and an attachment identifier that specifies the attachment to be processed.</span></span>
    
6. <span data-ttu-id="ccad3-112">Use el método [ITnef::SetProps](itnef-setprops.md) para agregar la etiqueta de propiedad de **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) con una cadena única que identifica el sistema de mensajería de los datos adjuntos, si los datos adjuntos tienen un nombre de archivo que el no se admite el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ccad3-112">Use the [ITnef::SetProps](itnef-setprops.md) method to add the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property tag with a unique string that identifies the attachment to the messaging system if the attachment has a filename that the messaging system cannot support.</span></span> <span data-ttu-id="ccad3-113">Por ejemplo, varios datos adjuntos con el mismo nombre de archivo original, o un nombre de archivo que no es un nombre de archivo válido para el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ccad3-113">For example, multiple attachments with the same original filename, or a filename that is not a valid filename for the messaging system.</span></span> <span data-ttu-id="ccad3-114">Esta cadena se utilizará junto con un número clave al escribir las etiquetas de datos adjuntos en el texto del mensaje con etiqueta para asociar un archivo adjunto a sus datos.</span><span class="sxs-lookup"><span data-stu-id="ccad3-114">This string will be used with a key number when writing the attachment tags in the tagged message text to associate an attachment with its data.</span></span> <span data-ttu-id="ccad3-115">Para obtener más información, vea [TNEF-Tagged texto del mensaje](tnef-tagged-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="ccad3-115">For more information, see, [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span></span>
    
7. <span data-ttu-id="ccad3-116">Repita las llamadas **AddProps** y **SetProps** por cada dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="ccad3-116">Repeat the **AddProps** and **SetProps** calls for each attachment.</span></span> 
    
8. <span data-ttu-id="ccad3-117">Llame al método [ITnef::Finish](itnef-finish.md) para codificar el mensaje en la secuencia TNEF después de que se agregan todas las propiedades solicitadas.</span><span class="sxs-lookup"><span data-stu-id="ccad3-117">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
9. <span data-ttu-id="ccad3-118">Obtener el texto del mensaje con etiqueta llamando al método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) .</span><span class="sxs-lookup"><span data-stu-id="ccad3-118">Obtain the tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="ccad3-119">Este texto etiquetado es de lectura con los métodos de la interfaz **IStream** , codifican mediante el modelo de datos adjuntos del sistema de mensajería y se escriben en el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ccad3-119">This tagged text is read using methods from the **IStream** interface, encoded using the messaging system's attachment model, and written out to the messaging system.</span></span> 
    
10. <span data-ttu-id="ccad3-120">Llame al método [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar el objeto [ITnef](itnefiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="ccad3-120">Call the [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to release the [ITnef](itnefiunknown.md) object.</span></span> 
    
11. <span data-ttu-id="ccad3-121">Escribir los datos adjuntos restante para el sistema de mensajería a través del modelo de datos adjuntos del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ccad3-121">Write the remaining attachments to the messaging system through the messaging system's attachment model.</span></span>
    
<span data-ttu-id="ccad3-122">El proveedor de transporte debe utilizar el procedimiento descrito anteriormente para los datos adjuntos de proceso.</span><span class="sxs-lookup"><span data-stu-id="ccad3-122">Your transport provider should use the previously described procedure to process attachments.</span></span> <span data-ttu-id="ccad3-123">Si eso no es posible, el proveedor de transporte debe usar los siguientes pasos para el procesamiento de datos adjuntos personalizado:</span><span class="sxs-lookup"><span data-stu-id="ccad3-123">If that is not possible, the transport provider should use the following steps for customized attachment processing:</span></span>
  
1. <span data-ttu-id="ccad3-124">El proveedor de transporte se asegura de que las propiedades **PR_ATTACH_TRANSPORT_NAME** de todos los datos adjuntos contienen valores únicos que son identificadores de conexión válida para el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ccad3-124">The transport provider ensures that the **PR_ATTACH_TRANSPORT_NAME** properties of all the attachments contain unique values that are valid attachment identifiers for the messaging system.</span></span> 
    
2. <span data-ttu-id="ccad3-125">El proveedor de transporte, a continuación, usa una sola llamada a **ITnef::AddProps** por cada dato adjunto, pasando el indicador TNEF_PROP_CONTAINED.</span><span class="sxs-lookup"><span data-stu-id="ccad3-125">The transport provider then uses a single call to **ITnef::AddProps** for each attachment, passing in the TNEF_PROP_CONTAINED flag.</span></span> 
    

