---
title: IConverterSessionSetEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5a81e04d112e0adf201dcacf03673daac77a04ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382424"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="5ae22-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="5ae22-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="5ae22-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ae22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ae22-105">Inicializa la codificación que se utilizará durante la conversión.</span><span class="sxs-lookup"><span data-stu-id="5ae22-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="5ae22-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ae22-106">Parameters</span></span>

<span data-ttu-id="5ae22-107">_et_</span><span class="sxs-lookup"><span data-stu-id="5ae22-107">_et_</span></span>
  
> <span data-ttu-id="5ae22-108">Un valor [ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5ae22-108">An [ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="5ae22-109">Se admiten sólo los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="5ae22-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="5ae22-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="5ae22-110">IET_BASE64</span></span>
   - <span data-ttu-id="5ae22-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="5ae22-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="5ae22-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="5ae22-112">IET_QP</span></span>
   - <span data-ttu-id="5ae22-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="5ae22-113">IET_7BIT</span></span>
   - <span data-ttu-id="5ae22-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="5ae22-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5ae22-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ae22-115">Return value</span></span>

<span data-ttu-id="5ae22-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="5ae22-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="5ae22-117">El tipo de codificación pasado no era válido.</span><span class="sxs-lookup"><span data-stu-id="5ae22-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ae22-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5ae22-118">Remarks</span></span>

<span data-ttu-id="5ae22-119">Llame a **SetEncoding** antes de usar [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para llevar a cabo la conversión.</span><span class="sxs-lookup"><span data-stu-id="5ae22-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="5ae22-120">Use **SetEncoding** para establecer la codificación para sólo el cuerpo del mensaje más externo de un elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="5ae22-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="5ae22-121">Microsoft Outlook 2010 y Microsoft Outlook 2013 eligen la codificación para los datos adjuntos individuales.</span><span class="sxs-lookup"><span data-stu-id="5ae22-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5ae22-122">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5ae22-122">MFCMAPI reference</span></span>

<span data-ttu-id="5ae22-123">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5ae22-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5ae22-124">**File**</span><span class="sxs-lookup"><span data-stu-id="5ae22-124">**File**</span></span>|<span data-ttu-id="5ae22-125">**Función**</span><span class="sxs-lookup"><span data-stu-id="5ae22-125">**Function**</span></span>|<span data-ttu-id="5ae22-126">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="5ae22-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5ae22-127">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="5ae22-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="5ae22-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="5ae22-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="5ae22-129">MFCMAPI utiliza MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="5ae22-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="5ae22-130">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="5ae22-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="5ae22-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="5ae22-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="5ae22-132">MFCMAPI utiliza MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="5ae22-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5ae22-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ae22-133">See also</span></span>

- [<span data-ttu-id="5ae22-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ae22-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="5ae22-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="5ae22-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="5ae22-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="5ae22-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="5ae22-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="5ae22-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="5ae22-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="5ae22-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="5ae22-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="5ae22-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="5ae22-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="5ae22-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="5ae22-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5ae22-141">MAPI Constants</span></span>](mapi-constants.md)

