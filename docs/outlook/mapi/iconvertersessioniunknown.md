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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a89b1a93b2b03f97426a3988739e9b0d8411f113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817180"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="e4fbe-103">IConverterSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e4fbe-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="e4fbe-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4fbe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4fbe-105">Permite que las conversiones entre objetos MIME y los mensajes MAPI.</span><span class="sxs-lookup"><span data-stu-id="e4fbe-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="e4fbe-106">Esto puede resultar útil en transportar los mensajes a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="e4fbe-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e4fbe-107">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="e4fbe-107">Provided by:</span></span>  <br/> |<span data-ttu-id="e4fbe-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="e4fbe-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="e4fbe-109">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="e4fbe-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e4fbe-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="e4fbe-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e4fbe-111">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="e4fbe-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e4fbe-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="e4fbe-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="e4fbe-113">Especifica una libreta de direcciones MAPI opcional que usa la MAPI para el convertidor MIME para resolver direcciones ambiguas Cuando se convierte un mensaje MAPI a una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="e4fbe-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="e4fbe-114">**[SetEncoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="e4fbe-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="e4fbe-115">Inicializa la codificación para usar durante la conversión.</span><span class="sxs-lookup"><span data-stu-id="e4fbe-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="e4fbe-116">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="e4fbe-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e4fbe-117">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="e4fbe-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="e4fbe-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="e4fbe-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="e4fbe-119">Convierte una secuencia MIME en un mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="e4fbe-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="e4fbe-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="e4fbe-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="e4fbe-121">Convierte un mensaje MAPI a una secuencia MIME.</span><span class="sxs-lookup"><span data-stu-id="e4fbe-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="e4fbe-122">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="e4fbe-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e4fbe-123">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="e4fbe-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e4fbe-124">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="e4fbe-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e4fbe-125">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="e4fbe-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e4fbe-126">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="e4fbe-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e4fbe-127">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="e4fbe-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="e4fbe-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="e4fbe-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="e4fbe-129">Establece el ancho de una secuencia de MIME que devuelve el convertidor en **MAPIToMIMEStm**de ajuste de texto.</span><span class="sxs-lookup"><span data-stu-id="e4fbe-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="e4fbe-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="e4fbe-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="e4fbe-131">Establece el formato que el convertidor devuelve una secuencia MIME en **MAPIToMIMEStm**.</span><span class="sxs-lookup"><span data-stu-id="e4fbe-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="e4fbe-132">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="e4fbe-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e4fbe-133">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="e4fbe-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="e4fbe-134">**[SetCharSet](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="e4fbe-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="e4fbe-135">Especifica que la MAPI para el convertidor MIME utiliza cuando se convierte un mensaje MAPI a una secuencia MIME del conjunto de un carácter opcional.</span><span class="sxs-lookup"><span data-stu-id="e4fbe-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4fbe-136">Notas</span><span class="sxs-lookup"><span data-stu-id="e4fbe-136">Remarks</span></span>

<span data-ttu-id="e4fbe-137">Llame a **SetEncoding** antes de usar **MAPIToMIMEStm** para llevar a cabo la conversión.</span><span class="sxs-lookup"><span data-stu-id="e4fbe-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e4fbe-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="e4fbe-138">See also</span></span>



[<span data-ttu-id="e4fbe-139">Acerca de la API de conversión de MIME a MAPI</span><span class="sxs-lookup"><span data-stu-id="e4fbe-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="e4fbe-140">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e4fbe-140">MAPI Constants</span></span>](mapi-constants.md)

