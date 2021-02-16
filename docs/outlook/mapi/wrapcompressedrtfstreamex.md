---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325777"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="4ad04-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="4ad04-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="4ad04-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ad04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ad04-105">Descomprime el cuerpo de un mensaje de correo electrónico en formato de texto enriquecido (RTF) comprimido, indica el formato de la secuencia descomprimida, convierte opcionalmente la secuencia descomprimida a su formato nativo y devuelve la secuencia descomprimida o la secuencia nativa convertida.</span><span class="sxs-lookup"><span data-stu-id="4ad04-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4ad04-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="4ad04-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ad04-107">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="4ad04-107">Exported by:</span></span>  <br/> |<span data-ttu-id="4ad04-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="4ad04-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="4ad04-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4ad04-109">Called by:</span></span>  <br/> |<span data-ttu-id="4ad04-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="4ad04-110">Client</span></span>  <br/> |
|<span data-ttu-id="4ad04-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="4ad04-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="4ad04-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="4ad04-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="4ad04-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ad04-113">Parameters</span></span>

<span data-ttu-id="4ad04-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="4ad04-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="4ad04-115">[entrada] Se trata de un puntero a una secuencia que se abre en la propiedad canónica [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4ad04-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="4ad04-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="4ad04-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="4ad04-117">[entrada] Se trata de un puntero a un</span><span class="sxs-lookup"><span data-stu-id="4ad04-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="4ad04-118">[RTF_WCSINFO](rtf_wcsinfo.md) estructura que contiene opciones para la función.</span><span class="sxs-lookup"><span data-stu-id="4ad04-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="4ad04-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="4ad04-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="4ad04-120">[salida] Se trata de un puntero a la ubicación donde se devuelve una secuencia para el RTF descomprimido.</span><span class="sxs-lookup"><span data-stu-id="4ad04-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="4ad04-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="4ad04-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="4ad04-122">[salida] Se trata de un puntero a [una RTF_WCSRETINFO](rtf_wcsretinfo.md) que contiene información sobre el formato de la secuencia descomprimida devuelta.</span><span class="sxs-lookup"><span data-stu-id="4ad04-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="4ad04-123">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4ad04-123">Return values</span></span>

<span data-ttu-id="4ad04-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="4ad04-124">S_OK</span></span> 
  
- <span data-ttu-id="4ad04-125">La llamada a la función se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="4ad04-125">The function call is successful.</span></span>
    
<span data-ttu-id="4ad04-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4ad04-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="4ad04-127">Esto se devuelve si la marca **MAPI_NATIVE_BODY** se combina con la marca **MAPI_MODIFY** en el campo **ulFlags** de la estructura **RTF_WCSINFO** apuntada por  *pWCSInfo*  .</span><span class="sxs-lookup"><span data-stu-id="4ad04-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4ad04-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ad04-128">Remarks</span></span>

<span data-ttu-id="4ad04-129">**WrapCompressedRTFStreamEx** te permite acceder al cuerpo de un mensaje de correo electrónico encapsulado en RTF comprimido descomprimiendo la secuencia, devuelve la secuencia descomprimida y su formato y, opcionalmente, la secuencia de cuerpo nativo.</span><span class="sxs-lookup"><span data-stu-id="4ad04-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="4ad04-130">La secuencia de cuerpo nativo puede estar en RTF, texto sin formato o HTML.</span><span class="sxs-lookup"><span data-stu-id="4ad04-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="4ad04-131">El Microsoft Office Outlook de objetos proporciona una propiedad **Body** para objetos **MailItem** y una propiedad [MailItem.BodyFormat (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) que indica el formato del texto del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="4ad04-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="4ad04-132">Por diseño, una solución en la que Outlook no confía invoca cuadros de diálogo de seguridad generados por la Protección de seguridad de Outlook.</span><span class="sxs-lookup"><span data-stu-id="4ad04-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="4ad04-133">El uso de la función MAPI **exportada WrapCompressedRTFStreamEx** permite que una solución use MAPI en lugar del modelo de objetos de Outlook y evite estos cuadros de diálogo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4ad04-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="4ad04-134">Dado que la marca MAPI NATIVE_BODY no se puede combinar con la marca **MAPI \_ MODIFY** en el campo **ulFlags** de la estructura **RTF \_ WCSINFO** señalada por *pWCSInfo,* solo puede tener acceso **\_ a** la secuencia de cuerpo nativo en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4ad04-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="4ad04-135">Para obtener acceso a la secuencia de cuerpo nativo en modo de lectura y escritura, debes usar la **función WrapCompressedRTFStream.**</span><span class="sxs-lookup"><span data-stu-id="4ad04-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4ad04-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4ad04-136">See also</span></span>

- [<span data-ttu-id="4ad04-137">Recuperar el cuerpo de un mensaje en RTF comprimido y convertirlo a su formato nativo</span><span class="sxs-lookup"><span data-stu-id="4ad04-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

