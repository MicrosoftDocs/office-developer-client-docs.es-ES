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
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="0feed-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="0feed-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="0feed-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0feed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0feed-105">Crea una secuencia de texto en formato de texto enriquecido (RTF) sin comprimir a partir del formato comprimido usado en la **propiedad PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0feed-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0feed-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0feed-106">Header file:</span></span>  <br/> |<span data-ttu-id="0feed-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0feed-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0feed-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="0feed-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0feed-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0feed-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0feed-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="0feed-110">Called by:</span></span>  <br/> |<span data-ttu-id="0feed-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="0feed-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="0feed-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0feed-112">Parameters</span></span>

 <span data-ttu-id="0feed-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="0feed-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="0feed-114">[entrada] Puntero a una secuencia abierta en la PR_RTF_COMPRESSED propiedad de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="0feed-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="0feed-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0feed-115">_ulFlags_</span></span>
  
> <span data-ttu-id="0feed-116">[entrada] Máscara de bits de marcas de opción para la función.</span><span class="sxs-lookup"><span data-stu-id="0feed-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="0feed-117">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="0feed-117">The following flags can be set:</span></span>
    
<span data-ttu-id="0feed-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0feed-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="0feed-119">Indica si el cliente tiene la intención de leer o escribir la interfaz de secuencia ajustada que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="0feed-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="0feed-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="0feed-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="0feed-121">Rtf sin comprimir debe escribirse en la secuencia a la que  _apunta lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="0feed-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="0feed-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="0feed-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="0feed-123">[salida] Puntero a la ubicación donde **WrapCompressedRTFStream** devuelve una secuencia para el RTF sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="0feed-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0feed-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0feed-124">Return value</span></span>

<span data-ttu-id="0feed-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="0feed-125">S_OK</span></span> 
  
> <span data-ttu-id="0feed-126">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="0feed-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0feed-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0feed-127">Remarks</span></span>

<span data-ttu-id="0feed-128">Si la MAPI_MODIFY se pasa en el parámetro  _ulFlags,_ el parámetro  _lpCompressedRTFStream_ ya debe estar abierto para lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0feed-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="0feed-129">El texto RTF nuevo y sin comprimir debe escribirse en la interfaz de secuencia devuelta  _en lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="0feed-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="0feed-130">Dado que no es posible anexar la secuencia existente, se debe escribir todo el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="0feed-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="0feed-131">Si se pasa cero en el  _parámetro ulFlags,_ es posible que  _lpCompressedRTFStream_ se abra como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0feed-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="0feed-132">Solo se puede leer todo el texto del mensaje de la interfaz de secuencia devuelta  _en lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="0feed-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="0feed-133">No es posible buscar empezando en medio de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0feed-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="0feed-134">**WrapCompressedRTFStream** supone que el puntero de la secuencia comprimida está establecido al principio de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0feed-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="0feed-135">Algunos métodos **OLE IStream** no son compatibles con la secuencia sin comprimir devuelta.</span><span class="sxs-lookup"><span data-stu-id="0feed-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="0feed-136">Estos incluyen **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat** e **IStream::UnlockRegion**.</span><span class="sxs-lookup"><span data-stu-id="0feed-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="0feed-137">Para copiar a toda la secuencia, se necesita un bucle de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0feed-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="0feed-138">Dado que el cliente escribe nuevo RTF en formato sin comprimir, debe usar **WrapCompressedRTFStream**, en lugar de escribir directamente en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0feed-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="0feed-139">Los clientes compatibles con RTF deben buscar la marca STORE_UNCOMPRESSED_RTF en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) y pasarla a **WrapCompressed RTFStream** si está establecida.</span><span class="sxs-lookup"><span data-stu-id="0feed-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0feed-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0feed-140">See also</span></span>



[<span data-ttu-id="0feed-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="0feed-141">RTFSync</span></span>](rtfsync.md)

