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
ms.openlocfilehash: d367073de2134ff766cbae3d4f6bcfa30b862122
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351110"
---
# <a name="pidtagoriginatorcertificate-canonical-property"></a><span data-ttu-id="a08f8-103">Propiedad canónica PidTagOriginatorCertificate</span><span class="sxs-lookup"><span data-stu-id="a08f8-103">PidTagOriginatorCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="a08f8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a08f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a08f8-105">Contiene un certificado ASN. 1 para el autor del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a08f8-105">Contains an ASN.1 certificate for the message originator.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a08f8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a08f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a08f8-107">PR_ORIGINATOR_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="a08f8-107">PR_ORIGINATOR_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="a08f8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a08f8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a08f8-109">0x0022</span><span class="sxs-lookup"><span data-stu-id="a08f8-109">0x0022</span></span>  <br/> |
|<span data-ttu-id="a08f8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a08f8-110">Data type:</span></span>  <br/> |<span data-ttu-id="a08f8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a08f8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a08f8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a08f8-112">Area:</span></span>  <br/> |<span data-ttu-id="a08f8-113">MIME</span><span class="sxs-lookup"><span data-stu-id="a08f8-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a08f8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a08f8-114">Remarks</span></span>

<span data-ttu-id="a08f8-115">Esta propiedad es una copia de la propiedad **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) del autor.</span><span class="sxs-lookup"><span data-stu-id="a08f8-115">This property is a copy of the originator's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a08f8-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a08f8-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a08f8-117">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a08f8-117">Header files</span></span>

<span data-ttu-id="a08f8-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a08f8-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="a08f8-119">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a08f8-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="a08f8-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a08f8-120">Mapitags.h</span></span>
  
> <span data-ttu-id="a08f8-121">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a08f8-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a08f8-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a08f8-122">See also</span></span>



[<span data-ttu-id="a08f8-123">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a08f8-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a08f8-124">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="a08f8-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a08f8-125">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a08f8-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a08f8-126">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="a08f8-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

