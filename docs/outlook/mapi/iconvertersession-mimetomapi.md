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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723036"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="1ee31-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="1ee31-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="1ee31-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ee31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ee31-105">Convierte una secuencia MIME en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="1ee31-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="1ee31-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ee31-106">Parameters</span></span>

 <span data-ttu-id="1ee31-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="1ee31-107">_pstm_</span></span>
  
> <span data-ttu-id="1ee31-108">[entrada] Interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) a una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="1ee31-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="1ee31-109">_pMsg_</span><span class="sxs-lookup"><span data-stu-id="1ee31-109">_pmsg_</span></span>
  
> <span data-ttu-id="1ee31-110">[out] Puntero al mensaje que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="1ee31-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="1ee31-111">Vea mapidefs.h para la definición de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="1ee31-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="1ee31-112">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="1ee31-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="1ee31-113">[entrada] Este valor debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="1ee31-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="1ee31-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1ee31-114">_ulFlags_</span></span>
  
> <span data-ttu-id="1ee31-115">[entrada] Este parámetro identifica ninguna acción especial para que sean tomadas durante la conversión.</span><span class="sxs-lookup"><span data-stu-id="1ee31-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="1ee31-116">Debe ser cero (0) si no es ninguna acción específica para que sean tomadas, o una combinación de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="1ee31-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="1ee31-117">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="1ee31-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="1ee31-118">Envía/sin enviar información se conserva en sin enviar X.</span><span class="sxs-lookup"><span data-stu-id="1ee31-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="1ee31-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="1ee31-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="1ee31-120">La secuencia MIME es para un mensaje de Protocolo Simple de transferencia de MAPI (SMTP).</span><span class="sxs-lookup"><span data-stu-id="1ee31-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="1ee31-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="1ee31-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="1ee31-122">Los destinatarios de CCO de la secuencia MIME se deben incluir en el mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="1ee31-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="1ee31-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="1ee31-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="1ee31-124">El cuerpo HTML del objeto stream MIME se debe convertir a formato de texto enriquecido (RTF) en el mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="1ee31-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="1ee31-125">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="1ee31-125">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="1ee31-126">El convertidor debe controlar la secuencia MIME como un mensaje internacional (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="1ee31-126">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="1ee31-127">No se admite en Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="1ee31-127">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1ee31-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ee31-128">Return value</span></span>

<span data-ttu-id="1ee31-129">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1ee31-129">E_INVALIDARG</span></span>
  
> <span data-ttu-id="1ee31-130">Indica que _pstm_ es **null**, _pmsg_ es **null**o _ulFlags indicado_ no es válido.</span><span class="sxs-lookup"><span data-stu-id="1ee31-130">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1ee31-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ee31-131">Remarks</span></span>

<span data-ttu-id="1ee31-132">Si ha especificado **CCSF_USE_RTF** como parte de _ulFlags_ y el almacén de mensajes de destino es compatible con HTML y RTF, el mensaje MAPI se convertirá a HTML o RTF.</span><span class="sxs-lookup"><span data-stu-id="1ee31-132">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="1ee31-133">Si el mensaje se convierte en RTF, se va a comprimir el formato convertido RTF, todo el código HTML se incrustarán en la cadena RTF comprimida, y la cadena estarán contenida en la [Propiedad canónico PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="1ee31-133">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1ee31-134">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1ee31-134">MFCMAPI reference</span></span>

<span data-ttu-id="1ee31-135">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1ee31-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1ee31-136">**File**</span><span class="sxs-lookup"><span data-stu-id="1ee31-136">**File**</span></span>|<span data-ttu-id="1ee31-137">**Función**</span><span class="sxs-lookup"><span data-stu-id="1ee31-137">**Function**</span></span>|<span data-ttu-id="1ee31-138">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1ee31-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ee31-139">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="1ee31-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="1ee31-140">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="1ee31-140">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="1ee31-141">MFCMAPI utiliza MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="1ee31-141">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="1ee31-142">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="1ee31-142">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="1ee31-143">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="1ee31-143">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="1ee31-144">MFCMAPI utiliza MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="1ee31-144">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ee31-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1ee31-145">See also</span></span>



[<span data-ttu-id="1ee31-146">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ee31-146">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="1ee31-147">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="1ee31-147">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="1ee31-148">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="1ee31-148">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="1ee31-149">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="1ee31-149">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="1ee31-150">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="1ee31-150">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="1ee31-151">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="1ee31-151">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="1ee31-152">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="1ee31-152">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="1ee31-153">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="1ee31-153">MAPI Constants</span></span>](mapi-constants.md)

