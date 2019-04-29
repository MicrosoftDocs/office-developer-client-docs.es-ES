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
# <a name="creating-a-message-attachment"></a><span data-ttu-id="0a7cc-103">Crear un archivo adjunto de mensaje</span><span class="sxs-lookup"><span data-stu-id="0a7cc-103">Creating a message attachment</span></span>
  
<span data-ttu-id="0a7cc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a7cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a7cc-105">Los datos adjuntos de un mensaje son datos adicionales, como un archivo, otro mensaje o un objeto OLE, que puede enviar o guardar junto con un mensaje.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="0a7cc-106">Cada archivo adjunto tiene una colección de propiedades que lo identifican y describen su tipo y cómo se representa.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="0a7cc-107">Al igual que los destinatarios, solo se puede tener acceso a los datos adjuntos de los mensajes a través del mensaje al que pertenecen.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="0a7cc-108">Por lo tanto, para que los datos adjuntos se puedan usar, el mensaje debe estar abierto.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="0a7cc-109">Crear un dato adjunto de mensaje</span><span class="sxs-lookup"><span data-stu-id="0a7cc-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="0a7cc-110">Llame al método [IMessage:: CreateAttach](imessage-createattach.md) del mensaje y pase NULL como identificador de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="0a7cc-111">**CreateAttach** devuelve un número que identifica de forma única los nuevos datos adjuntos en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="0a7cc-112">El número de datos adjuntos se almacena en la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) y solo es válido mientras el mensaje que contiene los datos adjuntos esté abierto.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="0a7cc-113">Llame a [IMAPIProp:: SetProps](imapiprop-setprops.md) para establecer **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) para indicar cómo tener acceso a los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="0a7cc-114">Se requiere **PR_ATTACH_METHOD** .</span><span class="sxs-lookup"><span data-stu-id="0a7cc-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="0a7cc-115">Establézcalo en:</span><span class="sxs-lookup"><span data-stu-id="0a7cc-115">Set it to:</span></span> 
    
   - <span data-ttu-id="0a7cc-116">ATTACH_BY_VALUE si los datos adjuntos son datos binarios.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="0a7cc-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE o ATTACH_BY_REF_ONLY si los datos adjuntos son un archivo.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="0a7cc-118">ATTACH_EMBEDDED_MSG si los datos adjuntos son un mensaje.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="0a7cc-119">ATTACH_OLE si los datos adjuntos son un objeto OLE.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="0a7cc-120">Establezca la propiedad de datos adjuntos adecuada:</span><span class="sxs-lookup"><span data-stu-id="0a7cc-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="0a7cc-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) para datos binarios y objetos OLE 1.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="0a7cc-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) para los archivos.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="0a7cc-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) para mensajes y objetos OLE 2.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="0a7cc-124">Establezca **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) para que contenga la representación gráfica de los datos adjuntos de archivos o datos adjuntos binarios.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="0a7cc-125">No la establezca para objetos OLE, que almacenan la información de representación de forma interna o para mensajes adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="0a7cc-126">Establezca **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para indicar dónde se deben mostrar los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="0a7cc-127">**PR_RENDERING_POSITION** solo se aplica a los clientes que establecen la propiedad **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="0a7cc-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="0a7cc-128">Si solo admite **PR_RTF_COMPRESSED**, incluya la siguiente información de marcador de posición en la secuencia comprimida:</span><span class="sxs-lookup"><span data-stu-id="0a7cc-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="0a7cc-129">Para establecer **PR_RENDERING_POSITION**, asigne un número que represente un desplazamiento ordinal en caracteres, donde el primer carácter de **PR_BODY** sea 0, si necesita saber en qué lugar del mensaje se representa el archivo adjunto, o 0xFFFFFFFF, si no lo hace representar datos adjuntos dentro de **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="0a7cc-130">Establecer **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) para indicar el nombre corto del archivo para un archivo adjunto y **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) para indicar el nombre del archivo como compatible en una plataforma que controla el formato de nombre de archivo largo.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="0a7cc-131">Ambas propiedades son opcionales.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-131">Both properties are optional.</span></span> <span data-ttu-id="0a7cc-132">Sin embargo, si establece **PR_ATTACH_LONG_FILENAME**, también establece **PR_ATTACH_FILENAME**.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="0a7cc-133">Establezca **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para indicar el nombre de los datos adjuntos que pueden aparecer en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="0a7cc-134">PR_DISPLAY_NAME es opcional.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-prattachdatabin"></a><span data-ttu-id="0a7cc-135">Establecer PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="0a7cc-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="0a7cc-136">Llame a [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir la propiedad con la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0a7cc-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="0a7cc-137">Si un archivo contiene los datos y está abierto o si necesita controlar explícitamente el tamaño del búfer, llame a **IStream:: Write** en un bucle para ubicar los datos en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="0a7cc-138">Otra opción es llamar a **OpenStreamOnFile** para crear una secuencia para obtener acceso al archivo de datos y, a continuación, llamar al método **IStream:: CopyTo** de la secuencia para copiar los datos en la secuencia devuelta por **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="0a7cc-139">Llamar al método **IStream:: commit** de la nueva secuencia.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-prattachdataobj"></a><span data-ttu-id="0a7cc-140">Establecer PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="0a7cc-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="0a7cc-141">Llame a **IMAPIProp:: OpenProperty** para abrir la propiedad con la interfaz **IStreamDocfile** para crear una secuencia que funcione con el almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="0a7cc-142">**IStreamDocfile** está implementado por los proveedores de almacenamiento de mensajes para proporcionar a los clientes una forma de mayor rendimiento para almacenar y recuperar almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="0a7cc-143">La interfaz **IStreamDocfile** es la misma que **IStream**, pero se garantiza que el contenido de la secuencia tiene el formato de almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="0a7cc-144">Si la llamada se realiza correctamente, cree la secuencia con los mismos pasos detallados para la configuración **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="0a7cc-145">Si **OpenProperty** produce un error:</span><span class="sxs-lookup"><span data-stu-id="0a7cc-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="0a7cc-146">Vuelva a llamar a **OpenProperty** para obtener el **IStorage**.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="0a7cc-147">Llame a **StgOpenStorage** para abrir el objeto OLE y devolver un objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="0a7cc-148">Llamar al método **IStorage:: CopyTo** del objeto de almacenamiento devuelto para copiarlo en el objeto de almacenamiento devuelto desde **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="0a7cc-149">Llamar al método **IStorage:: commit** del nuevo objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-prattachpathname"></a><span data-ttu-id="0a7cc-150">Establecer PR_ATTACH_PATHNAME</span><span class="sxs-lookup"><span data-stu-id="0a7cc-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="0a7cc-151">Asigne una estructura [SPropValue](spropvalue.md) , configure el miembro **ulPropTag** a **PR_ATTACH_PATHNAME** y el miembro **Value. LPSZ** a la cadena de caracteres que representa el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="0a7cc-152">Llame al método [IMAPIProp:: SetProps](imapiprop-setprops.md) del archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="0a7cc-153">Si la plataforma admite nombres de archivo largos, establezca tanto **PR_ATTACH_PATHNAME** como **PR_ATTACH_LONG_PATHNAME**.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="0a7cc-154">Puede que sea necesario realizar una llamada de sistema operativo para recuperar el nombre corto del archivo.</span><span class="sxs-lookup"><span data-stu-id="0a7cc-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0a7cc-155">Ver también</span><span class="sxs-lookup"><span data-stu-id="0a7cc-155">See also</span></span>

- [<span data-ttu-id="0a7cc-156">Datos adJuntos MAPI</span><span class="sxs-lookup"><span data-stu-id="0a7cc-156">MAPI Attachments</span></span>](mapi-attachments.md)

