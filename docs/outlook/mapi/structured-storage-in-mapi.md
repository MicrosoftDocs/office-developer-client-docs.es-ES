---
title: Almacenamiento estructurado en MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 462ee84d5e9acd26f80bae6516179f21651749be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820795"
---
# <a name="structured-storage-in-mapi"></a><span data-ttu-id="6cbad-103">Almacenamiento estructurado en MAPI</span><span class="sxs-lookup"><span data-stu-id="6cbad-103">Structured Storage in MAPI</span></span>

  
  
<span data-ttu-id="6cbad-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6cbad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6cbad-105">Almacenamiento estructurado hace referencia a la organización jerárquica de almacenamiento de información que se introdujo con COM.</span><span class="sxs-lookup"><span data-stu-id="6cbad-105">Structured storage refers to the hierarchical organization of storage introduced with COM.</span></span> <span data-ttu-id="6cbad-106">En un entorno de almacenamiento estructurado, el almacenamiento se organiza en dos o tres tipos de objetos:</span><span class="sxs-lookup"><span data-stu-id="6cbad-106">In a structured storage environment, storage is organized into two or three types of objects:</span></span> 
  
- <span data-ttu-id="6cbad-107">Objetos Stream</span><span class="sxs-lookup"><span data-stu-id="6cbad-107">Stream objects</span></span>
    
- <span data-ttu-id="6cbad-108">Objetos de bytes de bloqueo</span><span class="sxs-lookup"><span data-stu-id="6cbad-108">Lock bytes objects</span></span>
    
- <span data-ttu-id="6cbad-109">Objetos de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="6cbad-109">Storage objects</span></span>
    
<span data-ttu-id="6cbad-110">Bytes de secuencia y bloqueo son objetos de nivel inferior que tener acceso directamente a los datos.</span><span class="sxs-lookup"><span data-stu-id="6cbad-110">Stream and lock bytes are lower-level objects that directly access the data.</span></span> <span data-ttu-id="6cbad-111">Objetos Stream de implementan la interfaz **IStream** que define los métodos para leer, escribir, posicionamiento y acciones como copiar bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="6cbad-111">Stream objects implement the **IStream** interface which defines methods for reading, writing, positioning, and copying bytes of data.</span></span> <span data-ttu-id="6cbad-112">Bloquear bytes objetos implementan otra interfaz COM, **ILockBytes**, para tener acceso a datos con una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="6cbad-112">Lock bytes objects implement another COM interface, **ILockBytes**, to access data with a byte array.</span></span> <span data-ttu-id="6cbad-113">Matrices de bytes se suelen usar para proporcionar acceso personalizado a almacenamiento subyacente.</span><span class="sxs-lookup"><span data-stu-id="6cbad-113">Byte arrays are typically used to provide customized access to underlying storage.</span></span>
  
<span data-ttu-id="6cbad-114">Objetos de almacenamiento se coloca sobre los objetos de bytes de secuencia o bloqueo; que pueden contener uno o varios de estos objetos, así como otros objetos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="6cbad-114">Storage objects are layered on top of the stream or lock bytes objects; they can contain one or more of these objects as well as other storage objects.</span></span> <span data-ttu-id="6cbad-115">Objetos de almacenamiento implementan la interfaz de **IStorage** que define los métodos para crear, obtener acceso a y mantener los objetos anidados.</span><span class="sxs-lookup"><span data-stu-id="6cbad-115">Storage objects implement the **IStorage** interface which defines methods for creating, accessing, and maintaining nested objects.</span></span> 
  
