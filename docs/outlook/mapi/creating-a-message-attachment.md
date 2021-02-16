---
title: Crear un archivo adjunto de mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2bdba3574c962c825f45cd098efa1cba6e21a4ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405999"
---
# <a name="creating-a-message-attachment"></a><span data-ttu-id="4be8d-103">Crear un archivo adjunto de mensaje</span><span class="sxs-lookup"><span data-stu-id="4be8d-103">Creating a message attachment</span></span>
  
<span data-ttu-id="4be8d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4be8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4be8d-105">Los datos adjuntos de un mensaje son algunos datos adicionales, como un archivo, otro mensaje o un objeto OLE, que puede enviar o guardar junto con un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4be8d-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="4be8d-106">Cada dato adjunto tiene una colección de propiedades que lo identifica y describe su tipo y cómo se representa.</span><span class="sxs-lookup"><span data-stu-id="4be8d-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="4be8d-107">Al igual que los destinatarios, solo se puede tener acceso a los datos adjuntos de los mensajes a través del mensaje al que pertenecen.</span><span class="sxs-lookup"><span data-stu-id="4be8d-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="4be8d-108">Por lo tanto, para que se puedan usar datos adjuntos, su mensaje debe estar abierto.</span><span class="sxs-lookup"><span data-stu-id="4be8d-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="4be8d-109">Crear datos adjuntos de un mensaje</span><span class="sxs-lookup"><span data-stu-id="4be8d-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="4be8d-110">Llama al método [IMessage::CreateAttach](imessage-createattach.md) del mensaje y pasa NULL como identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="4be8d-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="4be8d-111">**CreateAttach devuelve** un número que identifica de forma exclusiva los nuevos datos adjuntos dentro del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4be8d-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="4be8d-112">El número de datos adjuntos se almacena en la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) y solo es válido mientras el mensaje que contiene los datos adjuntos esté abierto.</span><span class="sxs-lookup"><span data-stu-id="4be8d-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="4be8d-113">Llame [a IMAPIProp::SetProps](imapiprop-setprops.md) para establecer **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) para indicar cómo obtener acceso a los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4be8d-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="4be8d-114">**PR_ATTACH_METHOD** es necesario.</span><span class="sxs-lookup"><span data-stu-id="4be8d-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="4be8d-115">Estacórlo en:</span><span class="sxs-lookup"><span data-stu-id="4be8d-115">Set it to:</span></span> 
    
   - <span data-ttu-id="4be8d-116">ATTACH_BY_VALUE si los datos adjuntos son datos binarios.</span><span class="sxs-lookup"><span data-stu-id="4be8d-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="4be8d-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE o ATTACH_BY_REF_ONLY si los datos adjuntos son un archivo.</span><span class="sxs-lookup"><span data-stu-id="4be8d-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="4be8d-118">ATTACH_EMBEDDED_MSG si los datos adjuntos son un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4be8d-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="4be8d-119">ATTACH_OLE si los datos adjuntos son un objeto OLE.</span><span class="sxs-lookup"><span data-stu-id="4be8d-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="4be8d-120">Establezca la propiedad de datos adjuntos apropiada:</span><span class="sxs-lookup"><span data-stu-id="4be8d-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="4be8d-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) para datos binarios y objetos OLE 1.</span><span class="sxs-lookup"><span data-stu-id="4be8d-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="4be8d-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) para los archivos.</span><span class="sxs-lookup"><span data-stu-id="4be8d-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="4be8d-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) para mensajes y objetos OLE 2.</span><span class="sxs-lookup"><span data-stu-id="4be8d-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="4be8d-124">Establezca **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) para contener la representación gráfica de los datos adjuntos de archivos o datos adjuntos binarios.</span><span class="sxs-lookup"><span data-stu-id="4be8d-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="4be8d-125">No lo establezca para objetos OLE, que almacenan la información de representación internamente o para mensajes adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4be8d-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="4be8d-126">Establezca **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para indicar dónde deben mostrarse los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4be8d-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="4be8d-127">**PR_RENDERING_POSITION** se aplica solo a los clientes que establecen la **PR_BODY** propiedad.</span><span class="sxs-lookup"><span data-stu-id="4be8d-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="4be8d-128">Si solo admite la **PR_RTF_COMPRESSED**, coloque la siguiente información de marcador de posición en la secuencia comprimida:</span><span class="sxs-lookup"><span data-stu-id="4be8d-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="4be8d-129">Para establecer PR_RENDERING_POSITION **,** asigne un número que represente un desplazamiento ordinal en caracteres, con el primer carácter de **PR_BODY** en 0, si necesita saber dónde se representan los datos adjuntos en el mensaje o 0xFFFFFFFF, si no representa datos adjuntos dentro de **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="4be8d-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="4be8d-130">Establezca **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) para indicar el nombre corto del archivo para un archivo adjunto y **PR \_ ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) para indicar el nombre del archivo tal como se admite en una plataforma que controla el formato de nombre de archivo largo.</span><span class="sxs-lookup"><span data-stu-id="4be8d-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="4be8d-131">Ambas propiedades son opcionales.</span><span class="sxs-lookup"><span data-stu-id="4be8d-131">Both properties are optional.</span></span> <span data-ttu-id="4be8d-132">Sin embargo, si establece **PR_ATTACH_LONG_FILENAME**, también establecer **PR_ATTACH_FILENAME**.</span><span class="sxs-lookup"><span data-stu-id="4be8d-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="4be8d-133">Establezca **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para indicar el nombre de los datos adjuntos que pueden aparecer en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4be8d-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="4be8d-134">PR_DISPLAY_NAME es opcional.</span><span class="sxs-lookup"><span data-stu-id="4be8d-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-pr_attach_data_bin"></a><span data-ttu-id="4be8d-135">Establecer PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="4be8d-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="4be8d-136">Llame [a IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la propiedad con la **interfaz IStream.**</span><span class="sxs-lookup"><span data-stu-id="4be8d-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="4be8d-137">Si un archivo contiene los datos y está abierto o si necesitas un control explícito sobre el tamaño del búfer, llama a **IStream::Write** en un bucle para colocar los datos en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="4be8d-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="4be8d-138">Otra opción es llamar a **OpenStreamOnFile** para crear una secuencia para tener acceso al archivo de datos y, a continuación, llamar al método **IStream::CopyTo** de esta secuencia para copiar los datos en la secuencia devuelta por **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="4be8d-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="4be8d-139">Llama al método **IStream::Commit** de la nueva secuencia.</span><span class="sxs-lookup"><span data-stu-id="4be8d-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-pr_attach_data_obj"></a><span data-ttu-id="4be8d-140">Establecer PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="4be8d-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="4be8d-141">Llame **a IMAPIProp::OpenProperty** para abrir la propiedad con la interfaz **IStreamDocfile** para crear una secuencia que funcione con almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="4be8d-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="4be8d-142">Los proveedores de almacén de mensajes implementan **IStreamDocfile** para proporcionar a los clientes una forma de mayor rendimiento de almacenar y recuperar almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="4be8d-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="4be8d-143">La **interfaz IStreamDocfile** es la misma que **IStream,** pero se garantiza que el contenido de la secuencia tenga el formato de almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="4be8d-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="4be8d-144">Si esta llamada se realiza correctamente, cree la secuencia con los mismos pasos descritos para establecer **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="4be8d-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="4be8d-145">Si **se produce un error en OpenProperty:**</span><span class="sxs-lookup"><span data-stu-id="4be8d-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="4be8d-146">Vuelva **a llamar a OpenProperty** **solicitando IStorage**.</span><span class="sxs-lookup"><span data-stu-id="4be8d-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="4be8d-147">Llame **a StgOpenStorage** para abrir el objeto OLE y devolver un objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="4be8d-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="4be8d-148">Llame al método **IStorage::CopyTo** del objeto de almacenamiento devuelto para copiar al objeto de almacenamiento devuelto desde **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="4be8d-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="4be8d-149">Llame al método **IStorage::Commit** del nuevo objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="4be8d-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-pr_attach_pathname"></a><span data-ttu-id="4be8d-150">Establecer PR_ATTACH_PATHNAME</span><span class="sxs-lookup"><span data-stu-id="4be8d-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="4be8d-151">Asigna una [estructura SPropValue,](spropvalue.md) estableciendo el miembro **ulPropTag** en **PR_ATTACH_PATHNAME** y el miembro **Value.LPSZ** en la cadena de caracteres que representa el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="4be8d-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="4be8d-152">Llame al método [IMAPIProp::SetProps](imapiprop-setprops.md) de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4be8d-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="4be8d-153">Si su plataforma admite nombres de archivo largos, establezca **PR_ATTACH_PATHNAME** y **PR_ATTACH_LONG_PATHNAME**.</span><span class="sxs-lookup"><span data-stu-id="4be8d-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="4be8d-154">Puede que sea necesario realizar una llamada al sistema operativo para recuperar el nombre de archivo corto.</span><span class="sxs-lookup"><span data-stu-id="4be8d-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4be8d-155">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4be8d-155">See also</span></span>

- [<span data-ttu-id="4be8d-156">Datos adjuntos mapi</span><span class="sxs-lookup"><span data-stu-id="4be8d-156">MAPI Attachments</span></span>](mapi-attachments.md)

