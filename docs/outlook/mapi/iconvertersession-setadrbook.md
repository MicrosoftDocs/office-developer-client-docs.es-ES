---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ae00fd0711b8fcae01db6a89da7607d79d8757c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584362"
---
# <a name="iconvertersessionsetadrbook"></a><span data-ttu-id="c5757-103">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="c5757-103">IConverterSession::SetAdrBook</span></span>

  
  
<span data-ttu-id="c5757-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5757-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5757-105">Especifica una libreta de direcciones MAPI opcional que usa la MAPI para el convertidor MIME para resolver direcciones ambiguas Cuando se convierte un mensaje MAPI a una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="c5757-105">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a><span data-ttu-id="c5757-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5757-106">Parameters</span></span>

 <span data-ttu-id="c5757-107">_Libreta personal de direcciones_</span><span class="sxs-lookup"><span data-stu-id="c5757-107">_pab_</span></span>
  
> <span data-ttu-id="c5757-108">[entrada] Puntero a un [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) interfaz que se utilizará en la conversión MIME de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c5757-108">[in] Pointer to an [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface to be used in the MAPI to MIME conversion.</span></span> <span data-ttu-id="c5757-109">Establezca este parámetro en **null** cuando ya no sea necesaria la libreta de direcciones; Esto libera la interfaz y restablece el convertidor a no utilizar cualquier libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c5757-109">Set this parameter to **null** when you no longer need the Address Book; this releases the interface and resets the converter to not using any Address Book.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c5757-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5757-110">Return value</span></span>

<span data-ttu-id="c5757-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="c5757-111">S_OK</span></span>
  
> <span data-ttu-id="c5757-112">La llamada a la función es correcta.</span><span class="sxs-lookup"><span data-stu-id="c5757-112">The function call is successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5757-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5757-113">Remarks</span></span>

<span data-ttu-id="c5757-114">Convertir una MAPI mensaje en secuencia MIME normalmente no requiere iniciar sesión en un perfil MAPI.</span><span class="sxs-lookup"><span data-stu-id="c5757-114">Converting a MAPI message to MIME stream generally does not require logging on to a MAPI profile.</span></span> <span data-ttu-id="c5757-115">Sin embargo, la especificación de una libreta de direcciones MAPI para la conversión requiere inicio de sesión a un perfil para obtener la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c5757-115">However, specifying a MAPI Address Book for conversion requires logging on to a profile to obtain the Address Book.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c5757-116">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c5757-116">MFCMAPI reference</span></span>

<span data-ttu-id="c5757-117">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="c5757-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c5757-118">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="c5757-118">**File**</span></span>|<span data-ttu-id="c5757-119">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="c5757-119">**Function**</span></span>|<span data-ttu-id="c5757-120">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="c5757-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c5757-121">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="c5757-121">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="c5757-122">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="c5757-122">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="c5757-123">MFCMAPI utiliza MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="c5757-123">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="c5757-124">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="c5757-124">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="c5757-125">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="c5757-125">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="c5757-126">MFCMAPI utiliza MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="c5757-126">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5757-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5757-127">See also</span></span>



[<span data-ttu-id="c5757-128">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c5757-128">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="c5757-129">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="c5757-129">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="c5757-130">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="c5757-130">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="c5757-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="c5757-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="c5757-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="c5757-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="c5757-133">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="c5757-133">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="c5757-134">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="c5757-134">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