<span data-ttu-id="6cbad-116">Debido a que **IStream**, **ILockBytes**y **IStorage** son interfaces COM en lugar de interfaces MAPI, sus métodos devuelven valores de error de COM en lugar de MAPI.</span><span class="sxs-lookup"><span data-stu-id="6cbad-116">Because **IStream**, **ILockBytes**, and **IStorage** are COM interfaces rather than MAPI interfaces, their methods return COM error values rather than MAPI values.</span></span> <span data-ttu-id="6cbad-117">Los clientes y proveedores de servicios de llamar a métodos de estas interfaces deben usar la función de la API **MapStorageSCode** para traducir estos valores en valores de error MAPI.</span><span class="sxs-lookup"><span data-stu-id="6cbad-117">Clients and service providers calling methods in these interfaces must use the API function **MapStorageSCode** to translate these values into MAPI error values.</span></span> <span data-ttu-id="6cbad-118">Para obtener más información, vea [MapStorageSCode](mapstoragescode.md).</span><span class="sxs-lookup"><span data-stu-id="6cbad-118">For more information, see [MapStorageSCode](mapstoragescode.md).</span></span>
  
<span data-ttu-id="6cbad-119">Los clientes y proveedores de servicios de usan almacenamiento estructurado para trabajar con las propiedades que son demasiado grandes para mantener con los métodos **IMAPIProp** , cadena suelen ser grande y propiedades binarias.</span><span class="sxs-lookup"><span data-stu-id="6cbad-119">Clients and service providers use structured storage for working with properties that are too large to maintain with the **IMAPIProp** methods, typically large string and binary properties.</span></span> <span data-ttu-id="6cbad-120">Una de las maneras comunes que los clientes o proveedores de servicios de obtener acceso a ellos es mediante la especificación de **IStream** o **IStorage** como el identificador de interfaz en una llamada al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="6cbad-120">One of the common ways that clients or service providers access them is by specifying **IStream** or **IStorage** as the interface identifier in a call to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="6cbad-121">Por ejemplo, los clientes llaman **OpenProperty** con **PR_ATTACH_DATA_BIN** como la etiqueta de propiedad y IID_IStream como el identificador de interfaz para tener acceso a datos adjuntos binarios en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="6cbad-121">For example, clients call **OpenProperty** with **PR_ATTACH_DATA_BIN** as the property tag and IID_IStream as the interface identifier to access a binary attachment in a message.</span></span> 
  
<span data-ttu-id="6cbad-122">Los clientes y proveedores de servicios pueden implementar sus propios objetos stream y almacenamiento de información o llamar a funciones de la API para las implementaciones de acceso proporcionadas por MAPI o COM.</span><span class="sxs-lookup"><span data-stu-id="6cbad-122">Clients and service providers can implement their own stream and storage objects or call API functions to access implementations supplied by MAPI or COM.</span></span> <span data-ttu-id="6cbad-123">Debido a que las implementaciones proporcionadas atender la mayoría de los casos, los clientes y proveedores de servicios con muy poca frecuencia necesitan crear sus propios.</span><span class="sxs-lookup"><span data-stu-id="6cbad-123">Because the supplied implementations serve most purposes, clients and service providers rarely need to create their own.</span></span> 
  
