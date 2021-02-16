---
title: IConverterSessionSetTextWrapping
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetTextWrapping
api_type:
- COM
ms.assetid: 8674b288-43a3-6376-35ca-9dbaa3a1851e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a8a6546c38c629c193c1978998c95918943fe5c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423590"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="e8618-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="e8618-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="e8618-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8618-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8618-105">Establece el ancho de ajuste de texto de una secuencia MIME que devolverá el convertidor [en IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span><span class="sxs-lookup"><span data-stu-id="e8618-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="e8618-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8618-106">Parameters</span></span>

 <span data-ttu-id="e8618-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="e8618-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="e8618-108">[entrada] Si se va a ajustar el texto o no.</span><span class="sxs-lookup"><span data-stu-id="e8618-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="e8618-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="e8618-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="e8618-110">[entrada] Ancho de ajuste de texto que se usará.</span><span class="sxs-lookup"><span data-stu-id="e8618-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e8618-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8618-111">Return value</span></span>

<span data-ttu-id="e8618-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8618-112">S_OK</span></span>
  
> <span data-ttu-id="e8618-113">La llamada se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e8618-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="e8618-114">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e8618-114">MFCMAPI reference</span></span>

<span data-ttu-id="e8618-115">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e8618-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e8618-116">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="e8618-116">**File**</span></span>|<span data-ttu-id="e8618-117">**Función**</span><span class="sxs-lookup"><span data-stu-id="e8618-117">**Function**</span></span>|<span data-ttu-id="e8618-118">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="e8618-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e8618-119">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="e8618-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="e8618-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="e8618-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="e8618-121">MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="e8618-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="e8618-122">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="e8618-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="e8618-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="e8618-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="e8618-124">MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="e8618-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8618-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e8618-125">See also</span></span>



[<span data-ttu-id="e8618-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e8618-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="e8618-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="e8618-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="e8618-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="e8618-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="e8618-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="e8618-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="e8618-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="e8618-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="e8618-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="e8618-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="e8618-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="e8618-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="e8618-133">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e8618-133">MAPI Constants</span></span>](mapi-constants.md)

