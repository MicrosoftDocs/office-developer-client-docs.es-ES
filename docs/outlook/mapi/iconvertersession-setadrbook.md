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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326897"
---
# <a name="iconvertersessionsetadrbook"></a><span data-ttu-id="cd05e-103">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="cd05e-103">IConverterSession::SetAdrBook</span></span>

  
  
<span data-ttu-id="cd05e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd05e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd05e-105">Especifica una libreta de direcciones MAPI opcional que el convertidor de MAPI a MIME utiliza para resolver direcciones ambiguas al convertir un mensaje MAPI en una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="cd05e-105">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a><span data-ttu-id="cd05e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd05e-106">Parameters</span></span>

 <span data-ttu-id="cd05e-107">_LPD_</span><span class="sxs-lookup"><span data-stu-id="cd05e-107">_pab_</span></span>
  
> <span data-ttu-id="cd05e-108">a Puntero a una interfaz [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) que se va a usar en la conversión de MAPI a MIME.</span><span class="sxs-lookup"><span data-stu-id="cd05e-108">[in] Pointer to an [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface to be used in the MAPI to MIME conversion.</span></span> <span data-ttu-id="cd05e-109">Establezca este parámetro en **null** cuando ya no necesite la libreta de direcciones; Esto libera la interfaz y restablece el convertidor a no usar ninguna libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="cd05e-109">Set this parameter to **null** when you no longer need the Address Book; this releases the interface and resets the converter to not using any Address Book.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cd05e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd05e-110">Return value</span></span>

<span data-ttu-id="cd05e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd05e-111">S_OK</span></span>
  
> <span data-ttu-id="cd05e-112">La llamada a la función es correcta.</span><span class="sxs-lookup"><span data-stu-id="cd05e-112">The function call is successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cd05e-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd05e-113">Remarks</span></span>

<span data-ttu-id="cd05e-114">Por lo general, para convertir un mensaje MAPI en una secuencia MIME no es necesario iniciar sesión en un perfil MAPI.</span><span class="sxs-lookup"><span data-stu-id="cd05e-114">Converting a MAPI message to MIME stream generally does not require logging on to a MAPI profile.</span></span> <span data-ttu-id="cd05e-115">Sin embargo, si se especifica una libreta de direcciones MAPI para la conversión, es necesario iniciar sesión en un perfil para obtener la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="cd05e-115">However, specifying a MAPI Address Book for conversion requires logging on to a profile to obtain the Address Book.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cd05e-116">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cd05e-116">MFCMAPI reference</span></span>

<span data-ttu-id="cd05e-117">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="cd05e-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cd05e-118">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="cd05e-118">**File**</span></span>|<span data-ttu-id="cd05e-119">**Función**</span><span class="sxs-lookup"><span data-stu-id="cd05e-119">**Function**</span></span>|<span data-ttu-id="cd05e-120">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="cd05e-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cd05e-121">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="cd05e-121">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="cd05e-122">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="cd05e-122">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="cd05e-123">MFCMAPI usa MimeToMAPI para convertir un archivo EML en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="cd05e-123">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="cd05e-124">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="cd05e-124">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="cd05e-125">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="cd05e-125">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="cd05e-126">MFCMAPI usa MAPIToMIMEStm para convertir un mensaje MAPI en un archivo EML.</span><span class="sxs-lookup"><span data-stu-id="cd05e-126">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd05e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd05e-127">See also</span></span>



[<span data-ttu-id="cd05e-128">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd05e-128">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="cd05e-129">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="cd05e-129">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="cd05e-130">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="cd05e-130">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="cd05e-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="cd05e-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="cd05e-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="cd05e-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="cd05e-133">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="cd05e-133">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="cd05e-134">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="cd05e-134">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

