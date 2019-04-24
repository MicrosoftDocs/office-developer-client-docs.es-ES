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
ms.openlocfilehash: 178ab67875d8fb442500dd412dbafe4403deee16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348576"
---
# <a name="opentnefstreamex"></a><span data-ttu-id="3f20f-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="3f20f-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="3f20f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f20f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f20f-105">Crea un objeto de formato de encapsulación neutro para el transporte (TNEF) que se puede usar para codificar o descodificar un objeto de mensaje en una secuencia de datos TNEF para su uso mediante transportes o puertas de enlace y almacenes de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3f20f-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="3f20f-106">Es el punto de entrada para el acceso TNEF.</span><span class="sxs-lookup"><span data-stu-id="3f20f-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f20f-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3f20f-107">Header file:</span></span>  <br/> |<span data-ttu-id="3f20f-108">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="3f20f-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="3f20f-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="3f20f-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="3f20f-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="3f20f-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="3f20f-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="3f20f-111">Called by:</span></span>  <br/> |<span data-ttu-id="3f20f-112">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="3f20f-112">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="3f20f-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="3f20f-113">Parameters</span></span>

<span data-ttu-id="3f20f-114">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="3f20f-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="3f20f-115">a Pasa un objeto de soporte o pasa NULL.</span><span class="sxs-lookup"><span data-stu-id="3f20f-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="3f20f-116">Si es NULL, el parámetro _lpAddressBook_ no debe ser null.</span><span class="sxs-lookup"><span data-stu-id="3f20f-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="3f20f-117">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="3f20f-117">_lpStream_</span></span>
  
> <span data-ttu-id="3f20f-118">a Puntero a un objeto de secuencia de almacenamiento, como una interfaz OLE **IStream** , que proporciona un origen o un destino para un mensaje de transmisión TNEF.</span><span class="sxs-lookup"><span data-stu-id="3f20f-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="3f20f-119">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="3f20f-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="3f20f-120">a Puntero al nombre de la secuencia de datos que usa el objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="3f20f-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="3f20f-121">Si el autor de la llamada ha establecido el indicador TNEF_ENCODE ( _ulFlags_ ) en su llamada a **OpenTnefStream**, el parámetro _lpszName_ debe especificar un puntero que no sea nulo a una cadena que no sea NULL y que consista en cualquier carácter que se considere válido para el nombre de un archivo.</span><span class="sxs-lookup"><span data-stu-id="3f20f-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="3f20f-122">MAPI no permite nombres de cadena que incluyan los caracteres "[", "]" o ":", incluso si el sistema de archivos permite su uso.</span><span class="sxs-lookup"><span data-stu-id="3f20f-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="3f20f-123">El tamaño de la cadena que se pasa para el parámetro _lpszName_ no debe superar el valor de MAX_PATH, es decir, la longitud máxima de una cadena que contiene un nombre de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="3f20f-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="3f20f-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3f20f-124">_ulFlags_</span></span>
  
> <span data-ttu-id="3f20f-125">a Máscara de las marcas usadas para indicar el modo de la función.</span><span class="sxs-lookup"><span data-stu-id="3f20f-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="3f20f-126">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="3f20f-126">The following flags can be set:</span></span>
    
<span data-ttu-id="3f20f-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="3f20f-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="3f20f-128">Todas las propiedades posibles se asignan a sus atributos de nivel inferior, pero cuando hay una posible pérdida de datos debido a la conversión a un atributo de nivel inferior, la propiedad también se codifica en las encapsulaciones.</span><span class="sxs-lookup"><span data-stu-id="3f20f-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="3f20f-129">Tenga en cuenta que esto hará que se duplique la información del flujo TNEF.</span><span class="sxs-lookup"><span data-stu-id="3f20f-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="3f20f-130">TNEF_BEST_DATA es el valor predeterminado si no se especifican otros modos.</span><span class="sxs-lookup"><span data-stu-id="3f20f-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="3f20f-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="3f20f-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="3f20f-132">Proporciona compatibilidad con versiones anteriores con aplicaciones cliente más antiguas.</span><span class="sxs-lookup"><span data-stu-id="3f20f-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="3f20f-133">Las secuencias TNEF codificadas con este indicador asignarán todas las propiedades posibles al atributo de bajo nivel correspondiente.</span><span class="sxs-lookup"><span data-stu-id="3f20f-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="3f20f-134">Este modo también hace que el valor predeterminado de algunas propiedades que los clientes de nivel inferior requieran.</span><span class="sxs-lookup"><span data-stu-id="3f20f-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="3f20f-135">Esta marca está obsoleta y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="3f20f-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="3f20f-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="3f20f-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="3f20f-137">El objeto TNEF en la secuencia indicada se abre con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3f20f-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="3f20f-138">El proveedor de transporte debe establecer esta marca si la función es inicializar el objeto para la descodificación subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="3f20f-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="3f20f-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="3f20f-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="3f20f-140">El objeto TNEF en la secuencia indicada se abre para permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3f20f-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="3f20f-141">El proveedor de transporte debe establecer esta marca si la función es inicializar el objeto para la codificación subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="3f20f-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="3f20f-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="3f20f-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="3f20f-143">Codifica todas las propiedades en los bloques de encapsulación MAPI.</span><span class="sxs-lookup"><span data-stu-id="3f20f-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="3f20f-144">Por lo tanto, un archivo TNEF "puro" constará de, como máximo, los atributos attMAPIProps, attAttachment, attRenddata y attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="3f20f-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="3f20f-145">Este modo es ideal para su uso cuando no se requiere compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3f20f-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="3f20f-146">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="3f20f-146">_lpMessage_</span></span>
  