<span data-ttu-id="6cbad-124">Cuando un cliente llama **OpenProperty** en un objeto MAPI para tener acceso a una de sus propiedades a través de un objeto de almacenamiento, el proveedor de servicios normalmente abrirá el objeto de almacenamiento en modo directo.</span><span class="sxs-lookup"><span data-stu-id="6cbad-124">When a client calls **OpenProperty** on a MAPI object to access one of its properties through a storage object, the service provider will typically open the storage object in direct mode.</span></span> <span data-ttu-id="6cbad-125">Sin embargo, esto es típico en lugar de comportamiento necesario.</span><span class="sxs-lookup"><span data-stu-id="6cbad-125">However, this is typical rather than required behavior.</span></span> <span data-ttu-id="6cbad-126">Los clientes deben se presupone que todos los objetos de almacenamiento abiertos o creados por proveedores de servicios se negocian y requieren una llamada a **IStorage::Commit**.</span><span class="sxs-lookup"><span data-stu-id="6cbad-126">Clients should assume that all storage objects opened or created by service providers are transacted and require a call to **IStorage::Commit**.</span></span> <span data-ttu-id="6cbad-127">También debe recordar que los cambios realizados en los objetos de almacenamiento no estarán permanentes hasta que llame a **IMAPIProp::SaveChanges** después de la última **Confirmar** para guardar el objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="6cbad-127">They should also remember that changes to storage objects will not be made permanent until they call **IMAPIProp::SaveChanges** after the final **Commit** to save the MAPI object.</span></span> <span data-ttu-id="6cbad-128">Para obtener más información, vea [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="6cbad-128">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
  
<span data-ttu-id="6cbad-129">MAPI y COM proporcionan varias funciones de la API para definir ni obtener acceso a los objetos stream y almacenamiento de información.</span><span class="sxs-lookup"><span data-stu-id="6cbad-129">MAPI and COM provide several API functions for defining or accessing storage and stream objects.</span></span> <span data-ttu-id="6cbad-130">En la siguiente tabla, se describen las funciones usadas con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="6cbad-130">The commonly used functions are described in the following table.</span></span>
  
<span data-ttu-id="6cbad-131">**Funciones para obtener acceso a los objetos Stream y almacenamiento**</span><span class="sxs-lookup"><span data-stu-id="6cbad-131">**Functions for Accessing Storage and Stream Objects**</span></span>

|<span data-ttu-id="6cbad-132">**Función**</span><span class="sxs-lookup"><span data-stu-id="6cbad-132">**Function**</span></span>|<span data-ttu-id="6cbad-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6cbad-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6cbad-134">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="6cbad-134">HrIStorageFromStream</span></span>](hristoragefromstream.md) <br/> |<span data-ttu-id="6cbad-135">Crea un objeto de almacenamiento para obtener acceso a un objeto de bytes de secuencias o de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="6cbad-135">Creates a storage object to access a stream or lock bytes object.</span></span>  <br/> |
|[<span data-ttu-id="6cbad-136">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="6cbad-136">OpenIMsgOnIStg</span></span>](openimsgonistg.md) <br/> |<span data-ttu-id="6cbad-137">Crea un objeto de mensaje para tener acceso a un objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="6cbad-137">Creates a message object to access a storage object.</span></span>  <br/> |
|[<span data-ttu-id="6cbad-138">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="6cbad-138">OpenStreamOnFile</span></span>](openstreamonfile.md) <br/> |<span data-ttu-id="6cbad-139">Crea un objeto stream para tener acceso a un archivo.</span><span class="sxs-lookup"><span data-stu-id="6cbad-139">Creates a stream object to access a file.</span></span>  <br/> |
|[<span data-ttu-id="6cbad-140">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="6cbad-140">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md) <br/> |<span data-ttu-id="6cbad-141">Crea un objeto stream que contiene la versión comprimida o sin comprimir de un objeto stream que contiene el texto enriquecido de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="6cbad-141">Creates a stream object that contains the compressed or uncompressed version of a stream holding the rich text of a message.</span></span>  <br/> |
   
 <span data-ttu-id="6cbad-142">**Para recuperar los nombres de las secuencias de un determinado subalmacenamiento**</span><span class="sxs-lookup"><span data-stu-id="6cbad-142">**To retrieve the names of the streams in a given substorage**</span></span>
  
1. <span data-ttu-id="6cbad-143">Llamar al método **IStorage::EnumElements** del subalmacenamiento para obtener una interfaz **IEnumSTATSTG** .</span><span class="sxs-lookup"><span data-stu-id="6cbad-143">Call the substorage's **IStorage::EnumElements** method to get an **IEnumSTATSTG** interface.</span></span> 
    
2. <span data-ttu-id="6cbad-144">Llame al método **IEnumSTATSTG::Next** con tantos estructuras **STATSTG** en un momento tal y como se puede.</span><span class="sxs-lookup"><span data-stu-id="6cbad-144">Call **IEnumSTATSTG::Next** with as many **STATSTG** structures at a time as you can.</span></span> <span data-ttu-id="6cbad-145">Si se solicita 100 a la vez, **siguiente** normalmente devolverá S_FALSE con el contenido de _pceltFetched_ establecido en el número que se recuperaron realmente.</span><span class="sxs-lookup"><span data-stu-id="6cbad-145">If you ask for 100 at a time, **Next** will usually return S_FALSE with the contents of  _pceltFetched_ set to the number that were actually retrieved.</span></span> 
    
