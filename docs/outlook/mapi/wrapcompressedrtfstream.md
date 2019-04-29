---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 710e0e2fc334194e33c6d8ba1296e4c7b1938bc0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439803"
---
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="f79ec-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="f79ec-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="f79ec-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f79ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f79ec-105">Crea una secuencia de texto en formato de texto enriquecido (RTF) no comprimido a partir del formato comprimido usado en la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f79ec-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f79ec-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f79ec-106">Header file:</span></span>  <br/> |<span data-ttu-id="f79ec-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f79ec-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f79ec-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f79ec-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f79ec-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f79ec-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f79ec-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f79ec-110">Called by:</span></span>  <br/> |<span data-ttu-id="f79ec-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="f79ec-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="f79ec-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="f79ec-112">Parameters</span></span>

 <span data-ttu-id="f79ec-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="f79ec-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="f79ec-114">a Puntero a una secuencia abierta en la propiedad PR_RTF_COMPRESSED de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f79ec-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="f79ec-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f79ec-115">_ulFlags_</span></span>
  
> <span data-ttu-id="f79ec-116">a Máscara de máscara de las marcas de opción para la función.</span><span class="sxs-lookup"><span data-stu-id="f79ec-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="f79ec-117">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="f79ec-117">The following flags can be set:</span></span>
    
<span data-ttu-id="f79ec-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f79ec-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="f79ec-119">Si el cliente pretende leer o escribir la interfaz de secuencia ajustada que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="f79ec-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="f79ec-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="f79ec-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="f79ec-121">El formato RTF sin comprimir debe escribirse en la secuencia a la que apunta _lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="f79ec-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="f79ec-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="f79ec-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="f79ec-123">contempla Puntero a la ubicación donde **WrapCompressedRTFStream** devuelve una secuencia para el RTF descomprimido.</span><span class="sxs-lookup"><span data-stu-id="f79ec-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f79ec-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f79ec-124">Return value</span></span>

<span data-ttu-id="f79ec-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="f79ec-125">S_OK</span></span> 
  
> <span data-ttu-id="f79ec-126">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="f79ec-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f79ec-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f79ec-127">Remarks</span></span>

<span data-ttu-id="f79ec-128">Si la marca MAPI_MODIFY se pasa en el parámetro _ulFlags_ , el parámetro _lpCompressedRTFStream_ debe estar ya abierto para lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f79ec-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="f79ec-129">Nuevo texto RTF sin comprimir se debe escribir en la interfaz de secuencia devuelta en _lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="f79ec-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="f79ec-130">Dado que no es posible anexar la secuencia existente, se debe escribir todo el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f79ec-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="f79ec-131">Si se pasa cero en el parámetro _ulFlags_ , _lpCompressedRTFStream_ puede abrirse en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f79ec-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="f79ec-132">Solo se puede leer todo el texto del mensaje de la interfaz de secuencia devuelta en _lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="f79ec-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="f79ec-133">No se puede iniciar la búsqueda a partir de la mitad de la transmisión.</span><span class="sxs-lookup"><span data-stu-id="f79ec-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="f79ec-134">**WrapCompressedRTFStream** presupone que el puntero de la secuencia comprimida se establece en el principio de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f79ec-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="f79ec-135">Algunos métodos de OLE **IStream** no son compatibles con la secuencia descomprimida devuelta.</span><span class="sxs-lookup"><span data-stu-id="f79ec-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="f79ec-136">Entre estos se incluyen **IStream:: Clone**, **IStream:: LockRegion**, **IStream:: Revert**, **IStream:: Seek**, **IStream:: setSize**, **IStream:: Stat**y **IStream:: UnlockRegion**.</span><span class="sxs-lookup"><span data-stu-id="f79ec-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="f79ec-137">Para copiar en toda la secuencia, se necesita un bucle de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f79ec-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="f79ec-138">Debido a que el cliente escribe RTF nuevos en formato sin comprimir, debe usar **WrapCompressedRTFStream**, en lugar de escribir directamente en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f79ec-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="f79ec-139">Los clientes compatibles con RTF deben buscar la marca STORE_UNCOMPRESSED_RTF en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) y pasarla a **WrapCompressed RTFStream** si está establecida.</span><span class="sxs-lookup"><span data-stu-id="f79ec-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f79ec-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="f79ec-140">See also</span></span>



[<span data-ttu-id="f79ec-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="f79ec-141">RTFSync</span></span>](rtfsync.md)

