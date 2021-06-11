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
ms.openlocfilehash: c659b77767fddc4c783732082c2eb65c68af8dbf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431669"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="a683b-103">Propiedad canónica PidTagRecipientCertificate</span><span class="sxs-lookup"><span data-stu-id="a683b-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="a683b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a683b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a683b-105">Contiene el certificado ASN.1 de un destinatario de mensaje para su uso en un informe.</span><span class="sxs-lookup"><span data-stu-id="a683b-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a683b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a683b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a683b-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="a683b-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="a683b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a683b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a683b-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="a683b-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="a683b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a683b-110">Data type:</span></span>  <br/> |<span data-ttu-id="a683b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a683b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a683b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a683b-112">Area:</span></span>  <br/> |<span data-ttu-id="a683b-113">Destinatario MAPI</span><span class="sxs-lookup"><span data-stu-id="a683b-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a683b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a683b-114">Remarks</span></span>

<span data-ttu-id="a683b-115">Esta propiedad es una copia de la propiedad PR_USER_CERTIFICATE **del** destinatario ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) para su uso en un informe.</span><span class="sxs-lookup"><span data-stu-id="a683b-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="a683b-116">Se puede usar para demostrar al originador que el destinatario recibió realmente el mensaje, lo que un informe de entrega no indica necesariamente.</span><span class="sxs-lookup"><span data-stu-id="a683b-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a683b-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a683b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a683b-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a683b-118">Header files</span></span>

<span data-ttu-id="a683b-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a683b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="a683b-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a683b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="a683b-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a683b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="a683b-122">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="a683b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a683b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a683b-123">See also</span></span>



[<span data-ttu-id="a683b-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a683b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a683b-125">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a683b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a683b-126">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a683b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a683b-127">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="a683b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

