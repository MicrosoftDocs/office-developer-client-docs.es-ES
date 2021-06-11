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
description: 'Last modified: September 06, 2019'
ms.openlocfilehash: c9fcffa8ad4dc982e869f4ccd449e1377fb1ea57
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160289"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="014bb-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="014bb-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="014bb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="014bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="014bb-105">Convierte una secuencia MIME en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="014bb-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="014bb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="014bb-106">Parameters</span></span>

 <span data-ttu-id="014bb-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="014bb-107">_pstm_</span></span>
  
> <span data-ttu-id="014bb-108">[in] [Interfaz IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) a una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="014bb-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="014bb-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="014bb-109">_pmsg_</span></span>
  
> <span data-ttu-id="014bb-110">[in] Puntero al mensaje que se cargará.</span><span class="sxs-lookup"><span data-stu-id="014bb-110">[in] Pointer to the message to load.</span></span> <span data-ttu-id="014bb-111">El autor de la llamada debe proporcionar un mensaje para que la API se rellene, por lo que el objeto debe ir [in].</span><span class="sxs-lookup"><span data-stu-id="014bb-111">The caller must supply a message for the API to fill out, so the object must go [in].</span></span> <span data-ttu-id="014bb-112">Vea mapidefs.h para obtener la definición de tipo **de LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="014bb-112">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="014bb-113">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="014bb-113">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="014bb-114">[in] Este valor debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="014bb-114">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="014bb-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="014bb-115">_ulFlags_</span></span>
  
> <span data-ttu-id="014bb-116">[in] Este parámetro identifica cualquier acción especial que se debe realizar durante la conversión.</span><span class="sxs-lookup"><span data-stu-id="014bb-116">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="014bb-117">Debe ser cero (0) si no se va a realizar ninguna acción específica o una combinación de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="014bb-117">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="014bb-118">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="014bb-118">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="014bb-119">La información enviada o no se conserva en X-Unsent.</span><span class="sxs-lookup"><span data-stu-id="014bb-119">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="014bb-120">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="014bb-120">CCSF_SMTP</span></span>
  
> <span data-ttu-id="014bb-121">La secuencia MIME es para un mensaje del Protocolo simple de transferencia de correo (SMTP).</span><span class="sxs-lookup"><span data-stu-id="014bb-121">The MIME stream is for a Simple Mail Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="014bb-122">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="014bb-122">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="014bb-123">Los destinatarios CCO de la secuencia MIME deben incluirse en el mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="014bb-123">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="014bb-124">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="014bb-124">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="014bb-125">El cuerpo HTML de la secuencia MIME debe convertirse al formato de texto enriquecido (RTF) en el mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="014bb-125">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="014bb-126">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="014bb-126">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="014bb-127">El convertidor debe controlar la secuencia MIME como un mensaje internacional (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="014bb-127">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="014bb-128">No se admite en Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="014bb-128">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="014bb-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="014bb-129">Return value</span></span>

<span data-ttu-id="014bb-130">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="014bb-130">E_INVALIDARG</span></span>
  
> <span data-ttu-id="014bb-131">Indica que  _pstm_ es **null,**  _pmsg_ es **null** o  _ulFlags_ no es válido.</span><span class="sxs-lookup"><span data-stu-id="014bb-131">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="014bb-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="014bb-132">Remarks</span></span>

<span data-ttu-id="014bb-133">Si ha especificado  CCSF_USE_RTF como parte de _ulFlags_ y el almacén de mensajes de destino admite HTML y RTF, el mensaje MAPI se convertirá en HTML o RTF.</span><span class="sxs-lookup"><span data-stu-id="014bb-133">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="014bb-134">Si el mensaje se convierte en RTF, el formato convertido se comprimirá RTF, cualquier HTML se incrustará en la cadena RTF comprimida y la cadena se incluirá en la propiedad canónica [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="014bb-134">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="014bb-135">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="014bb-135">MFCMAPI reference</span></span>

<span data-ttu-id="014bb-136">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="014bb-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="014bb-137">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="014bb-137">**File**</span></span>|<span data-ttu-id="014bb-138">**Función**</span><span class="sxs-lookup"><span data-stu-id="014bb-138">**Function**</span></span>|<span data-ttu-id="014bb-139">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="014bb-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="014bb-140">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="014bb-140">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="014bb-141">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="014bb-141">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="014bb-142">MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="014bb-142">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="014bb-143">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="014bb-143">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="014bb-144">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="014bb-144">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="014bb-145">MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="014bb-145">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="014bb-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="014bb-146">See also</span></span>



[<span data-ttu-id="014bb-147">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="014bb-147">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="014bb-148">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="014bb-148">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="014bb-149">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="014bb-149">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="014bb-150">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="014bb-150">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="014bb-151">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="014bb-151">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="014bb-152">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="014bb-152">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="014bb-153">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="014bb-153">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="014bb-154">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="014bb-154">MAPI Constants</span></span>](mapi-constants.md)

