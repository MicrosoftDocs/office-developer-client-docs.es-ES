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
ms.openlocfilehash: b528d6ef45c02b27f8e07d151793fc338f9af7b1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394359"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="0920e-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="0920e-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="0920e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0920e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0920e-105">Establece el formato en el que el convertidor devolverá una secuencia MIME en [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span><span class="sxs-lookup"><span data-stu-id="0920e-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="0920e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0920e-106">Parameters</span></span>

<span data-ttu-id="0920e-107">_mstSaveFormat_</span><span class="sxs-lookup"><span data-stu-id="0920e-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="0920e-108">[entrada] Dar formato a la operación de guardar que se usará para una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="0920e-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="0920e-109">Para obtener más información, vea el tipo de enumeración [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0920e-109">For more information, see the enum type [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="0920e-110">**SAVE_RFC1521**: uso MIME, que es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0920e-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="0920e-111">**SAVE_RFC822**: utilizar uuencode.</span><span class="sxs-lookup"><span data-stu-id="0920e-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="0920e-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="0920e-112">Return values</span></span>

<span data-ttu-id="0920e-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="0920e-113">S_OK</span></span>
  
> <span data-ttu-id="0920e-114">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="0920e-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="0920e-115">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0920e-115">MFCMAPI reference</span></span>

<span data-ttu-id="0920e-116">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="0920e-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0920e-117">**File**</span><span class="sxs-lookup"><span data-stu-id="0920e-117">**File**</span></span>|<span data-ttu-id="0920e-118">**Función**</span><span class="sxs-lookup"><span data-stu-id="0920e-118">**Function**</span></span>|<span data-ttu-id="0920e-119">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="0920e-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0920e-120">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="0920e-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="0920e-121">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="0920e-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="0920e-122">MFCMAPI utiliza MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="0920e-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="0920e-123">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="0920e-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="0920e-124">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="0920e-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="0920e-125">MFCMAPI utiliza MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="0920e-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0920e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0920e-126">See also</span></span>

- [<span data-ttu-id="0920e-127">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0920e-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="0920e-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="0920e-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="0920e-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="0920e-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="0920e-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="0920e-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="0920e-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="0920e-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="0920e-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="0920e-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="0920e-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="0920e-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="0920e-134">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="0920e-134">MAPI Constants</span></span>](mapi-constants.md)

