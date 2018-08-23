---
title: OpenTnefStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStreamEx
api_type:
- COM
ms.assetid: eb84c408-2d8b-453b-92f4-5fd8851b84ca
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b651a913855e99e2f26dfd99fb725cc332201932
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565189"
---
# <a name="opentnefstreamex"></a><span data-ttu-id="e2cd2-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="e2cd2-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="e2cd2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2cd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2cd2-105">Crea un objeto de formato de encapsulación neutro para el transporte (TNEF) que se puede usar para codificar o descodificar un objeto de mensaje en una secuencia de datos TNEF para su uso por los transportes o puertas de enlace y los almacenes de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="e2cd2-106">Éste es el punto de entrada para el acceso de TNEF.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2cd2-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e2cd2-107">Header file:</span></span>  <br/> |<span data-ttu-id="e2cd2-108">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="e2cd2-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="e2cd2-109">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="e2cd2-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="e2cd2-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="e2cd2-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="e2cd2-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e2cd2-111">Called by:</span></span>  <br/> |<span data-ttu-id="e2cd2-112">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="e2cd2-112">Transport providers</span></span>  <br/> |
   
```cpp
HRESULT OpenTnefStreamEx(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName,
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKeyVal,
  LPADDRESSBOOK lpAddressBook,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a><span data-ttu-id="e2cd2-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2cd2-113">Parameters</span></span>

<span data-ttu-id="e2cd2-114">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="e2cd2-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="e2cd2-115">[entrada] Pasa un objeto de soporte técnico o pasa en NULL.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="e2cd2-116">Si es nulo, el parámetro _lpAddressBook_ debe ser distinto de null.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="e2cd2-117">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="e2cd2-117">_lpStream_</span></span>
  
> <span data-ttu-id="e2cd2-118">[entrada] Puntero a un objeto stream de almacenamiento, como una interfaz **IStream** OLE, que proporciona un origen o destino para un mensaje de secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="e2cd2-119">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="e2cd2-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="e2cd2-120">[entrada] Puntero en el nombre de la secuencia de datos que utiliza el objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="e2cd2-121">Si el autor de la llamada ha establecido el indicador TNEF_ENCODE (parámetro _ulFlags_ ) en su llamada a **OpenTnefStream**, el parámetro _lpszName_ debe especificar un puntero no nulo a una cadena no nula formada por los caracteres que se considere válidos para asignar nombres a un archivo.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="e2cd2-122">MAPI no admite nombres de cadena, incluidos los caracteres "[", "]", o ":", incluso si el sistema de archivos permite su uso.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="e2cd2-123">El tamaño de la cadena que se pasa para el parámetro _lpszName_ no debe superar el valor de MAX_PATH, la longitud máxima de una cadena que contiene un nombre de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="e2cd2-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e2cd2-124">_ulFlags_</span></span>
  
> <span data-ttu-id="e2cd2-125">[entrada] Máscara de bits de indicadores que se utilizan para indicar el modo de la función.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="e2cd2-126">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="e2cd2-126">The following flags can be set:</span></span>
    
<span data-ttu-id="e2cd2-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="e2cd2-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="e2cd2-128">Todas las propiedades posibles se asignan a sus atributos de nivel inferior, pero cuando hay una posible pérdida de datos debido a la conversión a un atributo de nivel inferior, la propiedad también se codifica en la encapsulaciones.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="e2cd2-129">Tenga en cuenta que esto hará que la duplicación de información en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="e2cd2-130">TNEF_BEST_DATA es el valor predeterminado si no se especifiquen ningún otros modos.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="e2cd2-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="e2cd2-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="e2cd2-132">Proporciona compatibilidad con versiones anteriores con aplicaciones de cliente anteriores.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="e2cd2-133">Secuencias TNEF codificadas con esta marca va a asignar todas las propiedades posibles en su atributo de nivel inferior correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="e2cd2-134">Este modo también hace que el valor predeterminado de algunas propiedades que necesitan los clientes de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="e2cd2-135">Esta marca está obsoleta y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="e2cd2-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="e2cd2-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="e2cd2-137">Se abre el objeto TNEF en la secuencia indicada con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="e2cd2-138">El proveedor de transporte debe establecer este indicador si la función es inicializar el objeto de descodificación subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="e2cd2-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="e2cd2-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="e2cd2-140">Se abre el objeto TNEF en la secuencia indicada para el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="e2cd2-141">El proveedor de transporte debe establecer este indicador si la función es inicializar el objeto de codificación subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="e2cd2-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="e2cd2-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="e2cd2-143">Codifica todas las propiedades en los bloques de encapsulación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="e2cd2-144">Por lo tanto, un archivo TNEF "puro" consistirá, como máximo, los atributos attMAPIProps, attAttachment, attRenddata y attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="e2cd2-145">Este modo es ideal para su uso cuando no hay compatibilidad con versiones anteriores se requiere.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="e2cd2-146">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="e2cd2-146">_lpMessage_</span></span>
  
> <span data-ttu-id="e2cd2-147">[entrada] Puntero a un objeto de mensaje como un destino para un mensaje descodificado con datos adjuntos o un origen de un mensaje codificado con datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="e2cd2-148">Las propiedades de un mensaje de destino se pueden sobrescribir con las propiedades de un mensaje codificado.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="e2cd2-149">_wKeyVal_</span><span class="sxs-lookup"><span data-stu-id="e2cd2-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="e2cd2-150">[entrada] Una clave de búsqueda que utiliza el objeto TNEF para que coincida con los datos adjuntos a las etiquetas de texto insertados en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="e2cd2-151">Este valor debe ser relativamente único a través de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="e2cd2-152">_lpAddressBook_</span><span class="sxs-lookup"><span data-stu-id="e2cd2-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="e2cd2-153">[entrada] Puntero a un objeto de la libreta de direcciones utilizado para obtener información de los identificadores de entrada de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="e2cd2-154">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="e2cd2-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="e2cd2-155">[out] Puntero al nuevo objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2cd2-156">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2cd2-156">Return value</span></span>

<span data-ttu-id="e2cd2-157">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2cd2-157">S_OK</span></span> 
  
> <span data-ttu-id="e2cd2-158">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2cd2-159">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2cd2-159">Remarks</span></span>

<span data-ttu-id="e2cd2-160">La función **OpenTnefStreamEx** es la sustitución recomendada para [OpenTnefStream](opentnefstream.md), el punto de entrada original para el acceso de TNEF.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="e2cd2-161">Un objeto TNEF creado por la función **OpenTnefStreamEx** más adelante, llama al método OLE **IUnknown:: AddRef** para agregar referencias para el objeto de soporte, el objeto stream y el objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="e2cd2-162">El proveedor de transporte puede liberar las referencias para todos los tres objetos con una sola llamada al método OLE **IUnknown:: Release** en el objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="e2cd2-163">**OpenTnefStreamEx** asigna e inicializa un objeto TNEF para el proveedor de uso en la codificación de un mensaje MAPI en un mensaje de secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="e2cd2-164">Como alternativa, esta función puede configurar el objeto para el proveedor de uso de las llamadas subsiguientes a [ITnef::ExtractProps](itnef-extractprops.md) para descodificar un mensaje de secuencia TNEF en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="e2cd2-165">Para liberar el objeto TNEF y cerrar la sesión, el proveedor de transporte debe llamar al método **IUnknown:: Release** heredado en el objeto.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="e2cd2-166">El valor de base para el parámetro _wKeyVal_ no debe ser cero y no debe ser el mismo para todas las llamadas a **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="e2cd2-167">En su lugar, utilice números aleatorios según la hora del sistema desde el generador de números aleatorios de la biblioteca de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e2cd2-168">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e2cd2-168">MFCMAPI reference</span></span>

<span data-ttu-id="e2cd2-169">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e2cd2-170">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="e2cd2-170">**File**</span></span>|<span data-ttu-id="e2cd2-171">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="e2cd2-171">**Function**</span></span>|<span data-ttu-id="e2cd2-172">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="e2cd2-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e2cd2-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="e2cd2-173">File.cpp</span></span>  <br/> |<span data-ttu-id="e2cd2-174">LoadFromTNEF</span><span class="sxs-lookup"><span data-stu-id="e2cd2-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="e2cd2-175">MFCMAPI usa el método **OpenTnefStreamEx** para abrir una secuencia en el archivo TNEF, por lo que se pueden extraer las propiedades.</span><span class="sxs-lookup"><span data-stu-id="e2cd2-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2cd2-176">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e2cd2-176">See also</span></span>

- [<span data-ttu-id="e2cd2-177">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2cd2-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="e2cd2-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="e2cd2-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="e2cd2-179">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="e2cd2-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

