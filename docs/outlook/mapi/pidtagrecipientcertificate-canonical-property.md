---
title: Propiedad canónica PidTagRecipientCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 464db3d360f6e872ac28f8d7cbec842d8b521f7e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585118"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="46431-103">Propiedad canónica PidTagRecipientCertificate</span><span class="sxs-lookup"><span data-stu-id="46431-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="46431-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46431-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46431-105">Contiene el certificado ASN.1 del destinatario de un mensaje para su uso en un informe.</span><span class="sxs-lookup"><span data-stu-id="46431-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46431-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="46431-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46431-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="46431-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="46431-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="46431-108">Identifier:</span></span>  <br/> |<span data-ttu-id="46431-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="46431-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="46431-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="46431-110">Data type:</span></span>  <br/> |<span data-ttu-id="46431-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="46431-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="46431-112">Área:</span><span class="sxs-lookup"><span data-stu-id="46431-112">Area:</span></span>  <br/> |<span data-ttu-id="46431-113">Destinatario MAPI</span><span class="sxs-lookup"><span data-stu-id="46431-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46431-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46431-114">Remarks</span></span>

<span data-ttu-id="46431-115">Esta propiedad es una copia de la propiedad del destinatario **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) para su uso en un informe.</span><span class="sxs-lookup"><span data-stu-id="46431-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="46431-116">Se puede usar para probar al autor de la que el destinatario realmente ha recibido el mensaje, que no necesariamente indica un informe de entrega.</span><span class="sxs-lookup"><span data-stu-id="46431-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="46431-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="46431-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="46431-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="46431-118">Header files</span></span>

<span data-ttu-id="46431-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46431-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="46431-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="46431-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="46431-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="46431-121">Mapitags.h</span></span>
  
> <span data-ttu-id="46431-122">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="46431-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46431-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="46431-123">See also</span></span>



[<span data-ttu-id="46431-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="46431-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46431-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="46431-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46431-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="46431-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46431-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="46431-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

