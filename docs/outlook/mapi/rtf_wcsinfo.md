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
# <a name="rtfwcsinfo"></a><span data-ttu-id="cd15f-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="cd15f-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="cd15f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd15f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd15f-105">Esta estructura permite especificar la información para descomprimir el cuerpo de un mensaje en formato comprimido de texto enriquecido (RTF) y, opcionalmente, devolver el flujo del cuerpo en su formato nativo.</span><span class="sxs-lookup"><span data-stu-id="cd15f-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cd15f-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="cd15f-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="cd15f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd15f-107">Members</span></span>

 <span data-ttu-id="cd15f-108">_size_</span><span class="sxs-lookup"><span data-stu-id="cd15f-108">_size_</span></span>
  
> <span data-ttu-id="cd15f-109">El tamaño de la estructura **RTF_WCSINFO** en número de bytes.</span><span class="sxs-lookup"><span data-stu-id="cd15f-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="cd15f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cd15f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="cd15f-111">Es la máscara de las marcas de opción para la función [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="cd15f-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="cd15f-112">Los indicadores de opción admitidos son:</span><span class="sxs-lookup"><span data-stu-id="cd15f-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="cd15f-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="cd15f-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="cd15f-114">Indica si el cliente pretende escribir la interfaz de secuencia ajustada que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="cd15f-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="cd15f-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="cd15f-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="cd15f-116">Esto indica si se supone que el RTF descomprimido debe escribirse en la secuencia a la que apunta el puntero _lpCompressedRTFStream_ de la función [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="cd15f-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="cd15f-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="cd15f-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="cd15f-118">Esto indica si la secuencia descomprimida también se convierte en el cuerpo nativo antes de devolver la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cd15f-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="cd15f-119">Esta marca no se puede combinar con la marca **MAPI_MODIFY** .</span><span class="sxs-lookup"><span data-stu-id="cd15f-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="cd15f-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="cd15f-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="cd15f-121">Este es el valor de la página de códigos del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cd15f-121">This is the code page value of the message.</span></span> <span data-ttu-id="cd15f-122">Normalmente, este valor se obtiene de la [propiedad canónica PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cd15f-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="cd15f-123">Este valor solo se usa cuando se pasa la marca **MAPI_NATIVE_BODY** en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="cd15f-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="cd15f-124">De lo contrario, este valor se omite.</span><span class="sxs-lookup"><span data-stu-id="cd15f-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="cd15f-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="cd15f-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="cd15f-126">Este es el valor de la página de códigos del flujo descomprimido devuelto que desea.</span><span class="sxs-lookup"><span data-stu-id="cd15f-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="cd15f-127">Si se establece en un valor distinto de cero, la función [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) convierte la secuencia en la página de códigos especificada.</span><span class="sxs-lookup"><span data-stu-id="cd15f-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="cd15f-128">Si se establece en un valor de cero, MAPI decide la página de códigos que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="cd15f-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="cd15f-129">Este valor solo se usa cuando la marca **MAPI_NATIVE_BODY** se pasa en _ulFlags_y el formato del cuerpo no es RTF.</span><span class="sxs-lookup"><span data-stu-id="cd15f-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="cd15f-130">De lo contrario, este valor se omite.</span><span class="sxs-lookup"><span data-stu-id="cd15f-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd15f-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="cd15f-131">See also</span></span>



[<span data-ttu-id="cd15f-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="cd15f-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

