---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: bdb879a2412c817b7b314cd7bf6de1fa4c9f40d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820982"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="9f43b-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="9f43b-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="9f43b-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f43b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f43b-105">Descomprime el el cuerpo de un mensaje de correo electrónico que está en comprimido con formato (RTF), indica el formato de la secuencia descomprimido, de forma opcional convierte la secuencia descomprimida en su formato nativo y devuelve la secuencia de descomprimido o la convertir la secuencia nativo.</span><span class="sxs-lookup"><span data-stu-id="9f43b-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9f43b-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="9f43b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f43b-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="9f43b-107">Exported by:</span></span>  <br/> |<span data-ttu-id="9f43b-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="9f43b-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="9f43b-109">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9f43b-109">Called by:</span></span>  <br/> |<span data-ttu-id="9f43b-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="9f43b-110">Client</span></span>  <br/> |
|<span data-ttu-id="9f43b-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="9f43b-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="9f43b-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="9f43b-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="9f43b-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f43b-113">Parameters</span></span>

<span data-ttu-id="9f43b-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="9f43b-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="9f43b-115">[entrada] Se trata de un puntero a una secuencia que se abre en la [Propiedad canónico PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f43b-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="9f43b-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="9f43b-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="9f43b-117">[entrada] Esto es un puntero a un</span><span class="sxs-lookup"><span data-stu-id="9f43b-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="9f43b-118">Estructura [RTF_WCSINFO](rtf_wcsinfo.md) que contiene las opciones de la función.</span><span class="sxs-lookup"><span data-stu-id="9f43b-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="9f43b-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="9f43b-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="9f43b-120">[out] Esto es un puntero a la ubicación donde se devuelve una secuencia para el RTF descomprimido.</span><span class="sxs-lookup"><span data-stu-id="9f43b-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="9f43b-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="9f43b-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="9f43b-122">[out] Se trata de un puntero a una estructura [RTF_WCSRETINFO](rtf_wcsretinfo.md) que contiene información acerca del formato de la secuencia devuelta descomprimida.</span><span class="sxs-lookup"><span data-stu-id="9f43b-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="9f43b-123">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="9f43b-123">Return values</span></span>

<span data-ttu-id="9f43b-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f43b-124">S_OK</span></span> 
  
- <span data-ttu-id="9f43b-125">La llamada a la función es correcta.</span><span class="sxs-lookup"><span data-stu-id="9f43b-125">The function call is successful.</span></span>
    
<span data-ttu-id="9f43b-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9f43b-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="9f43b-127">Esto se devuelve si el indicador **MAPI_NATIVE_BODY** se combina con el indicador **MAPI_MODIFY** en el campo **ulFlags** de la estructura **RTF_WCSINFO** señalada a *pWCSInfo* .</span><span class="sxs-lookup"><span data-stu-id="9f43b-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9f43b-128">Notas</span><span class="sxs-lookup"><span data-stu-id="9f43b-128">Remarks</span></span>

<span data-ttu-id="9f43b-129">**WrapCompressedRTFStreamEx** le permite tener acceso al cuerpo de un mensaje de correo electrónico encapsulado en RTF comprimido por descomprimir la secuencia, devuelve la secuencia descomprimida y su formato y, opcionalmente, la secuencia de cuerpo nativo.</span><span class="sxs-lookup"><span data-stu-id="9f43b-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="9f43b-130">La secuencia de cuerpo nativo puede ser en RTF, texto sin formato o HTML.</span><span class="sxs-lookup"><span data-stu-id="9f43b-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="9f43b-131">El modelo de objetos de Microsoft Office Outlook proporciona una propiedad de **cuerpo** para objetos **MailItem** y una [Propiedad MailItem.BodyFormat (Outlook)](http://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) que indica el formato del texto del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="9f43b-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](http://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="9f43b-132">Por diseño, una solución que no sea de confianza para Outlook invoca cuadros de diálogo de seguridad generados por la protección de seguridad de Outlook.</span><span class="sxs-lookup"><span data-stu-id="9f43b-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="9f43b-133">Uso de la función MAPI exportada **WrapCompressedRTFStreamEx** permite una solución usar MAPI en lugar del modelo de objetos de Outlook y para evitar estos cuadros de diálogo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9f43b-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="9f43b-134">Debido a que la **MAPI\_NATIVE_BODY** marca no se puede combinar con la **MAPI\_modificar** marca en el campo **ulFlags** de la **RTF\_WCSINFO** estructura señala a *pWCSInfo*, sólo puede tener acceso nativo secuencia de cuerpo en modo de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="9f43b-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="9f43b-135">Para obtener acceso a la secuencia de cuerpo nativos en modo de lectura y escritura, debe utilizar la función **WrapCompressedRTFStream** .</span><span class="sxs-lookup"><span data-stu-id="9f43b-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f43b-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="9f43b-136">See also</span></span>

- [<span data-ttu-id="9f43b-137">Recuperar el cuerpo de un mensaje en formato RTF comprimido y convertirlo a su formato nativo</span><span class="sxs-lookup"><span data-stu-id="9f43b-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

