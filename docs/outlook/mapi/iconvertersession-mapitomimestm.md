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
description: 'Last modified: September 20, 2017'
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326948"
---
# <a name="iconvertersessionmapitomimestm"></a><span data-ttu-id="38473-103">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="38473-103">IConverterSession::MAPIToMIMEStm</span></span>
 
  
<span data-ttu-id="38473-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38473-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38473-105">Convierte un mensaje MAPI en una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="38473-105">Converts a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="38473-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38473-106">Parameters</span></span>

 <span data-ttu-id="38473-107">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="38473-107">_pmsg_</span></span>
  
> <span data-ttu-id="38473-108">[entrada] Puntero al mensaje que se convertirá.</span><span class="sxs-lookup"><span data-stu-id="38473-108">[in] Pointer to the message to convert.</span></span> <span data-ttu-id="38473-109">Vea mapidefs.h para obtener la definición de tipo **de LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="38473-109">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="38473-110">_pstm_</span><span class="sxs-lookup"><span data-stu-id="38473-110">_pstm_</span></span>
  
> <span data-ttu-id="38473-111">[salida] [Interfaz IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para generar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="38473-111">[out] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to output the stream.</span></span> 
    
 <span data-ttu-id="38473-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="38473-112">_ulFlags_</span></span>
  
>  <span data-ttu-id="38473-113">[entrada] Marcas que indican acciones específicas para el convertidor:</span><span class="sxs-lookup"><span data-stu-id="38473-113">[in] Flags that indicate specific actions for the converter:</span></span> 
    
<span data-ttu-id="38473-114">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="38473-114">CCSF_8BITHEADERS</span></span>
  
> <span data-ttu-id="38473-115">El convertidor debe permitir encabezados de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="38473-115">The converter should allow 8-bit headers.</span></span>
    
<span data-ttu-id="38473-116">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="38473-116">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="38473-117">La información enviada o no enviada se conserva en X-Unsent.</span><span class="sxs-lookup"><span data-stu-id="38473-117">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="38473-118">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="38473-118">CCSF_GLOBAL_MESSAGE</span></span>
  
> <span data-ttu-id="38473-119">El convertidor debe crear un mensaje internacional (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="38473-119">The converter should build an international message (EAI/RFC6530).</span></span>
    
<span data-ttu-id="38473-120">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="38473-120">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="38473-121">Los destinatarios CCO del mensaje MAPI deben incluirse en la secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="38473-121">BCC recipients of the MAPI message should be included in the MIME stream.</span></span>
    
<span data-ttu-id="38473-122">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="38473-122">CCSF_NO_MSGID</span></span>
  
> <span data-ttu-id="38473-123">No incluya ningún Message-Id en los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="38473-123">Do not include Message-Id field in outgoing messages.</span></span>
    
<span data-ttu-id="38473-124">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="38473-124">CCSF_NOHEADERS</span></span>
  
> <span data-ttu-id="38473-125">El convertidor debe omitir los encabezados del mensaje externo.</span><span class="sxs-lookup"><span data-stu-id="38473-125">The converter should ignore the headers of the outside message.</span></span>
    
<span data-ttu-id="38473-126">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="38473-126">CCSF_PLAIN_TEXT_ONLY</span></span>
  
> <span data-ttu-id="38473-127">El convertidor solo debe enviar texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="38473-127">The converter should just send plain text.</span></span>
    
<span data-ttu-id="38473-128">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="38473-128">CCSF_SMTP</span></span>
  
> <span data-ttu-id="38473-129">Se pasa un mensaje SMTP al convertidor.</span><span class="sxs-lookup"><span data-stu-id="38473-129">The converter is being passed an SMTP message.</span></span> <span data-ttu-id="38473-130">Esta marca siempre debe establecerse.</span><span class="sxs-lookup"><span data-stu-id="38473-130">This flag must always be set.</span></span>
    
<span data-ttu-id="38473-131">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="38473-131">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="38473-132">El convertidor debe convertir el formato HTML a RTF en el mensaje MIME.</span><span class="sxs-lookup"><span data-stu-id="38473-132">The converter should convert from HTML to RTF format in the MIME message.</span></span>
    
<span data-ttu-id="38473-133">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="38473-133">CCSF_USE_TNEF</span></span>
  
> <span data-ttu-id="38473-134">El convertidor debe usar el formato TNEF (Transport Neutral Encapsulation Format) en el mensaje MIME.</span><span class="sxs-lookup"><span data-stu-id="38473-134">The converter should use Transport Neutral Encapsulation Format (TNEF) format in the MIME message.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="38473-135">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="38473-135">Return values</span></span>

<span data-ttu-id="38473-136">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="38473-136">E_INVALIDARG</span></span>
  
> <span data-ttu-id="38473-137">Se han pasado marcas no válidas o  *pmsg*  o  *pstm*  es NULL.</span><span class="sxs-lookup"><span data-stu-id="38473-137">Invalid flags were passed, or  *pmsg*  or  *pstm*  is NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="38473-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38473-138">Remarks</span></span>

<span data-ttu-id="38473-139">Solo se admite para tipos de mensajes estándar de Outlook.</span><span class="sxs-lookup"><span data-stu-id="38473-139">Supported only for standard Outlook message types.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="38473-140">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="38473-140">MFCMAPI reference</span></span>

<span data-ttu-id="38473-141">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="38473-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="38473-142">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="38473-142">**File**</span></span>|<span data-ttu-id="38473-143">**Función**</span><span class="sxs-lookup"><span data-stu-id="38473-143">**Function**</span></span>|<span data-ttu-id="38473-144">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="38473-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="38473-145">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="38473-145">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="38473-146">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="38473-146">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="38473-147">MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="38473-147">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="38473-148">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="38473-148">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="38473-149">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="38473-149">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="38473-150">MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="38473-150">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38473-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="38473-151">See also</span></span>



[<span data-ttu-id="38473-152">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38473-152">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="38473-153">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="38473-153">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="38473-154">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="38473-154">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="38473-155">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="38473-155">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="38473-156">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="38473-156">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="38473-157">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="38473-157">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="38473-158">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="38473-158">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="38473-159">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="38473-159">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
  
[<span data-ttu-id="38473-160">Propiedad canónica PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="38473-160">PidTagMessageEditorFormat Canonical Property</span></span>](pidtagmessageeditorformat-canonical-property.md)
  
[<span data-ttu-id="38473-161">Propiedad can�nico de PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="38473-161">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)


[<span data-ttu-id="38473-162">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="38473-162">MAPI Constants</span></span>](mapi-constants.md)

