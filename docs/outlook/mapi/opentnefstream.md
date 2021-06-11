---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 524b52026010b9a06d5822b48b7c04bbf90a113e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423961"
---
# <a name="opentnefstream"></a><span data-ttu-id="366c7-103">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="366c7-103">OpenTnefStream</span></span>

<span data-ttu-id="366c7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="366c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="366c7-105">Llamado por un proveedor de transporte para iniciar una sesión de formato de encapsulación neutral de transporte MAPI (TNEF).</span><span class="sxs-lookup"><span data-stu-id="366c7-105">Called by a transport provider to initiate a MAPI Transport Neutral Encapsulation Format (TNEF) session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="366c7-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="366c7-106">Header file:</span></span>  <br/> |<span data-ttu-id="366c7-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="366c7-107">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="366c7-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="366c7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="366c7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="366c7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="366c7-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="366c7-110">Called by:</span></span>  <br/> |<span data-ttu-id="366c7-111">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="366c7-111">Transport providers</span></span>  <br/> |
   
```cpp
HRESULT OpenTnefStream(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName, 
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKey,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a><span data-ttu-id="366c7-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="366c7-112">Parameters</span></span>

<span data-ttu-id="366c7-113">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="366c7-113">_lpvSupport_</span></span>
  
> <span data-ttu-id="366c7-114">[in] Pasa un objeto de soporte técnico o pasa null.</span><span class="sxs-lookup"><span data-stu-id="366c7-114">[in] Passes a support object, or passes in NULL.</span></span> 
    
<span data-ttu-id="366c7-115">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="366c7-115">_lpStream_</span></span>
  
> <span data-ttu-id="366c7-116">[in] Puntero a una interfaz OLE **IStream** de objeto de secuencia de almacenamiento que proporciona un origen o destino para un mensaje de secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="366c7-116">[in] Pointer to a storage stream object OLE **IStream** interface providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="366c7-117">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="366c7-117">_lpszStreamName_</span></span>
  
> <span data-ttu-id="366c7-118">[in] Puntero al nombre de la secuencia de datos que usa el objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="366c7-118">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="366c7-119">Si el autor de la llamada ha establecido la marca de TNEF_ENCODE ( _parámetro ulFlags)_ en su llamada a **OpenTnefStream**, el parámetro  _lpszName_ debe especificar un puntero que no sea nulo a una cadena que no sea nula y que consista en cualquier carácter que se considere válido para asignar un nombre a un archivo.</span><span class="sxs-lookup"><span data-stu-id="366c7-119">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="366c7-120">MAPI no permite nombres de cadena, incluidos los caracteres "[", "]" o ., incluso si el sistema de archivos permite su uso.</span><span class="sxs-lookup"><span data-stu-id="366c7-120">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="366c7-121">El tamaño de la cadena pasada para  _lpszName_ no debe superar el valor de MAX_PATH, la longitud máxima de una cadena que contiene un nombre de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="366c7-121">The size of the string passed for  _lpszName_ must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="366c7-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="366c7-122">_ulFlags_</span></span>
  
> <span data-ttu-id="366c7-123">[in] Máscara de bits de las marcas usadas para indicar el modo de la función.</span><span class="sxs-lookup"><span data-stu-id="366c7-123">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="366c7-124">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="366c7-124">The following flags can be set:</span></span>
    
<span data-ttu-id="366c7-125">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="366c7-125">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="366c7-126">Todas las propiedades posibles se asignan a sus atributos de nivel inferior, pero cuando hay una posible pérdida de datos debido a la conversión a un atributo de nivel inferior, la propiedad también se codifica en las encapsulaciones.</span><span class="sxs-lookup"><span data-stu-id="366c7-126">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="366c7-127">Tenga en cuenta que esto provocará la duplicación de información en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="366c7-127">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="366c7-128">TNEF_BEST_DATA es el valor predeterminado si no se especifica ningún otro modo.</span><span class="sxs-lookup"><span data-stu-id="366c7-128">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="366c7-129">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="366c7-129">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="366c7-130">Proporciona compatibilidad con versiones anteriores con las aplicaciones cliente anteriores.</span><span class="sxs-lookup"><span data-stu-id="366c7-130">Provides backward compatibility with the older client applications.</span></span> <span data-ttu-id="366c7-131">Las secuencias TNEF codificadas con esta marca asignarán todas las propiedades posibles a su atributo de nivel inferior correspondiente.</span><span class="sxs-lookup"><span data-stu-id="366c7-131">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="366c7-132">Este modo también provoca la configuración predeterminada de algunas propiedades que requieren los clientes de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="366c7-132">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="366c7-133">Esta marca está obsoleta y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="366c7-133">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="366c7-134">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="366c7-134">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="366c7-135">El objeto TNEF de la secuencia indicada se abre con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="366c7-135">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="366c7-136">El proveedor de transporte debe establecer esta marca si desea que la función inicialice el objeto para la posterior decodificación.</span><span class="sxs-lookup"><span data-stu-id="366c7-136">The transport provider must set this flag if it wants the function to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="366c7-137">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="366c7-137">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="366c7-138">El objeto TNEF de la secuencia indicada se abre para el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="366c7-138">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="366c7-139">El proveedor de transporte debe establecer esta marca si desea que la función inicialice el objeto para la codificación posterior.</span><span class="sxs-lookup"><span data-stu-id="366c7-139">The transport provider must set this flag if it wants the function to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="366c7-140">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="366c7-140">TNEF_PURE</span></span> 
  
> <span data-ttu-id="366c7-141">Codifica todas las propiedades en los bloques de encapsulación MAPI.</span><span class="sxs-lookup"><span data-stu-id="366c7-141">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="366c7-142">Por lo tanto, un archivo TNEF "puro" constará, como máximo, de attMAPIProps, attAttachment, attRenddata y attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="366c7-142">Therefore, a "pure" TNEF file will consist of, at most, attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="366c7-143">Este modo es ideal para su uso cuando no se requiere compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="366c7-143">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="366c7-144">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="366c7-144">_lpMessage_</span></span>
  
> <span data-ttu-id="366c7-145">[in] Puntero a un objeto de mensaje como destino de un mensaje descodificado con datos adjuntos o un origen para un mensaje codificado con datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="366c7-145">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="366c7-146">Las propiedades de un mensaje codificado pueden sobrescribir las propiedades de un mensaje de destino.</span><span class="sxs-lookup"><span data-stu-id="366c7-146">Any properties of a destination message might be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="366c7-147">_wKey_</span><span class="sxs-lookup"><span data-stu-id="366c7-147">_wKey_</span></span>
  
> <span data-ttu-id="366c7-148">[in] Clave de búsqueda que el objeto TNEF usa para hacer coincidir datos adjuntos con las etiquetas de texto insertadas en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="366c7-148">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="366c7-149">Este valor debe ser relativamente único en todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="366c7-149">This value should be relatively unique across messages.</span></span>
    
<span data-ttu-id="366c7-150">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="366c7-150">_lppTNEF_</span></span>
  
> <span data-ttu-id="366c7-151">[salida] Puntero al nuevo objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="366c7-151">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="366c7-152">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="366c7-152">Return value</span></span>

<span data-ttu-id="366c7-153">S_OK</span><span class="sxs-lookup"><span data-stu-id="366c7-153">S_OK</span></span> 
  
> <span data-ttu-id="366c7-154">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="366c7-154">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="366c7-155">Comentarios</span><span class="sxs-lookup"><span data-stu-id="366c7-155">Remarks</span></span>

<span data-ttu-id="366c7-156">Posteriormente, un objeto TNEF creado por la función **OpenTnefStream** llama al método OLE **IUnknown::AddRef** para agregar referencias al objeto de soporte técnico, al objeto stream y al objeto message.</span><span class="sxs-lookup"><span data-stu-id="366c7-156">A TNEF object created by the **OpenTnefStream** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="366c7-157">El proveedor de transporte puede liberar las referencias de los tres objetos con una sola llamada al método OLE **IUnknown::Release** en el objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="366c7-157">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="366c7-158">**OpenTnefStream** asigna e inicializa una interfaz **ITnef** de objeto TNEF para que el proveedor la use en la codificación de una interfaz **IMessage** de mensaje MAPI en un mensaje de secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="366c7-158">**OpenTnefStream** allocates and initializes a TNEF object **ITnef** interface for the provider to use in encoding a MAPI message **IMessage** interface into a TNEF stream message.</span></span> <span data-ttu-id="366c7-159">Como alternativa, la función puede configurar el objeto para que el proveedor use en llamadas posteriores a [ITnef::ExtractProps](itnef-extractprops.md) para descodificar un mensaje de secuencia TNEF en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="366c7-159">Alternatively, the function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="366c7-160">Para liberar el objeto TNEF y cerrar la sesión, el proveedor de transporte debe llamar al método **IUnknown::Release** heredado en el objeto.</span><span class="sxs-lookup"><span data-stu-id="366c7-160">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="366c7-161">Esta función es el punto de entrada original para el acceso TNEF y se ha reemplazado por [OpenTnefStreamEx,](opentnefstreamex.md) pero se sigue usando para la compatibilidad de aquellos que ya usan TNEF.</span><span class="sxs-lookup"><span data-stu-id="366c7-161">This function is the original entry point for TNEF access and has been replaced by [OpenTnefStreamEx](opentnefstreamex.md) but is still used for compatibility for those already using TNEF.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="366c7-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="366c7-162">See also</span></span>

- [<span data-ttu-id="366c7-163">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="366c7-163">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="366c7-164">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="366c7-164">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)

