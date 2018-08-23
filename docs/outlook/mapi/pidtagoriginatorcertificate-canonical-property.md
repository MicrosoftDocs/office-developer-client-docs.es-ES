---
title: Propiedad canónica PidTagOriginatorCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorCertificate
api_type:
- COM
ms.assetid: 65f890d8-9d25-408e-ab29-89991278b92d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 966af9b3b3cbe52031402450be324ab6821d53ac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586581"
---
# <a name="pidtagoriginatorcertificate-canonical-property"></a><span data-ttu-id="c24f2-103">Propiedad canónica PidTagOriginatorCertificate</span><span class="sxs-lookup"><span data-stu-id="c24f2-103">PidTagOriginatorCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="c24f2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c24f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c24f2-105">Contiene un certificado ASN.1 para el autor del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c24f2-105">Contains an ASN.1 certificate for the message originator.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c24f2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c24f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c24f2-107">PR_ORIGINATOR_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="c24f2-107">PR_ORIGINATOR_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="c24f2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c24f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c24f2-109">0 x 0022</span><span class="sxs-lookup"><span data-stu-id="c24f2-109">0x0022</span></span>  <br/> |
|<span data-ttu-id="c24f2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c24f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="c24f2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c24f2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c24f2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c24f2-112">Area:</span></span>  <br/> |<span data-ttu-id="c24f2-113">MIME</span><span class="sxs-lookup"><span data-stu-id="c24f2-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c24f2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c24f2-114">Remarks</span></span>

<span data-ttu-id="c24f2-115">Esta propiedad es una copia de propiedad del autor de la de **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c24f2-115">This property is a copy of the originator's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c24f2-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c24f2-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c24f2-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c24f2-117">Header files</span></span>

<span data-ttu-id="c24f2-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c24f2-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="c24f2-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c24f2-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="c24f2-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c24f2-120">Mapitags.h</span></span>
  
> <span data-ttu-id="c24f2-121">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c24f2-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c24f2-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c24f2-122">See also</span></span>



[<span data-ttu-id="c24f2-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c24f2-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c24f2-124">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c24f2-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c24f2-125">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c24f2-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c24f2-126">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c24f2-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

