---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 356f4470be26ae3803a53af1cec34b3ac6eb0cc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326932"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="5255d-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="5255d-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="5255d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5255d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5255d-105">Convierte una secuencia MIME en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="5255d-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="5255d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5255d-106">Parameters</span></span>

 <span data-ttu-id="5255d-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="5255d-107">_pstm_</span></span>
  
> <span data-ttu-id="5255d-108">a Interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) a una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="5255d-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="5255d-109">_PMSG_</span><span class="sxs-lookup"><span data-stu-id="5255d-109">_pmsg_</span></span>
  
> <span data-ttu-id="5255d-110">contempla Puntero al mensaje que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="5255d-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="5255d-111">Consulte mapidefs. h para obtener la definición de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="5255d-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="5255d-112">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="5255d-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="5255d-113">a Este valor debe ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5255d-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="5255d-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5255d-114">_ulFlags_</span></span>
  
> <span data-ttu-id="5255d-115">a Este parámetro identifica cualquier acción especial que deba realizarse durante la conversión.</span><span class="sxs-lookup"><span data-stu-id="5255d-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="5255d-116">Debe ser cero (0) si no se va a realizar ninguna acción específica o una combinación de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="5255d-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="5255d-117">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="5255d-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="5255d-118">La información enviada/no enviada se conserva en X-no enviado.</span><span class="sxs-lookup"><span data-stu-id="5255d-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="5255d-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="5255d-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="5255d-120">La secuencia MIME es para un mensaje de protocolo de transferencia de MAPI simple (SMTP).</span><span class="sxs-lookup"><span data-stu-id="5255d-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="5255d-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="5255d-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="5255d-122">Los destinatarios CCO de la secuencia MIME deben incluirse en el mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="5255d-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="5255d-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="5255d-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="5255d-124">El cuerpo HTML de la secuencia MIME debe convertirse a formato de texto enriquecido (RTF) en el mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="5255d-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="5255d-125">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="5255d-125">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="5255d-126">El convertidor debe controlar la secuencia MIME como un mensaje Internacional (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="5255d-126">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="5255d-127">No se admite en Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="5255d-127">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5255d-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5255d-128">Return value</span></span>

<span data-ttu-id="5255d-129">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="5255d-129">E_INVALIDARG</span></span>
  
> <span data-ttu-id="5255d-130">Indica que _pstm_ es **null**, _PMSG_ es **null**o _ulFlags_ no es válido.</span><span class="sxs-lookup"><span data-stu-id="5255d-130">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5255d-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5255d-131">Remarks</span></span>

<span data-ttu-id="5255d-132">Si ha especificado **CCSF_USE_RTF** como parte de _ulFlags_ y el almacén de mensajes de destino admite tanto HTML como RTF, el mensaje MAPI se convertirá en HTML o RTF.</span><span class="sxs-lookup"><span data-stu-id="5255d-132">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="5255d-133">Si el mensaje se convierte en RTF, el formato convertido será comprimido RTF, cualquier HTML se incrustará en la cadena RTF comprimida y la cadena se incluirá en la [propiedad canónica PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="5255d-133">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5255d-134">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5255d-134">MFCMAPI reference</span></span>

<span data-ttu-id="5255d-135">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5255d-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5255d-136">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="5255d-136">**File**</span></span>|<span data-ttu-id="5255d-137">**Función**</span><span class="sxs-lookup"><span data-stu-id="5255d-137">**Function**</span></span>|<span data-ttu-id="5255d-138">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="5255d-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5255d-139">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="5255d-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="5255d-140">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="5255d-140">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="5255d-141">MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="5255d-141">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="5255d-142">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="5255d-142">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="5255d-143">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="5255d-143">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="5255d-144">MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="5255d-144">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5255d-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="5255d-145">See also</span></span>



[<span data-ttu-id="5255d-146">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5255d-146">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="5255d-147">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="5255d-147">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="5255d-148">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="5255d-148">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="5255d-149">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="5255d-149">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="5255d-150">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="5255d-150">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="5255d-151">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="5255d-151">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="5255d-152">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="5255d-152">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="5255d-153">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5255d-153">MAPI Constants</span></span>](mapi-constants.md)

