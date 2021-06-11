---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6bec29aa0e88e0224f9cd6049553f2df6379e23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430535"
---
# <a name="rtf_wcsinfo"></a><span data-ttu-id="48de3-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="48de3-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="48de3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48de3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48de3-105">Esta estructura permite especificar información para descomprimir el cuerpo de un mensaje en formato de texto enriquecido comprimido (RTF) y, opcionalmente, devolver la secuencia de cuerpo en su formato nativo.</span><span class="sxs-lookup"><span data-stu-id="48de3-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="48de3-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="48de3-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="48de3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="48de3-107">Members</span></span>

 <span data-ttu-id="48de3-108">_size_</span><span class="sxs-lookup"><span data-stu-id="48de3-108">_size_</span></span>
  
> <span data-ttu-id="48de3-109">El tamaño de la **RTF_WCSINFO** en número de bytes.</span><span class="sxs-lookup"><span data-stu-id="48de3-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="48de3-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="48de3-110">_ulFlags_</span></span>
  
> <span data-ttu-id="48de3-111">Esta es la máscara de bits de las marcas de opción para la [función WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="48de3-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="48de3-112">Las marcas de opción admitidas son:</span><span class="sxs-lookup"><span data-stu-id="48de3-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="48de3-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="48de3-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="48de3-114">Esto indica si el cliente tiene la intención de escribir la interfaz de secuencia ajustada que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="48de3-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="48de3-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="48de3-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="48de3-116">Esto indica si se supone que el RTF descomprimido debe escribirse en la secuencia a la que apunta el puntero _lpCompressedRTFStream_ de la función [WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="48de3-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="48de3-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="48de3-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="48de3-118">Esto indica si la secuencia descomprimida también se convierte en el cuerpo nativo antes de devolver la secuencia.</span><span class="sxs-lookup"><span data-stu-id="48de3-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="48de3-119">Esta marca no se puede combinar con **la MAPI_MODIFY** marca.</span><span class="sxs-lookup"><span data-stu-id="48de3-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="48de3-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="48de3-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="48de3-121">Este es el valor de la página de código del mensaje.</span><span class="sxs-lookup"><span data-stu-id="48de3-121">This is the code page value of the message.</span></span> <span data-ttu-id="48de3-122">Normalmente, este valor se obtiene de la propiedad canónica [PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="48de3-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="48de3-123">Este valor solo se usa cuando **la MAPI_NATIVE_BODY** se pasa en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="48de3-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="48de3-124">De lo contrario, este valor se omite.</span><span class="sxs-lookup"><span data-stu-id="48de3-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="48de3-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="48de3-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="48de3-126">Este es el valor de página de código de la secuencia descomprimida devuelta que desea.</span><span class="sxs-lookup"><span data-stu-id="48de3-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="48de3-127">Si se establece en un valor distinto de cero, la función [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) convierte la secuencia en la página de código especificada.</span><span class="sxs-lookup"><span data-stu-id="48de3-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="48de3-128">Si se establece en un valor cero, MAPI decide qué página de código usar.</span><span class="sxs-lookup"><span data-stu-id="48de3-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="48de3-129">Este valor solo se usa cuando **la marca MAPI_NATIVE_BODY** se pasa en  _ulFlags_ y el formato del cuerpo no es RTF.</span><span class="sxs-lookup"><span data-stu-id="48de3-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="48de3-130">De lo contrario, este valor se omite.</span><span class="sxs-lookup"><span data-stu-id="48de3-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48de3-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="48de3-131">See also</span></span>



[<span data-ttu-id="48de3-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="48de3-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

