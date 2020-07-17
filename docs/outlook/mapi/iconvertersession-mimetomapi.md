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
ms.openlocfilehash: c9fcffa8ad4dc982e869f4ccd449e1377fb1ea57
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160289"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="3f360-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="3f360-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="3f360-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f360-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f360-105">Convierte una secuencia MIME en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="3f360-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="3f360-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f360-106">Parameters</span></span>

 <span data-ttu-id="3f360-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="3f360-107">_pstm_</span></span>
  
> <span data-ttu-id="3f360-108">a Interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) a una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="3f360-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="3f360-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="3f360-109">_pmsg_</span></span>
  
> <span data-ttu-id="3f360-110">a Puntero al mensaje que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="3f360-110">[in] Pointer to the message to load.</span></span> <span data-ttu-id="3f360-111">El llamador debe proporcionar un mensaje para que se rellene la API, por lo que el objeto debe ir [in].</span><span class="sxs-lookup"><span data-stu-id="3f360-111">The caller must supply a message for the API to fill out, so the object must go [in].</span></span> <span data-ttu-id="3f360-112">Consulte mapidefs. h para obtener la definición de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="3f360-112">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="3f360-113">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="3f360-113">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="3f360-114">a Este valor debe ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3f360-114">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="3f360-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3f360-115">_ulFlags_</span></span>
  
> <span data-ttu-id="3f360-116">a Este parámetro identifica cualquier acción especial que deba realizarse durante la conversión.</span><span class="sxs-lookup"><span data-stu-id="3f360-116">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="3f360-117">Debe ser cero (0) si no se va a realizar ninguna acción específica o una combinación de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="3f360-117">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="3f360-118">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="3f360-118">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="3f360-119">La información enviada/no enviada se conserva en X-no enviado.</span><span class="sxs-lookup"><span data-stu-id="3f360-119">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="3f360-120">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="3f360-120">CCSF_SMTP</span></span>
  
> <span data-ttu-id="3f360-121">La secuencia MIME es para un mensaje de Protocolo simple de transferencia de correo (SMTP).</span><span class="sxs-lookup"><span data-stu-id="3f360-121">The MIME stream is for a Simple Mail Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="3f360-122">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="3f360-122">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="3f360-123">Los destinatarios CCO de la secuencia MIME deben incluirse en el mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="3f360-123">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="3f360-124">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="3f360-124">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="3f360-125">El cuerpo HTML de la secuencia MIME debe convertirse a formato de texto enriquecido (RTF) en el mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="3f360-125">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="3f360-126">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="3f360-126">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="3f360-127">El convertidor debe controlar la secuencia MIME como un mensaje Internacional (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="3f360-127">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="3f360-128">No se admite en Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="3f360-128">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3f360-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f360-129">Return value</span></span>

<span data-ttu-id="3f360-130">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3f360-130">E_INVALIDARG</span></span>
  
> <span data-ttu-id="3f360-131">Indica que _pstm_ es **null**, _PMSG_ es **null**o _ulFlags_ no es válido.</span><span class="sxs-lookup"><span data-stu-id="3f360-131">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3f360-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f360-132">Remarks</span></span>

<span data-ttu-id="3f360-133">Si ha especificado **CCSF_USE_RTF** como parte de _ulFlags_ y el almacén de mensajes de destino admite tanto HTML como RTF, el mensaje MAPI se convertirá en HTML o RTF.</span><span class="sxs-lookup"><span data-stu-id="3f360-133">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="3f360-134">Si el mensaje se convierte en RTF, el formato convertido será comprimido RTF, cualquier HTML se incrustará en la cadena RTF comprimida y la cadena se incluirá en la [propiedad canónica PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="3f360-134">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3f360-135">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3f360-135">MFCMAPI reference</span></span>

<span data-ttu-id="3f360-136">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="3f360-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3f360-137">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="3f360-137">**File**</span></span>|<span data-ttu-id="3f360-138">**Función**</span><span class="sxs-lookup"><span data-stu-id="3f360-138">**Function**</span></span>|<span data-ttu-id="3f360-139">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="3f360-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3f360-140">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="3f360-140">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="3f360-141">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="3f360-141">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="3f360-142">MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="3f360-142">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="3f360-143">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="3f360-143">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="3f360-144">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="3f360-144">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="3f360-145">MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="3f360-145">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f360-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f360-146">See also</span></span>



[<span data-ttu-id="3f360-147">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f360-147">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="3f360-148">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="3f360-148">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="3f360-149">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="3f360-149">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="3f360-150">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="3f360-150">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="3f360-151">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="3f360-151">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="3f360-152">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="3f360-152">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="3f360-153">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="3f360-153">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="3f360-154">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="3f360-154">MAPI Constants</span></span>](mapi-constants.md)

