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
ms.openlocfilehash: 7645208e6a0256957deb3a71ba3e04ad125a6b61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429197"
---
# <a name="iconvertersessionsetadrbook"></a><span data-ttu-id="01f5a-103">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="01f5a-103">IConverterSession::SetAdrBook</span></span>

  
  
<span data-ttu-id="01f5a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01f5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01f5a-105">Especifica una libreta de direcciones MAPI opcional que el convertidor MAPI a MIME usa para resolver direcciones ambiguas al convertir un mensaje MAPI en una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="01f5a-105">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a><span data-ttu-id="01f5a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="01f5a-106">Parameters</span></span>

 <span data-ttu-id="01f5a-107">_pab_</span><span class="sxs-lookup"><span data-stu-id="01f5a-107">_pab_</span></span>
  
> <span data-ttu-id="01f5a-108">[in] Puntero a una [interfaz IAddrBook : IMAPIProp](iaddrbookimapiprop.md) que se usará en la conversión MAPI a MIME.</span><span class="sxs-lookup"><span data-stu-id="01f5a-108">[in] Pointer to an [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface to be used in the MAPI to MIME conversion.</span></span> <span data-ttu-id="01f5a-109">Establezca este parámetro en **null** cuando ya no necesite la libreta de direcciones; esto libera la interfaz y restablece el convertidor para que no use ninguna libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="01f5a-109">Set this parameter to **null** when you no longer need the Address Book; this releases the interface and resets the converter to not using any Address Book.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="01f5a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01f5a-110">Return value</span></span>

<span data-ttu-id="01f5a-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="01f5a-111">S_OK</span></span>
  
> <span data-ttu-id="01f5a-112">La llamada a la función se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="01f5a-112">The function call is successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01f5a-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01f5a-113">Remarks</span></span>

<span data-ttu-id="01f5a-114">Por lo general, la conversión de un mensaje MAPI a una secuencia MIME no requiere iniciar sesión en un perfil MAPI.</span><span class="sxs-lookup"><span data-stu-id="01f5a-114">Converting a MAPI message to MIME stream generally does not require logging on to a MAPI profile.</span></span> <span data-ttu-id="01f5a-115">Sin embargo, para especificar una libreta de direcciones MAPI para la conversión es necesario iniciar sesión en un perfil para obtener la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="01f5a-115">However, specifying a MAPI Address Book for conversion requires logging on to a profile to obtain the Address Book.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="01f5a-116">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="01f5a-116">MFCMAPI reference</span></span>

<span data-ttu-id="01f5a-117">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="01f5a-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="01f5a-118">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="01f5a-118">**File**</span></span>|<span data-ttu-id="01f5a-119">**Función**</span><span class="sxs-lookup"><span data-stu-id="01f5a-119">**Function**</span></span>|<span data-ttu-id="01f5a-120">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="01f5a-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="01f5a-121">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="01f5a-121">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="01f5a-122">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="01f5a-122">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="01f5a-123">MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="01f5a-123">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="01f5a-124">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="01f5a-124">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="01f5a-125">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="01f5a-125">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="01f5a-126">MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="01f5a-126">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01f5a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="01f5a-127">See also</span></span>



[<span data-ttu-id="01f5a-128">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="01f5a-128">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="01f5a-129">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="01f5a-129">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="01f5a-130">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="01f5a-130">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="01f5a-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="01f5a-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="01f5a-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="01f5a-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="01f5a-133">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="01f5a-133">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="01f5a-134">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="01f5a-134">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

