---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 3a38a4604230c0aa3f5b0d104ae3b838f544b31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820542"
---
# <a name="rtfwcsretinfo"></a><span data-ttu-id="c50bd-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="c50bd-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="c50bd-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c50bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c50bd-105">Esta estructura proporciona información acerca de una secuencia en formato nativo devuelto desde descomprimir el cuerpo de un mensaje que se encapsula en el formato comprimido de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="c50bd-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c50bd-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c50bd-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="c50bd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c50bd-107">Members</span></span>

<span data-ttu-id="c50bd-108">_tamaño_</span><span class="sxs-lookup"><span data-stu-id="c50bd-108">_size_</span></span>
  
> <span data-ttu-id="c50bd-109">El tamaño de la estructura **RTF_WCSRETINFO** en número de bytes.</span><span class="sxs-lookup"><span data-stu-id="c50bd-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="c50bd-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="c50bd-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="c50bd-111">Esto es un valor que indica el formato del cuerpo nativo.</span><span class="sxs-lookup"><span data-stu-id="c50bd-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="c50bd-112">Este valor sólo es válida si el indicador **MAPI_NATIVE_BODY** se pasa en el parámetro _ulFlags_ de la estructura [RTF_WCSINFO](rtf_wcsinfo.md) que se pasa a la función [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="c50bd-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="c50bd-113">Esto puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="c50bd-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="c50bd-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="c50bd-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="c50bd-115">Este valor solo se usa si _ulFlags_ incluye la marca **MAPI_NATIVE_BODY** , y el cuerpo es RTF.</span><span class="sxs-lookup"><span data-stu-id="c50bd-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="c50bd-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="c50bd-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="c50bd-117">Este valor solo se usa si _ulFlags_ incluye la marca **MAPI_NATIVE_BODY** , y el cuerpo tiene formato de texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="c50bd-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="c50bd-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="c50bd-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="c50bd-119">Este valor solo se usa si _ulFlags_ incluye la marca **MAPI_NATIVE_BODY** , y el cuerpo tiene formato de lenguaje de marcado de hipertexto (HTML).</span><span class="sxs-lookup"><span data-stu-id="c50bd-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c50bd-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="c50bd-120">See also</span></span>

- [<span data-ttu-id="c50bd-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="c50bd-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

