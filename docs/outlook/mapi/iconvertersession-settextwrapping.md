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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 81771a263a7496042d4950b465c0d5b03290399b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19817172"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="bf191-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="bf191-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="bf191-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf191-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf191-105">Establece el ancho de una secuencia de MIME que va a devolver el convertidor en [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)de ajuste de texto.</span><span class="sxs-lookup"><span data-stu-id="bf191-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="bf191-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf191-106">Parameters</span></span>

 <span data-ttu-id="bf191-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="bf191-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="bf191-108">[entrada] Si se debe ajustar el texto o no.</span><span class="sxs-lookup"><span data-stu-id="bf191-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="bf191-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="bf191-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="bf191-110">[entrada] El ancho para usar de ajuste de texto.</span><span class="sxs-lookup"><span data-stu-id="bf191-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bf191-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf191-111">Return value</span></span>

<span data-ttu-id="bf191-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf191-112">S_OK</span></span>
  
> <span data-ttu-id="bf191-113">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="bf191-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="bf191-114">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bf191-114">MFCMAPI reference</span></span>

<span data-ttu-id="bf191-115">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="bf191-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bf191-116">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="bf191-116">**File**</span></span>|<span data-ttu-id="bf191-117">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="bf191-117">**Function**</span></span>|<span data-ttu-id="bf191-118">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="bf191-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf191-119">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="bf191-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="bf191-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="bf191-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="bf191-121">MFCMAPI utiliza MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf191-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="bf191-122">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="bf191-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="bf191-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="bf191-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="bf191-124">MFCMAPI utiliza MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="bf191-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf191-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="bf191-125">See also</span></span>



[<span data-ttu-id="bf191-126">IConverterSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bf191-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="bf191-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="bf191-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="bf191-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="bf191-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="bf191-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="bf191-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="bf191-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="bf191-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="bf191-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="bf191-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="bf191-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="bf191-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="bf191-133">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="bf191-133">MAPI Constants</span></span>](mapi-constants.md)

