---
title: Propiedad canónica PidTagRecipientNumberForAdvice
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ac4da2d4082cac632548594411528b7bf1d6dc64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820031"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="aab83-103">Propiedad canónica PidTagRecipientNumberForAdvice</span><span class="sxs-lookup"><span data-stu-id="aab83-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="aab83-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aab83-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aab83-105">Esta propiedad contiene el número de teléfono del destinatario de un mensaje al que llamar para advertir de la entrega física de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="aab83-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aab83-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="aab83-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aab83-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="aab83-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="aab83-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="aab83-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aab83-109">0x0C14</span><span class="sxs-lookup"><span data-stu-id="aab83-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="aab83-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="aab83-110">Data type:</span></span>  <br/> |<span data-ttu-id="aab83-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aab83-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="aab83-112">Área:</span><span class="sxs-lookup"><span data-stu-id="aab83-112">Area:</span></span>  <br/> |<span data-ttu-id="aab83-113">Destinatario MAPI</span><span class="sxs-lookup"><span data-stu-id="aab83-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aab83-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aab83-114">Remarks</span></span>

<span data-ttu-id="aab83-115">Estas propiedades están diseñadas para usarse junto con la entrega a un destino físico, en lugar de un buzón de correo electrónico, cuando no se espera que el destinatario humano estar presente en la entrega.</span><span class="sxs-lookup"><span data-stu-id="aab83-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="aab83-116">Un ejemplo es el número de teléfono en una página de portada de fax.</span><span class="sxs-lookup"><span data-stu-id="aab83-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aab83-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="aab83-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="aab83-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="aab83-118">Header files</span></span>

<span data-ttu-id="aab83-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aab83-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="aab83-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="aab83-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="aab83-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aab83-121">Mapitags.h</span></span>
  
> <span data-ttu-id="aab83-122">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="aab83-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aab83-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="aab83-123">See also</span></span>



[<span data-ttu-id="aab83-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="aab83-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aab83-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="aab83-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aab83-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="aab83-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aab83-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="aab83-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