3. <span data-ttu-id="6cbad-146">Verificación de las estructuras de **STATSTG** que se marcan con STGTY_STREAM.</span><span class="sxs-lookup"><span data-stu-id="6cbad-146">Check for the **STATSTG** structures that are flagged with STGTY_STREAM.</span></span> 
    
4. <span data-ttu-id="6cbad-147">El parámetro _pwcsName_ la versión.</span><span class="sxs-lookup"><span data-stu-id="6cbad-147">Release the  _pwcsName_ parameter.</span></span> 
    
 <span data-ttu-id="6cbad-148">**Para crear un objeto de almacenamiento para obtener acceso a un objeto existente de bytes de secuencias o de bloqueo**</span><span class="sxs-lookup"><span data-stu-id="6cbad-148">**To create a storage object to access an existing stream or lock bytes object**</span></span>
  
- <span data-ttu-id="6cbad-149">Los clientes llaman [HrIStorageFromStream](hristoragefromstream.md).</span><span class="sxs-lookup"><span data-stu-id="6cbad-149">Clients call [HrIStorageFromStream](hristoragefromstream.md).</span></span> 
    
 <span data-ttu-id="6cbad-150">**Para crear un objeto de mensaje para tener acceso a un objeto de almacenamiento existente**</span><span class="sxs-lookup"><span data-stu-id="6cbad-150">**To create a message object to access an existing storage object**</span></span>
  
