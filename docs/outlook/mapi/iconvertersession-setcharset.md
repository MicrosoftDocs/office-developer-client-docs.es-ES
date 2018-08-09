---
title: IConverterSessionSetCharSet
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
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 032f071e18af3a89a2850cf2bd1e141f34bc86d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817169"
---
# <a name="iconvertersessionsetcharset"></a><span data-ttu-id="167b4-103">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="167b4-103">IConverterSession::SetCharSet</span></span>

  
  
<span data-ttu-id="167b4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="167b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="167b4-105">Especifica que un carácter opcional establece que la MAPI para el uso de convertidor MIME al convertir un mensaje MAPI a una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="167b4-105">Specifies an optional character set that the MAPI to MIME converter use when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a><span data-ttu-id="167b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="167b4-106">Parameters</span></span>

 <span data-ttu-id="167b4-107">_fApply_</span><span class="sxs-lookup"><span data-stu-id="167b4-107">_fApply_</span></span>
  
> <span data-ttu-id="167b4-108">[entrada] Indica si se debe usar un juego específico para la conversión.</span><span class="sxs-lookup"><span data-stu-id="167b4-108">[in] Indicates whether to use a specific character set for the conversion.</span></span> <span data-ttu-id="167b4-109">Establezca este parámetro en **true** para aplicar el juego de caracteres de las conversiones subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="167b4-109">Set this parameter to **true** to apply the character set in subsequent conversions.</span></span> <span data-ttu-id="167b4-110">Establezca este parámetro en **false** si ya no desea aplicar cualquier juego de caracteres específico y volver a los valores predeterminados para los mensajes subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="167b4-110">Set this parameter to **false** if you no longer want to apply any specific character set and return to the defaults for subsequent messages.</span></span> 
    
 <span data-ttu-id="167b4-111">_hcharset_</span><span class="sxs-lookup"><span data-stu-id="167b4-111">_hcharset_</span></span>
  
> <span data-ttu-id="167b4-112">[entrada] Un identificador de un juego de caracteres como se define en mimeole.h de correo de Windows.</span><span class="sxs-lookup"><span data-stu-id="167b4-112">[in] A handle to a character set as defined in mimeole.h of Windows Mail.</span></span> <span data-ttu-id="167b4-113">Especifique **null** para especificar que no desea aplicar cualquier juego de caracteres específico.</span><span class="sxs-lookup"><span data-stu-id="167b4-113">Specify **null** to specify that you do not want to apply any specific character set.</span></span> <span data-ttu-id="167b4-114">Para los valores que no son **null** , usar una función como [MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx) para obtener un identificador para el juego de caracteres.</span><span class="sxs-lookup"><span data-stu-id="167b4-114">For non- **null** values, use a function such as [MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx) to obtain a handle to the character set.</span></span> 
    
 <span data-ttu-id="167b4-115">_csetapplytype_</span><span class="sxs-lookup"><span data-stu-id="167b4-115">_csetapplytype_</span></span>
  
> <span data-ttu-id="167b4-116">[entrada] Indica cómo aplicar un juego de caracteres para convertir un mensaje, como se define en mimeole.h de correo de Windows.</span><span class="sxs-lookup"><span data-stu-id="167b4-116">[in] Indicates how to apply a character set to convert a message, as defined in mimeole.h of Windows Mail.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="167b4-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="167b4-117">Return value</span></span>

<span data-ttu-id="167b4-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="167b4-118">S_OK</span></span>
  
> <span data-ttu-id="167b4-119">La llamada a la función es correcta.</span><span class="sxs-lookup"><span data-stu-id="167b4-119">The function call is successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="167b4-120">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="167b4-120">MFCMAPI reference</span></span>

<span data-ttu-id="167b4-121">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="167b4-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="167b4-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="167b4-122">**File**</span></span>|<span data-ttu-id="167b4-123">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="167b4-123">**Function**</span></span>|<span data-ttu-id="167b4-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="167b4-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="167b4-125">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="167b4-125">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="167b4-126">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="167b4-126">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="167b4-127">MFCMAPI utiliza MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="167b4-127">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="167b4-128">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="167b4-128">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="167b4-129">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="167b4-129">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="167b4-130">MFCMAPI utiliza MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="167b4-130">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="167b4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="167b4-131">See also</span></span>



[<span data-ttu-id="167b4-132">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="167b4-132">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="167b4-133">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="167b4-133">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="167b4-134">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="167b4-134">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="167b4-135">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="167b4-135">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="167b4-136">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="167b4-136">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="167b4-137">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="167b4-137">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="167b4-138">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="167b4-138">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

