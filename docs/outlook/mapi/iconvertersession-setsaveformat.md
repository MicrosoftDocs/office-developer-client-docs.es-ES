---
title: IConverterSessionSetSaveFormat
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
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f24ad938fdb8c3ac234e1d78f2668139840c8b8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568220"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="fdffa-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="fdffa-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="fdffa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdffa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdffa-105">Establece el formato en el que el convertidor devolverá una secuencia MIME en [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span><span class="sxs-lookup"><span data-stu-id="fdffa-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="fdffa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdffa-106">Parameters</span></span>

<span data-ttu-id="fdffa-107">_mstSaveFormat_</span><span class="sxs-lookup"><span data-stu-id="fdffa-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="fdffa-108">[entrada] Dar formato a la operación de guardar que se usará para una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="fdffa-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="fdffa-109">Para obtener más información, vea el tipo de enumeración [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fdffa-109">For more information, see the enum type [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="fdffa-110">**SAVE_RFC1521**: uso MIME, que es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fdffa-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="fdffa-111">**SAVE_RFC822**: utilizar uuencode.</span><span class="sxs-lookup"><span data-stu-id="fdffa-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="fdffa-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="fdffa-112">Return values</span></span>

<span data-ttu-id="fdffa-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="fdffa-113">S_OK</span></span>
  
> <span data-ttu-id="fdffa-114">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="fdffa-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="fdffa-115">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fdffa-115">MFCMAPI reference</span></span>

<span data-ttu-id="fdffa-116">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="fdffa-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fdffa-117">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="fdffa-117">**File**</span></span>|<span data-ttu-id="fdffa-118">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="fdffa-118">**Function**</span></span>|<span data-ttu-id="fdffa-119">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="fdffa-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fdffa-120">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="fdffa-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="fdffa-121">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="fdffa-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="fdffa-122">MFCMAPI utiliza MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="fdffa-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="fdffa-123">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="fdffa-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="fdffa-124">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="fdffa-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="fdffa-125">MFCMAPI utiliza MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="fdffa-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fdffa-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="fdffa-126">See also</span></span>

- [<span data-ttu-id="fdffa-127">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fdffa-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="fdffa-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="fdffa-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="fdffa-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="fdffa-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="fdffa-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="fdffa-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="fdffa-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="fdffa-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="fdffa-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="fdffa-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="fdffa-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="fdffa-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="fdffa-134">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="fdffa-134">MAPI Constants</span></span>](mapi-constants.md)