> <span data-ttu-id="3f20f-147">a Puntero a un objeto de mensaje como destino para un mensaje descodificado con datos adjuntos o un origen para un mensaje codificado con datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="3f20f-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="3f20f-148">Las propiedades de un mensaje codificado pueden sobrescribir cualquier propiedad de un mensaje de destino.</span><span class="sxs-lookup"><span data-stu-id="3f20f-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="3f20f-149">_wKeyVal_</span><span class="sxs-lookup"><span data-stu-id="3f20f-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="3f20f-150">a Clave de búsqueda que el objeto TNEF utiliza para hacer coincidir los datos adjuntos con las etiquetas de texto insertadas en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="3f20f-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="3f20f-151">Este valor debe ser relativamente único en todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="3f20f-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="3f20f-152">_lpAddressBook_</span><span class="sxs-lookup"><span data-stu-id="3f20f-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="3f20f-153">a Puntero a un objeto de la libreta de direcciones usado para obtener información de dirección para los identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="3f20f-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="3f20f-154">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="3f20f-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="3f20f-155">contempla Puntero al nuevo objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="3f20f-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3f20f-156">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f20f-156">Return value</span></span>

<span data-ttu-id="3f20f-157">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f20f-157">S_OK</span></span> 
  
> <span data-ttu-id="3f20f-158">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="3f20f-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f20f-159">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f20f-159">Remarks</span></span>

<span data-ttu-id="3f20f-160">La función **OpenTnefStreamEx** es el reemplazo recomendado para [OpenTnefStream](opentnefstream.md), el punto de entrada original de acceso TNEF.</span><span class="sxs-lookup"><span data-stu-id="3f20f-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="3f20f-161">Posteriormente, un objeto TNEF creado por la función **OpenTnefStreamEx** llama al método OLE **IUnknown:: AddRef** para agregar referencias para el objeto support, el objeto Stream y el objeto Message.</span><span class="sxs-lookup"><span data-stu-id="3f20f-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="3f20f-162">El proveedor de transporte puede liberar las referencias de los tres objetos con una sola llamada al método OLE **IUnknown:: Release** en el objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="3f20f-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="3f20f-163">**OpenTnefStreamEx** asigna e inicializa un objeto TNEF para que lo use el proveedor al codificar un mensaje MAPI en un mensaje de transmisión TNEF.</span><span class="sxs-lookup"><span data-stu-id="3f20f-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="3f20f-164">Como alternativa, esta función puede configurar el objeto que el proveedor debe usar en las llamadas posteriores a [ITnef:: ExtractProps](itnef-extractprops.md) para descodificar un mensaje de transmisión TNEF en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="3f20f-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="3f20f-165">Para liberar el objeto TNEF y cerrar la sesión, el proveedor de transporte debe llamar al método **IUnknown:: Release** heredado en el objeto.</span><span class="sxs-lookup"><span data-stu-id="3f20f-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="3f20f-166">El valor base para el parámetro _wKeyVal_ no debe ser cero y no debe ser el mismo para todas las llamadas a **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="3f20f-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="3f20f-167">En su lugar, use números aleatorios basados en la hora del sistema desde el generador de números aleatorios de la biblioteca en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="3f20f-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3f20f-168">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3f20f-168">MFCMAPI reference</span></span>

<span data-ttu-id="3f20f-169">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="3f20f-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3f20f-170">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="3f20f-170">**File**</span></span>|<span data-ttu-id="3f20f-171">**Función**</span><span class="sxs-lookup"><span data-stu-id="3f20f-171">**Function**</span></span>|<span data-ttu-id="3f20f-172">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="3f20f-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3f20f-173">Archivo. cpp</span><span class="sxs-lookup"><span data-stu-id="3f20f-173">File.cpp</span></span>  <br/> |<span data-ttu-id="3f20f-174">LoadFromTNEF</span><span class="sxs-lookup"><span data-stu-id="3f20f-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="3f20f-175">MFCMAPI usa el método **OpenTnefStreamEx** para abrir una secuencia en el archivo TNEF para que se puedan extraer propiedades.</span><span class="sxs-lookup"><span data-stu-id="3f20f-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f20f-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f20f-176">See also</span></span>

- [<span data-ttu-id="3f20f-177">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f20f-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="3f20f-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="3f20f-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="3f20f-179">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="3f20f-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

