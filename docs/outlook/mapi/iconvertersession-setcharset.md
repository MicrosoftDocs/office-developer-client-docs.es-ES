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
ms.openlocfilehash: 14b2904e57852c564395f4b27c9d5270afd1454a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336662"
---
# <a name="iconvertersessionsetcharset"></a><span data-ttu-id="ca951-103">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="ca951-103">IConverterSession::SetCharSet</span></span>

  
  
<span data-ttu-id="ca951-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca951-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca951-105">Especifica un conjunto de caracteres opcional que el convertidor MAPI a MIME usa al convertir un mensaje MAPI en una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="ca951-105">Specifies an optional character set that the MAPI to MIME converter use when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a><span data-ttu-id="ca951-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca951-106">Parameters</span></span>

 <span data-ttu-id="ca951-107">_fApply_</span><span class="sxs-lookup"><span data-stu-id="ca951-107">_fApply_</span></span>
  
> <span data-ttu-id="ca951-108">[in] Indica si se va a usar un juego de caracteres específico para la conversión.</span><span class="sxs-lookup"><span data-stu-id="ca951-108">[in] Indicates whether to use a specific character set for the conversion.</span></span> <span data-ttu-id="ca951-109">Establezca este parámetro en **true para** aplicar el juego de caracteres en conversiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ca951-109">Set this parameter to **true** to apply the character set in subsequent conversions.</span></span> <span data-ttu-id="ca951-110">Establezca este parámetro en **false** si ya no desea aplicar ningún juego de caracteres específico y volver a los valores predeterminados para los mensajes posteriores.</span><span class="sxs-lookup"><span data-stu-id="ca951-110">Set this parameter to **false** if you no longer want to apply any specific character set and return to the defaults for subsequent messages.</span></span> 
    
 <span data-ttu-id="ca951-111">_hcharset_</span><span class="sxs-lookup"><span data-stu-id="ca951-111">_hcharset_</span></span>
  
> <span data-ttu-id="ca951-112">[in] Identificador de un conjunto de caracteres definido en mimeole.h de Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="ca951-112">[in] A handle to a character set as defined in mimeole.h of Windows Mail.</span></span> <span data-ttu-id="ca951-113">Especifique **null** para especificar que no desea aplicar ningún juego de caracteres específico.</span><span class="sxs-lookup"><span data-stu-id="ca951-113">Specify **null** to specify that you do not want to apply any specific character set.</span></span> <span data-ttu-id="ca951-114">Para valores **que no son nulos,** use una función como [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) para obtener un identificador para el juego de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ca951-114">For non- **null** values, use a function such as [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) to obtain a handle to the character set.</span></span> 
    
 <span data-ttu-id="ca951-115">_csetapplytype_</span><span class="sxs-lookup"><span data-stu-id="ca951-115">_csetapplytype_</span></span>
  
> <span data-ttu-id="ca951-116">[in] Indica cómo aplicar un juego de caracteres para convertir un mensaje, tal como se define en mimeole.h de Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="ca951-116">[in] Indicates how to apply a character set to convert a message, as defined in mimeole.h of Windows Mail.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca951-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca951-117">Return value</span></span>

<span data-ttu-id="ca951-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca951-118">S_OK</span></span>
  
> <span data-ttu-id="ca951-119">La llamada a la función se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="ca951-119">The function call is successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="ca951-120">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ca951-120">MFCMAPI reference</span></span>

<span data-ttu-id="ca951-121">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ca951-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ca951-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ca951-122">**File**</span></span>|<span data-ttu-id="ca951-123">**Función**</span><span class="sxs-lookup"><span data-stu-id="ca951-123">**Function**</span></span>|<span data-ttu-id="ca951-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ca951-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ca951-125">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="ca951-125">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="ca951-126">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="ca951-126">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="ca951-127">MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="ca951-127">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="ca951-128">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="ca951-128">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="ca951-129">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="ca951-129">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="ca951-130">MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="ca951-130">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca951-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca951-131">See also</span></span>



[<span data-ttu-id="ca951-132">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca951-132">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="ca951-133">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="ca951-133">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="ca951-134">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="ca951-134">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="ca951-135">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="ca951-135">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="ca951-136">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="ca951-136">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="ca951-137">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="ca951-137">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="ca951-138">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="ca951-138">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

