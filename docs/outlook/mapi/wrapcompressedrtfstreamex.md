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
ms.openlocfilehash: 4b7e59c9ffccb2e063962b2cc4947b4fa54757bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572721"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="fc41e-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="fc41e-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="fc41e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc41e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc41e-105">Descomprime el el cuerpo de un mensaje de correo electrónico que está en comprimido con formato (RTF), indica el formato de la secuencia descomprimido, de forma opcional convierte la secuencia descomprimida en su formato nativo y devuelve la secuencia de descomprimido o la convertir la secuencia nativo.</span><span class="sxs-lookup"><span data-stu-id="fc41e-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fc41e-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="fc41e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc41e-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="fc41e-107">Exported by:</span></span>  <br/> |<span data-ttu-id="fc41e-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="fc41e-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="fc41e-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="fc41e-109">Called by:</span></span>  <br/> |<span data-ttu-id="fc41e-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="fc41e-110">Client</span></span>  <br/> |
|<span data-ttu-id="fc41e-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="fc41e-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="fc41e-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="fc41e-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="fc41e-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc41e-113">Parameters</span></span>

<span data-ttu-id="fc41e-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="fc41e-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="fc41e-115">[entrada] Se trata de un puntero a una secuencia que se abre en la [Propiedad canónico PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="fc41e-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="fc41e-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="fc41e-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="fc41e-117">[entrada] Esto es un puntero a un</span><span class="sxs-lookup"><span data-stu-id="fc41e-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="fc41e-118">Estructura [RTF_WCSINFO](rtf_wcsinfo.md) que contiene las opciones de la función.</span><span class="sxs-lookup"><span data-stu-id="fc41e-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="fc41e-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="fc41e-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="fc41e-120">[out] Esto es un puntero a la ubicación donde se devuelve una secuencia para el RTF descomprimido.</span><span class="sxs-lookup"><span data-stu-id="fc41e-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="fc41e-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="fc41e-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="fc41e-122">[out] Se trata de un puntero a una estructura [RTF_WCSRETINFO](rtf_wcsretinfo.md) que contiene información acerca del formato de la secuencia devuelta descomprimida.</span><span class="sxs-lookup"><span data-stu-id="fc41e-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="fc41e-123">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="fc41e-123">Return values</span></span>

<span data-ttu-id="fc41e-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc41e-124">S_OK</span></span> 
  
- <span data-ttu-id="fc41e-125">La llamada a la función es correcta.</span><span class="sxs-lookup"><span data-stu-id="fc41e-125">The function call is successful.</span></span>
    
<span data-ttu-id="fc41e-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fc41e-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="fc41e-127">Esto se devuelve si el indicador **MAPI_NATIVE_BODY** se combina con el indicador **MAPI_MODIFY** en el campo **ulFlags** de la estructura **RTF_WCSINFO** señalada a *pWCSInfo* .</span><span class="sxs-lookup"><span data-stu-id="fc41e-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fc41e-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc41e-128">Remarks</span></span>

<span data-ttu-id="fc41e-129">**WrapCompressedRTFStreamEx** le permite tener acceso al cuerpo de un mensaje de correo electrónico encapsulado en RTF comprimido por descomprimir la secuencia, devuelve la secuencia descomprimida y su formato y, opcionalmente, la secuencia de cuerpo nativo.</span><span class="sxs-lookup"><span data-stu-id="fc41e-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="fc41e-130">La secuencia de cuerpo nativo puede ser en RTF, texto sin formato o HTML.</span><span class="sxs-lookup"><span data-stu-id="fc41e-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="fc41e-131">El modelo de objetos de Microsoft Office Outlook proporciona una propiedad de **cuerpo** para objetos **MailItem** y una [Propiedad MailItem.BodyFormat (Outlook)](http://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) que indica el formato del texto del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="fc41e-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](http://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="fc41e-132">Por diseño, una solución que no sea de confianza para Outlook invoca cuadros de diálogo de seguridad generados por la protección de seguridad de Outlook.</span><span class="sxs-lookup"><span data-stu-id="fc41e-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="fc41e-133">Uso de la función MAPI exportada **WrapCompressedRTFStreamEx** permite una solución usar MAPI en lugar del modelo de objetos de Outlook y para evitar estos cuadros de diálogo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fc41e-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="fc41e-134">Debido a que la **MAPI\_NATIVE_BODY** marca no se puede combinar con la **MAPI\_modificar** marca en el campo **ulFlags** de la **RTF\_WCSINFO** estructura señala a *pWCSInfo*, sólo puede tener acceso nativo secuencia de cuerpo en modo de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fc41e-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="fc41e-135">Para obtener acceso a la secuencia de cuerpo nativos en modo de lectura y escritura, debe utilizar la función **WrapCompressedRTFStream** .</span><span class="sxs-lookup"><span data-stu-id="fc41e-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc41e-136">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="fc41e-136">See also</span></span>

- [<span data-ttu-id="fc41e-137">Recuperar el cuerpo de un mensaje en formato RTF comprimido y convertirlo a su formato nativo</span><span class="sxs-lookup"><span data-stu-id="fc41e-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

