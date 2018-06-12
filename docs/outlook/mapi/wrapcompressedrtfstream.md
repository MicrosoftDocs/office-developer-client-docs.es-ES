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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9025bcebdd5e656070b31cd82e6519166a3e3791
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821004"
---
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="460bd-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="460bd-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="460bd-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="460bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="460bd-105">Crea un objeto stream de texto en formato de texto de sin comprimir enriquecido (RTF) desde el formato comprimido utilizado en la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="460bd-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="460bd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="460bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="460bd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="460bd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="460bd-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="460bd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="460bd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="460bd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="460bd-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="460bd-110">Called by:</span></span>  <br/> |<span data-ttu-id="460bd-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="460bd-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="460bd-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="460bd-112">Parameters</span></span>

 <span data-ttu-id="460bd-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="460bd-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="460bd-114">[entrada] Puntero a un objeto stream abierto en la propiedad PR_RTF_COMPRESSED de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="460bd-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="460bd-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="460bd-115">_ulFlags_</span></span>
  
> <span data-ttu-id="460bd-116">[entrada] Máscara de bits de indicadores de opción para la función.</span><span class="sxs-lookup"><span data-stu-id="460bd-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="460bd-117">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="460bd-117">The following flags can be set:</span></span>
    
<span data-ttu-id="460bd-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="460bd-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="460bd-119">Si el cliente tiene la intención de lectura o escritura de la interfaz de secuencia ajustada que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="460bd-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="460bd-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="460bd-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="460bd-121">RTF sin comprimir debe escribirse en la secuencia indicada por _lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="460bd-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="460bd-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="460bd-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="460bd-123">[out] Puntero a la ubicación donde **WrapCompressedRTFStream** devuelve una secuencia para el RTF sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="460bd-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="460bd-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="460bd-124">Return value</span></span>

<span data-ttu-id="460bd-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="460bd-125">S_OK</span></span> 
  
> <span data-ttu-id="460bd-126">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="460bd-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="460bd-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="460bd-127">Remarks</span></span>

<span data-ttu-id="460bd-128">Si la marca MAPI_MODIFY se pasa en el parámetro _ulFlags_ , el parámetro _lpCompressedRTFStream_ ya debe estar abierto para lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="460bd-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="460bd-129">Nuevo, sin comprimir texto RTF debe escribirse en la interfaz de la secuencia devuelta en _lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="460bd-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="460bd-130">Debido a que no es posible que se anexará la secuencia existente, debe escribir el texto de mensaje completo.</span><span class="sxs-lookup"><span data-stu-id="460bd-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="460bd-131">Si se pasa cero en el parámetro _ulFlags_ , a continuación, _lpCompressedRTFStream_ se puede abrir como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="460bd-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="460bd-132">Sólo el texto de mensaje completo se puede leer fuera de la interfaz de la secuencia devuelta en _lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="460bd-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="460bd-133">No es posible iniciar la mitad de la secuencia de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="460bd-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="460bd-134">**WrapCompressedRTFStream** se da por supuesto que el puntero de comprimido de la secuencia se establece en el principio de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="460bd-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="460bd-135">Algunos métodos de **IStream** OLE no son compatibles con la secuencia devuelta sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="460bd-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="460bd-136">Esto incluye **sobre IStream:: Clone**, **IStream:: LockRegion**, **IStream:: Revert**, **IStream:: Seek**, **IStream:: SetSize**, **IStream:: Stat**e **IStream:: UnlockRegion**.</span><span class="sxs-lookup"><span data-stu-id="460bd-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="460bd-137">Para poder copiar a toda la secuencia, se necesita un bucle de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="460bd-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="460bd-138">Debido a que el cliente escribe RTF nuevo en formato sin comprimir, que debe usar **WrapCompressedRTFStream**, en lugar de escribir directamente en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="460bd-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="460bd-139">Los clientes de tener en cuenta RTF deben buscar el indicador STORE_UNCOMPRESSED_RTF en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) y pase al **WrapCompressed RTFStream** si se establece.</span><span class="sxs-lookup"><span data-stu-id="460bd-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="460bd-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="460bd-140">See also</span></span>



[<span data-ttu-id="460bd-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="460bd-141">RTFSync</span></span>](rtfsync.md)

