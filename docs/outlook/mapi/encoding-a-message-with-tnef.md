---
title: Codificación de un mensaje con TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2cb5c9a971f95e309f0a91cf477eefe98fe3bd64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816777"
---
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="a88be-103">Codificación de un mensaje con TNEF</span><span class="sxs-lookup"><span data-stu-id="a88be-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="a88be-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a88be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a88be-105">Cuando se envía un mensaje, el proveedor de transporte puede crear un archivo que se utiliza para contener el mensaje durante la transmisión.</span><span class="sxs-lookup"><span data-stu-id="a88be-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="a88be-106">A continuación, se ajusta una interfaz [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) alrededor del archivo.</span><span class="sxs-lookup"><span data-stu-id="a88be-106">Next, an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="a88be-107">El proveedor de transporte, a continuación, usa métodos [ITnef](itnefiunknown.md) para escribir las propiedades del mensaje en la secuencia en un formato con etiqueta que permite que las propiedades que desea descodificar fácilmente por los proveedores de transporte receptora.</span><span class="sxs-lookup"><span data-stu-id="a88be-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="a88be-108">**Para representar un mensaje completo en un solo archivo**</span><span class="sxs-lookup"><span data-stu-id="a88be-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="a88be-109">Obtener un objeto TNEF pasando un objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) y un mensaje en la función [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="a88be-109">Obtain a TNEF object by passing an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="a88be-110">Para obtener una lista de todas las propiedades definidas para el mensaje llamando al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="a88be-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="a88be-111">Utilizar los métodos [IMAPIProp](imapipropiunknown.md) para excluir todas las propiedades compatibles con el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="a88be-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="a88be-112">En un momento adecuado, escribir esas propiedades en el sistema de mensajería en el formato requerido por el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="a88be-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="a88be-113">Llame a [ITnef::AddProps](itnef-addprops.md) para codificar las propiedades restantes, incluidos todos los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a88be-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="a88be-114">Llame al método [ITnef::Finish](itnef-finish.md) para codificar el mensaje en la secuencia TNEF después de que se agregan todas las propiedades solicitadas.</span><span class="sxs-lookup"><span data-stu-id="a88be-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="a88be-115">Llame al método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) para obtener el texto del mensaje con etiqueta.</span><span class="sxs-lookup"><span data-stu-id="a88be-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="a88be-116">Este texto etiquetado se escribe en el sistema de mensajería con los métodos de la interfaz [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) OLE.</span><span class="sxs-lookup"><span data-stu-id="a88be-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="a88be-117">Llame al método [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) para liberar el objeto **ITnef** .</span><span class="sxs-lookup"><span data-stu-id="a88be-117">Call the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="a88be-118">**Para procesar un mensaje TNEF entrante**</span><span class="sxs-lookup"><span data-stu-id="a88be-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="a88be-119">Obtener un objeto de mensaje MAPI desde la cola MAPI y escribir las propiedades de encabezado de mensaje en el nuevo mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="a88be-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="a88be-120">Crear e inicializar un objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) para incluir los datos TNEF desde el mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="a88be-120">Create and initialize an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="a88be-121">Pase el mensaje MAPI y el objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) a la función [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="a88be-121">Pass the MAPI message and the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="a88be-122">Descodificar la información de los datos TNEF llamando al método [ITnef::ExtractProps](itnef-extractprops.md) .</span><span class="sxs-lookup"><span data-stu-id="a88be-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="a88be-123">Cualquier cosa descodificar **ExtractProps** sobrescribirá propiedades descodificadas de sobre del mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="a88be-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="a88be-124">Es decir, las propiedades TNEF extraídas sobrescribirán las propiedades existentes en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a88be-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="a88be-125">Procesar el texto del mensaje con etiqueta llamando a [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) y analizar el texto para recuperar las posiciones de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a88be-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="a88be-126">Guarde el mensaje mediante una llamada a [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="a88be-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="a88be-127">Liberar el objeto TNEF llamando al método [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a88be-127">Release the TNEF object by calling the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

