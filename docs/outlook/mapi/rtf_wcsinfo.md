---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c328e79b7e474369f11f8a4002e00137659db3c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820560"
---
# <a name="rtfwcsinfo"></a><span data-ttu-id="e4f50-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="e4f50-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="e4f50-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4f50-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4f50-105">Esta estructura permite especificar información para descomprimir el cuerpo de un mensaje en el formato comprimido de texto enriquecido (RTF) y, opcionalmente, devuelva la secuencia de cuerpo en su formato nativo.</span><span class="sxs-lookup"><span data-stu-id="e4f50-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e4f50-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="e4f50-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="e4f50-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e4f50-107">Members</span></span>

 <span data-ttu-id="e4f50-108">_tamaño_</span><span class="sxs-lookup"><span data-stu-id="e4f50-108">_size_</span></span>
  
> <span data-ttu-id="e4f50-109">El tamaño de la estructura **RTF_WCSINFO** en número de bytes.</span><span class="sxs-lookup"><span data-stu-id="e4f50-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="e4f50-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e4f50-110">_ulFlags_</span></span>
  
> <span data-ttu-id="e4f50-111">Esto es la máscara de bits de indicadores de opción para la función [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f50-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="e4f50-112">Los indicadores de opción compatibles son:</span><span class="sxs-lookup"><span data-stu-id="e4f50-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="e4f50-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="e4f50-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="e4f50-114">Esto indica si el cliente intenta crear una interfaz de la secuencia ajustada que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="e4f50-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="e4f50-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="e4f50-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="e4f50-116">Esto indica si se supone que el RTF descomprimido se escriben en la secuencia que señala el puntero _lpCompressedRTFStream_ de la función [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f50-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="e4f50-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="e4f50-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="e4f50-118">Esto indica si la secuencia descomprimida también se convierte en el cuerpo nativo antes de devolver la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e4f50-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="e4f50-119">Esta marca no se puede combinar con la marca **MAPI_MODIFY** .</span><span class="sxs-lookup"><span data-stu-id="e4f50-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="e4f50-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="e4f50-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="e4f50-121">Éste es el valor de la página de código del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4f50-121">This is the code page value of the message.</span></span> <span data-ttu-id="e4f50-122">Normalmente, este valor se obtiene de la [Propiedad canónico PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4f50-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="e4f50-123">Este valor sólo se utiliza cuando se pasa el indicador **MAPI_NATIVE_BODY** en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="e4f50-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="e4f50-124">De lo contrario, se omite este valor.</span><span class="sxs-lookup"><span data-stu-id="e4f50-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="e4f50-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="e4f50-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="e4f50-126">Éste es el valor de la página de código de la secuencia devuelta descomprimido que desee.</span><span class="sxs-lookup"><span data-stu-id="e4f50-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="e4f50-127">Si se establece en un valor distinto de cero, la función [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) convierte la secuencia a la página de código especificado.</span><span class="sxs-lookup"><span data-stu-id="e4f50-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="e4f50-128">Si se establece en un valor de cero, MAPI decide qué página de códigos para usar.</span><span class="sxs-lookup"><span data-stu-id="e4f50-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="e4f50-129">Este valor solo se usa cuando se pasa el indicador **MAPI_NATIVE_BODY** en _ulFlags_y el formato del cuerpo no es RTF.</span><span class="sxs-lookup"><span data-stu-id="e4f50-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="e4f50-130">De lo contrario, se omite este valor.</span><span class="sxs-lookup"><span data-stu-id="e4f50-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e4f50-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="e4f50-131">See also</span></span>



[<span data-ttu-id="e4f50-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="e4f50-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

