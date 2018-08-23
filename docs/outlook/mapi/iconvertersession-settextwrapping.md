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
ms.openlocfilehash: a89f6dd14e8bbea9d0d4145dc05bf332af95234a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573638"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="fbbb4-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="fbbb4-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="fbbb4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbbb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbbb4-105">Establece el ancho de una secuencia de MIME que va a devolver el convertidor en [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)de ajuste de texto.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="fbbb4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbbb4-106">Parameters</span></span>

 <span data-ttu-id="fbbb4-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="fbbb4-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="fbbb4-108">[entrada] Si se debe ajustar el texto o no.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="fbbb4-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="fbbb4-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="fbbb4-110">[entrada] El ancho para usar de ajuste de texto.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fbbb4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbbb4-111">Return value</span></span>

<span data-ttu-id="fbbb4-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="fbbb4-112">S_OK</span></span>
  
> <span data-ttu-id="fbbb4-113">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="fbbb4-114">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fbbb4-114">MFCMAPI reference</span></span>

<span data-ttu-id="fbbb4-115">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fbbb4-116">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-116">**File**</span></span>|<span data-ttu-id="fbbb4-117">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-117">**Function**</span></span>|<span data-ttu-id="fbbb4-118">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fbbb4-119">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="fbbb4-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="fbbb4-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="fbbb4-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="fbbb4-121">MFCMAPI utiliza MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="fbbb4-122">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="fbbb4-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="fbbb4-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="fbbb4-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="fbbb4-124">MFCMAPI utiliza MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fbbb4-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="fbbb4-125">See also</span></span>



[<span data-ttu-id="fbbb4-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fbbb4-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="fbbb4-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="fbbb4-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="fbbb4-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="fbbb4-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="fbbb4-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="fbbb4-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="fbbb4-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="fbbb4-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="fbbb4-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="fbbb4-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="fbbb4-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="fbbb4-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="fbbb4-133">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="fbbb4-133">MAPI Constants</span></span>](mapi-constants.md)

