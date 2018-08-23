---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 14964f367e3dbca484c4e1612b374a6a72ddf17b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593784"
---
# <a name="itnefopentaggedbody"></a><span data-ttu-id="d7c0a-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="d7c0a-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="d7c0a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7c0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7c0a-105">Se abre una interfaz de secuencia en el texto de un mensaje de encapsulado.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="d7c0a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7c0a-106">Parameters</span></span>

 <span data-ttu-id="d7c0a-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="d7c0a-107">_lpMessage_</span></span>
  
> <span data-ttu-id="d7c0a-108">[entrada] Un puntero al mensaje que está asociado el objeto stream.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="d7c0a-109">Este mensaje no es necesario que sea el mismo mensaje que se pasa en la llamada a la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="d7c0a-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="d7c0a-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7c0a-110">_ulFlags_</span></span>
  
> <span data-ttu-id="d7c0a-111">[entrada] Una máscara de bits de indicadores que controla cómo se abre la interfaz de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="d7c0a-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d7c0a-112">The following flags can be set:</span></span>
    
<span data-ttu-id="d7c0a-113">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="d7c0a-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="d7c0a-114">Si una propiedad no existe en el mensaje actual, se debe crear.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="d7c0a-115">Si la propiedad existe, se deben reemplazar los datos actuales de la propiedad con los datos de la secuencia de formato de encapsulación neutro para el transporte (TNEF).</span><span class="sxs-lookup"><span data-stu-id="d7c0a-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="d7c0a-116">Cuando una implementación establece la marca MAPI_CREATE, también debe establecer la marca MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="d7c0a-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d7c0a-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="d7c0a-118">Las solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-118">Requests read/write permission.</span></span> <span data-ttu-id="d7c0a-119">La interfaz predeterminada es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-119">The default interface is read-only.</span></span> <span data-ttu-id="d7c0a-120">MAPI_MODIFY se debe establecer siempre que se establezca MAPI_CREATE.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="d7c0a-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="d7c0a-121">_lppStream_</span></span>
  
> <span data-ttu-id="d7c0a-122">[out] Un puntero a un puntero a un objeto stream que contiene el texto de la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) de en el pasado encapsula el mensaje y admita la interfaz [IStream](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="d7c0a-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d7c0a-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7c0a-123">Return value</span></span>

<span data-ttu-id="d7c0a-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7c0a-124">S_OK</span></span> 
  
> <span data-ttu-id="d7c0a-125">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7c0a-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7c0a-126">Remarks</span></span>

<span data-ttu-id="d7c0a-127">Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::OpenTaggedBody** para abrir una interfaz de secuencia en el texto de un mensaje de encapsulado (es decir, en un TNEF de objetos).</span><span class="sxs-lookup"><span data-stu-id="d7c0a-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="d7c0a-128">Como parte de su procesamiento, **OpenTaggedBody** inserta o analiza las etiquetas de datos adjuntos que indican la posición de los datos adjuntos o los objetos OLE en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="d7c0a-129">Las etiquetas de datos adjuntos se encuentran en el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="d7c0a-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="d7c0a-130">**[[** _nombre de datos adjuntos_ **:** _n_ **en** _nombre del contenedor de datos adjuntos_ **]]**</span><span class="sxs-lookup"><span data-stu-id="d7c0a-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="d7c0a-131">_nombre de datos adjuntos_ se describe el objeto de datos adjuntos;  _n_ es un número que identifica los datos adjuntos que forma parte de una secuencia, incremento desde el valor que se pasa en el parámetro _lpKey_ del [OpenTnefStream](opentnefstream.md) o la función de [OpenTnefStreamEx](opentnefstreamex.md) ; y _el nombre del contenedor de datos adjuntos_ se describe el componente físico donde reside el objeto de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="d7c0a-132">**OpenTaggedBody** lee el texto del mensaje y se inserta una etiqueta de datos adjuntos siempre que sea un objeto attachment aparecía originalmente en el texto.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="d7c0a-133">No se cambia el texto del mensaje original.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="d7c0a-134">Cuando un mensaje que tiene etiquetas se pasa a una secuencia, se eliminan las etiquetas y los objetos de datos adjuntos se reubican en la posición de las etiquetas en el objeto stream.</span><span class="sxs-lookup"><span data-stu-id="d7c0a-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7c0a-135">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d7c0a-135">See also</span></span>



[<span data-ttu-id="d7c0a-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="d7c0a-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="d7c0a-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="d7c0a-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="d7c0a-138">Propiedad canónica PidTagBody</span><span class="sxs-lookup"><span data-stu-id="d7c0a-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="d7c0a-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d7c0a-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

