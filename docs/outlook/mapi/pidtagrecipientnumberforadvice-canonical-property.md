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
ms.openlocfilehash: 79ef85955f15e0ca829ac6f206dddc17031b0562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420643"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="4fa37-103">Propiedad canónica PidTagRecipientNumberForAdvice</span><span class="sxs-lookup"><span data-stu-id="4fa37-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="4fa37-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fa37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fa37-105">Esta propiedad contiene el número de teléfono de un destinatario de mensaje al que se llama para informar de la entrega física de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4fa37-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4fa37-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4fa37-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4fa37-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="4fa37-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="4fa37-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4fa37-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4fa37-109">0x0C14</span><span class="sxs-lookup"><span data-stu-id="4fa37-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="4fa37-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4fa37-110">Data type:</span></span>  <br/> |<span data-ttu-id="4fa37-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4fa37-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4fa37-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4fa37-112">Area:</span></span>  <br/> |<span data-ttu-id="4fa37-113">Destinatario MAPI</span><span class="sxs-lookup"><span data-stu-id="4fa37-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fa37-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4fa37-114">Remarks</span></span>

<span data-ttu-id="4fa37-115">Estas propiedades están pensadas para usarse junto con la entrega a un destino físico, en lugar de a un buzón de correo electrónico, cuando no se espera que el destinatario humano esté presente en la entrega.</span><span class="sxs-lookup"><span data-stu-id="4fa37-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="4fa37-116">Un ejemplo es el número de teléfono en una hoja de portada de fax.</span><span class="sxs-lookup"><span data-stu-id="4fa37-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4fa37-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4fa37-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4fa37-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4fa37-118">Header files</span></span>

<span data-ttu-id="4fa37-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4fa37-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4fa37-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4fa37-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4fa37-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4fa37-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4fa37-122">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="4fa37-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4fa37-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="4fa37-123">See also</span></span>



[<span data-ttu-id="4fa37-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4fa37-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4fa37-125">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="4fa37-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4fa37-126">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4fa37-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4fa37-127">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4fa37-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

