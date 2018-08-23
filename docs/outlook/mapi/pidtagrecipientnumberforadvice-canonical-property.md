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
ms.openlocfilehash: 3f23a332ee6778f71ce0809dfae8c0b6a92246a8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595149"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="06c0a-103">Propiedad canónica PidTagRecipientNumberForAdvice</span><span class="sxs-lookup"><span data-stu-id="06c0a-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="06c0a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06c0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06c0a-105">Esta propiedad contiene el número de teléfono del destinatario de un mensaje al que llamar para advertir de la entrega física de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="06c0a-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06c0a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="06c0a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06c0a-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="06c0a-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="06c0a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="06c0a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06c0a-109">0x0C14</span><span class="sxs-lookup"><span data-stu-id="06c0a-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="06c0a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="06c0a-110">Data type:</span></span>  <br/> |<span data-ttu-id="06c0a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="06c0a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="06c0a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="06c0a-112">Area:</span></span>  <br/> |<span data-ttu-id="06c0a-113">Destinatario MAPI</span><span class="sxs-lookup"><span data-stu-id="06c0a-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06c0a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="06c0a-114">Remarks</span></span>

<span data-ttu-id="06c0a-115">Estas propiedades están diseñadas para usarse junto con la entrega a un destino físico, en lugar de un buzón de correo electrónico, cuando no se espera que el destinatario humano estar presente en la entrega.</span><span class="sxs-lookup"><span data-stu-id="06c0a-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="06c0a-116">Un ejemplo es el número de teléfono en una página de portada de fax.</span><span class="sxs-lookup"><span data-stu-id="06c0a-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="06c0a-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="06c0a-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="06c0a-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="06c0a-118">Header files</span></span>

<span data-ttu-id="06c0a-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06c0a-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="06c0a-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="06c0a-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="06c0a-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06c0a-121">Mapitags.h</span></span>
  
> <span data-ttu-id="06c0a-122">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="06c0a-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06c0a-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="06c0a-123">See also</span></span>



[<span data-ttu-id="06c0a-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="06c0a-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06c0a-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="06c0a-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06c0a-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="06c0a-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06c0a-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="06c0a-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

