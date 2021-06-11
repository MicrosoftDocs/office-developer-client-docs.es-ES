---
title: Envío de mensajes mediante el procesamiento de datos adjuntos personalizados de TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339700"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="4410c-103">Envío de mensajes mediante el procesamiento de datos adjuntos personalizados de TNEF</span><span class="sxs-lookup"><span data-stu-id="4410c-103">Sending Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="4410c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4410c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4410c-105">Para personalizar el procesamiento de datos adjuntos al enviar un mensaje:</span><span class="sxs-lookup"><span data-stu-id="4410c-105">To customize attachment processing when sending a message:</span></span>
  
1. <span data-ttu-id="4410c-106">Para obtener un objeto TNEF, pase una **interfaz IStream** y un mensaje a la [función OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="4410c-106">Obtain a TNEF object by passing an **IStream** interface and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="4410c-107">Para obtener una lista de todas las propiedades definidas para el mensaje, llame al [método IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="4410c-107">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="4410c-108">Use [métodos IMAPIProp](imapipropiunknown.md) para excluir todas las propiedades admitidas por el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4410c-108">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="4410c-109">En el momento adecuado, escriba esas propiedades en el sistema de mensajería en el formato requerido por el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4410c-109">At an appropriate time write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="4410c-110">Llama al [método ITnef::AddProps](itnef-addprops.md) para agregar solo las propiedades del mensaje( es decir, ninguna de las propiedades de los datos adjuntos) estableciendo la marca TNEF_PROP_MESSAGE_ONLY.</span><span class="sxs-lookup"><span data-stu-id="4410c-110">Call the [ITnef::AddProps](itnef-addprops.md) method to add only the properties on the message — that is, none of the properties on the attachments — by setting the TNEF_PROP_MESSAGE_ONLY flag.</span></span> 
    
5. <span data-ttu-id="4410c-111">Llama a [ITnef::AddProps](itnef-addprops.md) con estos elementos: la marca TNEF_PROP_EXCLUDE, una matriz de etiquetas de propiedad que contiene la propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) o **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) y un identificador de datos adjuntos que especifica los datos adjuntos que se deben procesar.</span><span class="sxs-lookup"><span data-stu-id="4410c-111">Call [ITnef::AddProps](itnef-addprops.md) with these items: the TNEF_PROP_EXCLUDE flag, a property tag array that contains the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property, and an attachment identifier that specifies the attachment to be processed.</span></span>
    
6. <span data-ttu-id="4410c-112">Use el método [ITnef::SetProps](itnef-setprops.md) para agregar la etiqueta de propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) con una cadena única que identifique los datos adjuntos al sistema de mensajería si los datos adjuntos tienen un nombre de archivo que el sistema de mensajería no puede admitir.</span><span class="sxs-lookup"><span data-stu-id="4410c-112">Use the [ITnef::SetProps](itnef-setprops.md) method to add the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property tag with a unique string that identifies the attachment to the messaging system if the attachment has a filename that the messaging system cannot support.</span></span> <span data-ttu-id="4410c-113">Por ejemplo, varios datos adjuntos con el mismo nombre de archivo original o un nombre de archivo que no es un nombre de archivo válido para el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4410c-113">For example, multiple attachments with the same original filename, or a filename that is not a valid filename for the messaging system.</span></span> <span data-ttu-id="4410c-114">Esta cadena se usará con un número de clave al escribir las etiquetas de datos adjuntos en el texto del mensaje etiquetado para asociar un dato adjunto con sus datos.</span><span class="sxs-lookup"><span data-stu-id="4410c-114">This string will be used with a key number when writing the attachment tags in the tagged message text to associate an attachment with its data.</span></span> <span data-ttu-id="4410c-115">Para obtener más información, vea Texto del mensaje etiquetado [por TNEF](tnef-tagged-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="4410c-115">For more information, see, [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span></span>
    
7. <span data-ttu-id="4410c-116">Repita las **llamadas AddProps** **y SetProps** para cada dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="4410c-116">Repeat the **AddProps** and **SetProps** calls for each attachment.</span></span> 
    
8. <span data-ttu-id="4410c-117">Llame al [método ITnef::Finish](itnef-finish.md) para codificar el mensaje en la secuencia TNEF después de agregar todas las propiedades solicitadas.</span><span class="sxs-lookup"><span data-stu-id="4410c-117">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
9. <span data-ttu-id="4410c-118">Obtenga el texto del mensaje etiquetado llamando al [método ITnef::OpenTaggedBody.](itnef-opentaggedbody.md)</span><span class="sxs-lookup"><span data-stu-id="4410c-118">Obtain the tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="4410c-119">Este texto etiquetado se lee mediante métodos de la **interfaz IStream,** se codifica mediante el modelo de datos adjuntos del sistema de mensajería y se escribe en el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4410c-119">This tagged text is read using methods from the **IStream** interface, encoded using the messaging system's attachment model, and written out to the messaging system.</span></span> 
    
10. <span data-ttu-id="4410c-120">Llame al [método IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar el [objeto ITnef.](itnefiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="4410c-120">Call the [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to release the [ITnef](itnefiunknown.md) object.</span></span> 
    
11. <span data-ttu-id="4410c-121">Escriba los datos adjuntos restantes en el sistema de mensajería a través del modelo de datos adjuntos del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4410c-121">Write the remaining attachments to the messaging system through the messaging system's attachment model.</span></span>
    
<span data-ttu-id="4410c-122">El proveedor de transporte debe usar el procedimiento descrito anteriormente para procesar datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4410c-122">Your transport provider should use the previously described procedure to process attachments.</span></span> <span data-ttu-id="4410c-123">Si no es posible, el proveedor de transporte debe seguir los siguientes pasos para el procesamiento de datos adjuntos personalizados:</span><span class="sxs-lookup"><span data-stu-id="4410c-123">If that is not possible, the transport provider should use the following steps for customized attachment processing:</span></span>
  
1. <span data-ttu-id="4410c-124">El proveedor de transporte  garantiza que las PR_ATTACH_TRANSPORT_NAME de todos los datos adjuntos contienen valores únicos que son identificadores de datos adjuntos válidos para el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4410c-124">The transport provider ensures that the **PR_ATTACH_TRANSPORT_NAME** properties of all the attachments contain unique values that are valid attachment identifiers for the messaging system.</span></span> 
    
2. <span data-ttu-id="4410c-125">A continuación, el proveedor de transporte usa una sola llamada a **ITnef::AddProps** para cada dato adjunto, pasando la marca TNEF_PROP_CONTAINED usuario.</span><span class="sxs-lookup"><span data-stu-id="4410c-125">The transport provider then uses a single call to **ITnef::AddProps** for each attachment, passing in the TNEF_PROP_CONTAINED flag.</span></span> 
    

