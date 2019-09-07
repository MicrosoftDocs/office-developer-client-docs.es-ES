---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Última modificación: septiembre 06, 2019'
ms.openlocfilehash: f6f671cbfd5e14d602aaa31d31e54e859f068593
ms.sourcegitcommit: 27a9f3568318470e7ee09ad93a90c3f80d3ef0cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/07/2019
ms.locfileid: "36790774"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="2ab3a-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="2ab3a-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="2ab3a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ab3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ab3a-105">Convierte una secuencia MIME en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="2ab3a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ab3a-106">Parameters</span></span>

 <span data-ttu-id="2ab3a-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="2ab3a-107">_pstm_</span></span>
  
> <span data-ttu-id="2ab3a-108">a Interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) a una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="2ab3a-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="2ab3a-109">_pmsg_</span></span>
  
> <span data-ttu-id="2ab3a-110">a Puntero al mensaje que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-110">[in] Pointer to the message to load.</span></span> <span data-ttu-id="2ab3a-111">El llamador debe proporcionar un mensaje para que se rellene la API, por lo que el objeto debe ir [in].</span><span class="sxs-lookup"><span data-stu-id="2ab3a-111">The caller must supply a message for the API to fill out, so the object must go [in].</span></span> <span data-ttu-id="2ab3a-112">Consulte mapidefs. h para obtener la definición de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-112">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="2ab3a-113">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="2ab3a-113">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="2ab3a-114">a Este valor debe ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-114">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="2ab3a-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2ab3a-115">_ulFlags_</span></span>
  
> <span data-ttu-id="2ab3a-116">a Este parámetro identifica cualquier acción especial que deba realizarse durante la conversión.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-116">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="2ab3a-117">Debe ser cero (0) si no se va a realizar ninguna acción específica o una combinación de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="2ab3a-117">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="2ab3a-118">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="2ab3a-118">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="2ab3a-119">La información enviada/no enviada se conserva en X-no enviado.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-119">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="2ab3a-120">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="2ab3a-120">CCSF_SMTP</span></span>
  
> <span data-ttu-id="2ab3a-121">La secuencia MIME es para un mensaje de protocolo de transferencia de MAPI simple (SMTP).</span><span class="sxs-lookup"><span data-stu-id="2ab3a-121">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="2ab3a-122">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="2ab3a-122">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="2ab3a-123">Los destinatarios CCO de la secuencia MIME deben incluirse en el mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-123">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="2ab3a-124">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="2ab3a-124">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="2ab3a-125">El cuerpo HTML de la secuencia MIME debe convertirse a formato de texto enriquecido (RTF) en el mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-125">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="2ab3a-126">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="2ab3a-126">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="2ab3a-127">El convertidor debe controlar la secuencia MIME como un mensaje Internacional (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="2ab3a-127">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="2ab3a-128">No se admite en Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-128">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2ab3a-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ab3a-129">Return value</span></span>

<span data-ttu-id="2ab3a-130">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2ab3a-130">E_INVALIDARG</span></span>
  
> <span data-ttu-id="2ab3a-131">Indica que _pstm_ es **null**, _PMSG_ es **null**o _ulFlags_ no es válido.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-131">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2ab3a-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2ab3a-132">Remarks</span></span>

<span data-ttu-id="2ab3a-133">Si ha especificado **CCSF_USE_RTF** como parte de _ulFlags_ y el almacén de mensajes de destino admite tanto HTML como RTF, el mensaje MAPI se convertirá en HTML o RTF.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-133">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="2ab3a-134">Si el mensaje se convierte en RTF, el formato convertido será comprimido RTF, cualquier HTML se incrustará en la cadena RTF comprimida y la cadena se incluirá en la [propiedad canónica PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="2ab3a-134">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2ab3a-135">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2ab3a-135">MFCMAPI reference</span></span>

<span data-ttu-id="2ab3a-136">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2ab3a-137">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="2ab3a-137">**File**</span></span>|<span data-ttu-id="2ab3a-138">**Función**</span><span class="sxs-lookup"><span data-stu-id="2ab3a-138">**Function**</span></span>|<span data-ttu-id="2ab3a-139">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="2ab3a-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2ab3a-140">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="2ab3a-140">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="2ab3a-141">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="2ab3a-141">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="2ab3a-142">MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-142">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="2ab3a-143">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="2ab3a-143">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="2ab3a-144">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="2ab3a-144">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="2ab3a-145">MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="2ab3a-145">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ab3a-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ab3a-146">See also</span></span>



[<span data-ttu-id="2ab3a-147">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ab3a-147">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="2ab3a-148">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="2ab3a-148">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="2ab3a-149">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="2ab3a-149">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="2ab3a-150">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="2ab3a-150">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="2ab3a-151">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="2ab3a-151">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="2ab3a-152">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="2ab3a-152">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="2ab3a-153">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="2ab3a-153">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="2ab3a-154">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="2ab3a-154">MAPI Constants</span></span>](mapi-constants.md)

