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
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348737"
---
# <a name="itnefopentaggedbody"></a><span data-ttu-id="b02e4-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="b02e4-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="b02e4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b02e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b02e4-105">Abre una interfaz de secuencia en el texto de un mensaje encapsulado.</span><span class="sxs-lookup"><span data-stu-id="b02e4-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="b02e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b02e4-106">Parameters</span></span>

 <span data-ttu-id="b02e4-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="b02e4-107">_lpMessage_</span></span>
  
> <span data-ttu-id="b02e4-108">[entrada] Puntero al mensaje al que está asociada la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b02e4-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="b02e4-109">No es necesario que este mensaje sea el mismo que se pasa en la llamada a la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="b02e4-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="b02e4-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b02e4-110">_ulFlags_</span></span>
  
> <span data-ttu-id="b02e4-111">[entrada] Máscara de bits de marcas que controla cómo se abre la interfaz de secuencia.</span><span class="sxs-lookup"><span data-stu-id="b02e4-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="b02e4-112">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="b02e4-112">The following flags can be set:</span></span>
    
<span data-ttu-id="b02e4-113">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="b02e4-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="b02e4-114">Si una propiedad no existe en el mensaje actual, debe crearse.</span><span class="sxs-lookup"><span data-stu-id="b02e4-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="b02e4-115">Si la propiedad existe, los datos actuales de la propiedad deben reemplazarse por los datos de la secuencia Transport-Neutral de formato de encapsulamiento (TNEF).</span><span class="sxs-lookup"><span data-stu-id="b02e4-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="b02e4-116">Cuando una implementación establece la MAPI_CREATE, también debe establecer la MAPI_MODIFY personalizada.</span><span class="sxs-lookup"><span data-stu-id="b02e4-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="b02e4-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b02e4-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="b02e4-118">Solicita permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b02e4-118">Requests read/write permission.</span></span> <span data-ttu-id="b02e4-119">La interfaz predeterminada es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b02e4-119">The default interface is read-only.</span></span> <span data-ttu-id="b02e4-120">MAPI_MODIFY se debe establecer siempre que MAPI_CREATE se establezca.</span><span class="sxs-lookup"><span data-stu-id="b02e4-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="b02e4-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="b02e4-121">_lppStream_</span></span>
  
> <span data-ttu-id="b02e4-122">[salida] Puntero a un puntero a un objeto de secuencia que contiene el texto de la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) del mensaje encapsulado pasado y que admite la interfaz [IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream)</span><span class="sxs-lookup"><span data-stu-id="b02e4-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b02e4-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b02e4-123">Return value</span></span>

<span data-ttu-id="b02e4-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="b02e4-124">S_OK</span></span> 
  
> <span data-ttu-id="b02e4-125">La llamada se realiza correctamente y devuelve el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="b02e4-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b02e4-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b02e4-126">Remarks</span></span>

<span data-ttu-id="b02e4-127">Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::OpenTaggedBody** para abrir una interfaz de secuencia en el texto de un mensaje encapsulado (es decir, en un objeto TNEF).</span><span class="sxs-lookup"><span data-stu-id="b02e4-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="b02e4-128">Como parte de su procesamiento, **OpenTaggedBody** inserta o analiza etiquetas de datos adjuntos que indican la posición de los datos adjuntos u objetos OLE en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b02e4-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="b02e4-129">Las etiquetas de datos adjuntos tienen el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="b02e4-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="b02e4-130">**[[** _attachment name_ **:** _n_ **in** attachment container _name_ **]]**</span><span class="sxs-lookup"><span data-stu-id="b02e4-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="b02e4-131">_el nombre de los_ datos adjuntos describe el objeto attachment;  _n_ es un número que identifica los datos adjuntos que forman parte de una secuencia, incrementándose a partir del valor pasado en el parámetro  _lpKey_ de la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx;](opentnefstreamex.md) y  _el nombre del contenedor de_ datos adjuntos describe el componente físico donde reside el objeto de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b02e4-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="b02e4-132">**OpenTaggedBody** lee el texto del mensaje e inserta una etiqueta de datos adjuntos siempre que un objeto de datos adjuntos aparecía originalmente en el texto.</span><span class="sxs-lookup"><span data-stu-id="b02e4-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="b02e4-133">No se cambia el texto original del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b02e4-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="b02e4-134">Cuando se pasa un mensaje con etiquetas a una secuencia, las etiquetas se quitan y los objetos adjuntos se reubican en la posición de las etiquetas en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b02e4-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b02e4-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b02e4-135">See also</span></span>



[<span data-ttu-id="b02e4-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="b02e4-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="b02e4-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="b02e4-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="b02e4-138">PidTagBody (propiedad canónica)</span><span class="sxs-lookup"><span data-stu-id="b02e4-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="b02e4-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b02e4-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