- <span data-ttu-id="6cbad-151">Los clientes y proveedores de servicios de llamada [OpenIMsgOnIStg](openimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="6cbad-151">Service providers and clients call [OpenIMsgOnIStg](openimsgonistg.md).</span></span> <span data-ttu-id="6cbad-152">El objeto de mensaje que se crea difiere de los objetos de mensaje que normalmente creados los proveedores de almacén de mensajes en que no admite todos los [IMessage: IMAPIProp](imessageimapiprop.md) métodos, como **IMessage::SubmitMessage**de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="6cbad-152">The message object that is created differs from the message objects typically created by message store providers in that it does not support all of the [IMessage : IMAPIProp](imessageimapiprop.md) interface methods, such as **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="6cbad-153">Un parámetro de entrada opcional para **OpenIMsgOnIStg** es una función de devolución de llamada que se ajusta al prototipo [MSGCALLRELEASE](msgcallrelease.md) .</span><span class="sxs-lookup"><span data-stu-id="6cbad-153">An optional input parameter to **OpenIMsgOnIStg** is a callback function that conforms to the [MSGCALLRELEASE](msgcallrelease.md) prototype.</span></span> <span data-ttu-id="6cbad-154">Esta función se denomina por el nuevo objeto de mensaje cuando el recuento de referencia del mensaje llega a cero.</span><span class="sxs-lookup"><span data-stu-id="6cbad-154">This function is called by the new message object when the message's reference count reaches zero.</span></span> <span data-ttu-id="6cbad-155">Implementación de una función **MSGCALLRELEASE** puede ser útil para llevar a cabo el procesamiento final antes de quitar completamente el mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="6cbad-155">Implementing a **MSGCALLRELEASE** function can be useful for performing final processing before the new message is completely removed.</span></span> 
    
<span data-ttu-id="6cbad-156">[OpenStreamOnFile](openstreamonfile.md) normalmente se usa para almacenar los datos adjuntos del archivo porque crea una secuencia que lee y escribe en un archivo.</span><span class="sxs-lookup"><span data-stu-id="6cbad-156">[OpenStreamOnFile](openstreamonfile.md) is commonly used for storing file attachments because it creates a stream that reads from and writes to a file.</span></span> <span data-ttu-id="6cbad-157">**OpenProperty** con **PR_ATTACH_DATA_BIN** como la etiqueta de propiedad crea una secuencia para almacenar los datos adjuntos binarios.</span><span class="sxs-lookup"><span data-stu-id="6cbad-157">**OpenProperty** with **PR_ATTACH_DATA_BIN** as the property tag creates a stream for storing binary attachment data.</span></span> 
  
 <span data-ttu-id="6cbad-158">**Para comprimir o descomprimir una secuencia que contiene el texto del mensaje en el formato de texto enriquecido**</span><span class="sxs-lookup"><span data-stu-id="6cbad-158">**To compress or uncompress a stream containing message text in the Rich Text Format**</span></span>
  
- <span data-ttu-id="6cbad-159">Los clientes llaman [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span><span class="sxs-lookup"><span data-stu-id="6cbad-159">Clients call [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span> <span data-ttu-id="6cbad-160">**WrapCompressedRTFStream** crea una secuencia que se ajusta a la secuencia RTF.</span><span class="sxs-lookup"><span data-stu-id="6cbad-160">**WrapCompressedRTFStream** creates a stream that wraps the RTF stream.</span></span> <span data-ttu-id="6cbad-161">La secuencia de contenedor no implementa todos los métodos **IStream** ; se excluyen los siguientes métodos: **Seek**, **SetSize**, **Revertir**, **métodos LockRegion**, **UnlockRegion**, **Stat**y **clon**.</span><span class="sxs-lookup"><span data-stu-id="6cbad-161">The wrapper stream does not implement all of the **IStream** methods; the following methods are excluded: **Seek**, **SetSize**, **Revert**, **LockRegion**, **UnlockRegion**, **Stat**, and **Clone**.</span></span> <span data-ttu-id="6cbad-162">Esto es debido a que los objetos de secuencia creados por **WrapCompressedRTFStream** no admiten **SetSize** o **Stat**, no hay una forma sencilla de extender o recuperar su tamaño.</span><span class="sxs-lookup"><span data-stu-id="6cbad-162">This is because the stream objects created by **WrapCompressedRTFStream** do not support either **SetSize** or **Stat**, there is not an easy way to either extend or retrieve their size.</span></span> <span data-ttu-id="6cbad-163">Es la mejor estrategia seleccionar un tamaño de búfer razonable y leer o escribir en un bucle.</span><span class="sxs-lookup"><span data-stu-id="6cbad-163">The best strategy is to pick a reasonable buffer size and read or write in a loop.</span></span>
    
> [!NOTE]
> <span data-ttu-id="6cbad-164">COM tiene una implementación de objeto de almacenamiento en función de una matriz de bytes que devuelve un objeto **IEnumSTATSTG** desde el método **EnumElements** que es problemático.</span><span class="sxs-lookup"><span data-stu-id="6cbad-164">COM has a storage object implementation based on a byte array that returns an **IEnumSTATSTG** object from the **EnumElements** method that is problematic.</span></span> <span data-ttu-id="6cbad-165">En concreto, el método **QueryInterface** no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="6cbad-165">In particular, the **QueryInterface** method does not work correctly.</span></span> <span data-ttu-id="6cbad-166">Proveedores de servicios que implementan sus propios objetos de almacenamiento de información mediante la implementación de COM deben crear un contenedor fino para el objeto **IEnumSTATSTG** que reenvía las llamadas a los métodos **IEnumSTATSTG** subyacentes pero implementa su propio **AddRef **, **Versión**, **QueryInterface**y **clon** métodos.</span><span class="sxs-lookup"><span data-stu-id="6cbad-166">Service providers that implement their own storage objects using the COM implementation should create a thin wrapper for the **IEnumSTATSTG** object that forwards calls on to the underlying **IEnumSTATSTG** methods but implements its own **AddRef**, **Release**, **QueryInterface**, and **Clone** methods.</span></span> 
  
