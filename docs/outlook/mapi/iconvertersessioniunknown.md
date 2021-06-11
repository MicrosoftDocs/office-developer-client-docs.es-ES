---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432320"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="ace9e-103">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ace9e-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="ace9e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ace9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ace9e-105">Permite conversiones entre objetos MIME y mensajes MAPI.</span><span class="sxs-lookup"><span data-stu-id="ace9e-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="ace9e-106">Esto puede ser útil para transportar mensajes a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="ace9e-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ace9e-107">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="ace9e-107">Provided by:</span></span>  <br/> |<span data-ttu-id="ace9e-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="ace9e-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="ace9e-109">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="ace9e-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ace9e-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="ace9e-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ace9e-111">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="ace9e-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ace9e-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="ace9e-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="ace9e-113">Especifica una libreta de direcciones MAPI opcional que el convertidor MAPI a MIME usa para resolver direcciones ambiguas al convertir un mensaje MAPI en una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="ace9e-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="ace9e-114">**[SetEncoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="ace9e-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="ace9e-115">Inicializa la codificación que se usará durante la conversión.</span><span class="sxs-lookup"><span data-stu-id="ace9e-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="ace9e-116">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="ace9e-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="ace9e-117">*No se admite ni se documenta.*</span><span class="sxs-lookup"><span data-stu-id="ace9e-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="ace9e-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="ace9e-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="ace9e-119">Convierte una secuencia MIME en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="ace9e-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="ace9e-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="ace9e-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="ace9e-121">Convierte un mensaje MAPI en una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="ace9e-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="ace9e-122">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="ace9e-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="ace9e-123">*No se admite ni se documenta.*</span><span class="sxs-lookup"><span data-stu-id="ace9e-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="ace9e-124">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="ace9e-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="ace9e-125">*No se admite ni se documenta.*</span><span class="sxs-lookup"><span data-stu-id="ace9e-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="ace9e-126">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="ace9e-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="ace9e-127">*No se admite ni se documenta.*</span><span class="sxs-lookup"><span data-stu-id="ace9e-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="ace9e-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="ace9e-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="ace9e-129">Establece el ancho de ajuste de texto de una secuencia MIME que devuelve el convertidor **en MAPIToMIMEStm**.</span><span class="sxs-lookup"><span data-stu-id="ace9e-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="ace9e-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ace9e-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="ace9e-131">Establece el formato en el que el convertidor devuelve una secuencia MIME **en MAPIToMIMEStm**.</span><span class="sxs-lookup"><span data-stu-id="ace9e-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="ace9e-132">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="ace9e-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="ace9e-133">*No se admite ni se documenta.*</span><span class="sxs-lookup"><span data-stu-id="ace9e-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="ace9e-134">**[SetCharSet](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="ace9e-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="ace9e-135">Especifica un conjunto de caracteres opcional que usa el convertidor MAPI a MIME al convertir un mensaje MAPI en una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="ace9e-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ace9e-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ace9e-136">Remarks</span></span>

<span data-ttu-id="ace9e-137">Llama **a SetEncoding antes** de usar **MAPIToMIMEStm para** realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="ace9e-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ace9e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ace9e-138">See also</span></span>



[<span data-ttu-id="ace9e-139">Información sobre la API de conversión de MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="ace9e-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="ace9e-140">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ace9e-140">MAPI Constants</span></span>](mapi-constants.md)

