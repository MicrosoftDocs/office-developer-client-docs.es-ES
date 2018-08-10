---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: 'Última modificación: 20 de septiembre de 2017'
ms.openlocfilehash: b59114926d44ba613efbbde1c8dd5d17c26756c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817161"
---
# <a name="iconvertersessionmapitomimestm"></a><span data-ttu-id="e0b96-103">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="e0b96-103">IConverterSession::MAPIToMIMEStm</span></span>
 
  
<span data-ttu-id="e0b96-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0b96-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0b96-105">Convierte un mensaje MAPI a una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="e0b96-105">Converts a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="e0b96-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0b96-106">Parameters</span></span>

 <span data-ttu-id="e0b96-107">_pMsg_</span><span class="sxs-lookup"><span data-stu-id="e0b96-107">_pmsg_</span></span>
  
> <span data-ttu-id="e0b96-108">[entrada] Puntero al mensaje que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="e0b96-108">[in] Pointer to the message to convert.</span></span> <span data-ttu-id="e0b96-109">Vea mapidefs.h para la definición de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="e0b96-109">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="e0b96-110">_pstm_</span><span class="sxs-lookup"><span data-stu-id="e0b96-110">_pstm_</span></span>
  
> <span data-ttu-id="e0b96-111">[out] Interfaz [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) a la secuencia de salida.</span><span class="sxs-lookup"><span data-stu-id="e0b96-111">[out] [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface to output the stream.</span></span> 
    
 <span data-ttu-id="e0b96-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e0b96-112">_ulFlags_</span></span>
  
>  <span data-ttu-id="e0b96-113">[entrada] Marcas que muestran las acciones específicas para el convertidor de:</span><span class="sxs-lookup"><span data-stu-id="e0b96-113">[in] Flags that indicate specific actions for the converter:</span></span> 
    
<span data-ttu-id="e0b96-114">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="e0b96-114">CCSF_8BITHEADERS</span></span>
  
> <span data-ttu-id="e0b96-115">El convertidor debe permitir que los encabezados de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="e0b96-115">The converter should allow 8-bit headers.</span></span>
    
<span data-ttu-id="e0b96-116">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="e0b96-116">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="e0b96-117">Envía/sin enviar información se conserva en sin enviar X.</span><span class="sxs-lookup"><span data-stu-id="e0b96-117">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="e0b96-118">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="e0b96-118">CCSF_GLOBAL_MESSAGE</span></span>
  
> <span data-ttu-id="e0b96-119">El convertidor debe crear un mensaje internacional (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="e0b96-119">The converter should build an international message (EAI/RFC6530).</span></span>
    
<span data-ttu-id="e0b96-120">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="e0b96-120">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="e0b96-121">Los destinatarios de CCO del mensaje MAPI se deben incluir en la secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="e0b96-121">BCC recipients of the MAPI message should be included in the MIME stream.</span></span>
    
<span data-ttu-id="e0b96-122">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="e0b96-122">CCSF_NO_MSGID</span></span>
  
> <span data-ttu-id="e0b96-123">Campo de identificador de mensaje no se incluya en los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="e0b96-123">Do not include Message-Id field in outgoing messages.</span></span>
    
<span data-ttu-id="e0b96-124">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="e0b96-124">CCSF_NOHEADERS</span></span>
  
> <span data-ttu-id="e0b96-125">El convertidor debe omitir los encabezados del mensaje externo.</span><span class="sxs-lookup"><span data-stu-id="e0b96-125">The converter should ignore the headers of the outside message.</span></span>
    
<span data-ttu-id="e0b96-126">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="e0b96-126">CCSF_PLAIN_TEXT_ONLY</span></span>
  
> <span data-ttu-id="e0b96-127">El convertidor debe enviar sólo texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="e0b96-127">The converter should just send plain text.</span></span>
    
<span data-ttu-id="e0b96-128">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="e0b96-128">CCSF_SMTP</span></span>
  
> <span data-ttu-id="e0b96-129">El convertidor se pasa un mensaje SMTP.</span><span class="sxs-lookup"><span data-stu-id="e0b96-129">The converter is being passed an SMTP message.</span></span> <span data-ttu-id="e0b96-130">Siempre se debe establecer este indicador.</span><span class="sxs-lookup"><span data-stu-id="e0b96-130">This flag must always be set.</span></span>
    
<span data-ttu-id="e0b96-131">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="e0b96-131">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="e0b96-132">El convertidor debe convertir de HTML a formato RTF en el mensaje MIME.</span><span class="sxs-lookup"><span data-stu-id="e0b96-132">The converter should convert from HTML to RTF format in the MIME message.</span></span>
    
<span data-ttu-id="e0b96-133">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="e0b96-133">CCSF_USE_TNEF</span></span>
  
> <span data-ttu-id="e0b96-134">En el mensaje MIME, el convertidor debe utilizar formato de formato de encapsulación neutro de transporte (TNEF).</span><span class="sxs-lookup"><span data-stu-id="e0b96-134">The converter should use Transport Neutral Encapsulation Format (TNEF) format in the MIME message.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e0b96-135">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="e0b96-135">Return values</span></span>

<span data-ttu-id="e0b96-136">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e0b96-136">E_INVALIDARG</span></span>
  
> <span data-ttu-id="e0b96-137">Se pasaron indicadores no válidos o *pmsg* o *pstm* es NULL.</span><span class="sxs-lookup"><span data-stu-id="e0b96-137">Invalid flags were passed, or  *pmsg*  or  *pstm*  is NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e0b96-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0b96-138">Remarks</span></span>

<span data-ttu-id="e0b96-139">Admite únicamente para los tipos de mensaje estándar de Outlook.</span><span class="sxs-lookup"><span data-stu-id="e0b96-139">Supported only for standard Outlook message types.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e0b96-140">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e0b96-140">MFCMAPI reference</span></span>

<span data-ttu-id="e0b96-141">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e0b96-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e0b96-142">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="e0b96-142">**File**</span></span>|<span data-ttu-id="e0b96-143">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="e0b96-143">**Function**</span></span>|<span data-ttu-id="e0b96-144">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="e0b96-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0b96-145">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="e0b96-145">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="e0b96-146">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="e0b96-146">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="e0b96-147">MFCMAPI utiliza MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="e0b96-147">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="e0b96-148">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="e0b96-148">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="e0b96-149">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="e0b96-149">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="e0b96-150">MFCMAPI utiliza MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="e0b96-150">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0b96-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0b96-151">See also</span></span>



[<span data-ttu-id="e0b96-152">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0b96-152">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="e0b96-153">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="e0b96-153">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="e0b96-154">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="e0b96-154">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="e0b96-155">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="e0b96-155">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="e0b96-156">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="e0b96-156">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="e0b96-157">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="e0b96-157">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="e0b96-158">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="e0b96-158">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="e0b96-159">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="e0b96-159">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
  
[<span data-ttu-id="e0b96-160">Propiedad canónica PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="e0b96-160">PidTagMessageEditorFormat Canonical Property</span></span>](pidtagmessageeditorformat-canonical-property.md)
  
[<span data-ttu-id="e0b96-161">Propiedad can�nico de PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="e0b96-161">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)


[<span data-ttu-id="e0b96-162">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e0b96-162">MAPI Constants</span></span>](mapi-constants.md)
