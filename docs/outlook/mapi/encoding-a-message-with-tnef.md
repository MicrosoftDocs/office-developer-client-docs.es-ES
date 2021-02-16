---
title: Codificar un mensaje con TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336704"
---
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="fa5ad-103">Codificar un mensaje con TNEF</span><span class="sxs-lookup"><span data-stu-id="fa5ad-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="fa5ad-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa5ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa5ad-105">Cuando se envía un mensaje, el proveedor de transporte puede crear un archivo que se usa para contener el mensaje durante la transmisión.</span><span class="sxs-lookup"><span data-stu-id="fa5ad-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="fa5ad-106">A continuación, se ajusta una interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) alrededor del archivo.</span><span class="sxs-lookup"><span data-stu-id="fa5ad-106">Next, an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="fa5ad-107">A continuación, el proveedor de transporte usa métodos [ITnef](itnefiunknown.md) para escribir las propiedades del mensaje en la secuencia en un formato etiquetado que permite que los proveedores de transporte receptores puedan descodificar fácilmente las propiedades.</span><span class="sxs-lookup"><span data-stu-id="fa5ad-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="fa5ad-108">**Para representar un mensaje completo en un solo archivo**</span><span class="sxs-lookup"><span data-stu-id="fa5ad-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="fa5ad-109">Para obtener un objeto TNEF, pasa un [objeto IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) y un mensaje a la [función OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="fa5ad-109">Obtain a TNEF object by passing an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="fa5ad-110">Obtenga una lista de todas las propiedades definidas para el mensaje llamando al [método IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="fa5ad-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="fa5ad-111">Use [métodos IMAPIProp](imapipropiunknown.md) para excluir todas las propiedades admitidas por el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="fa5ad-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="fa5ad-112">En el momento adecuado, escriba esas propiedades en el sistema de mensajería en el formato requerido por el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="fa5ad-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="fa5ad-113">Llame [a ITnef::AddProps](itnef-addprops.md) para codificar las propiedades restantes, incluidos todos los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="fa5ad-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="fa5ad-114">Llame al [método ITnef::Finish](itnef-finish.md) para codificar el mensaje en la secuencia TNEF después de agregar todas las propiedades solicitadas.</span><span class="sxs-lookup"><span data-stu-id="fa5ad-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="fa5ad-115">Llame al [método ITnef::OpenTaggedBody](itnef-opentaggedbody.md) para obtener el texto del mensaje etiquetado.</span><span class="sxs-lookup"><span data-stu-id="fa5ad-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="fa5ad-116">Este texto etiquetado se escribe en el sistema de mensajería mediante métodos de la interfaz [OLE IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa5ad-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="fa5ad-117">Llame al [método IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) para liberar el **objeto ITnef.**</span><span class="sxs-lookup"><span data-stu-id="fa5ad-117">Call the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="fa5ad-118">**Para procesar un mensaje TNEF entrante**</span><span class="sxs-lookup"><span data-stu-id="fa5ad-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="fa5ad-119">Obtenga un objeto de mensaje MAPI de la cola MAPI y escriba las propiedades del encabezado del mensaje en el nuevo mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="fa5ad-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="fa5ad-120">Cree e inicialice un [objeto IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para que contenga los datos TNEF del mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="fa5ad-120">Create and initialize an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="fa5ad-121">Pase el mensaje MAPI y [el objeto IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) a [la función OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="fa5ad-121">Pass the MAPI message and the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="fa5ad-122">Descodifica la información de los datos TNEF llamando al método [ITnef::ExtractProps.](itnef-extractprops.md)</span><span class="sxs-lookup"><span data-stu-id="fa5ad-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="fa5ad-123">Cualquier elemento descodificado por **ExtractProps** sobrescribirá las propiedades descodificadas del sobre del mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="fa5ad-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="fa5ad-124">Es decir, las propiedades TNEF extraídas sobrescribirán las propiedades existentes en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="fa5ad-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="fa5ad-125">Procese el texto del mensaje etiquetado llamando [a ITnef::OpenTaggedBody](itnef-opentaggedbody.md) y analice el texto para recuperar las posiciones de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="fa5ad-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="fa5ad-126">Guarde el mensaje llamando a [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="fa5ad-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="fa5ad-127">Libere el objeto TNEF llamando al [método IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa5ad-127">Release the TNEF object by calling the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

