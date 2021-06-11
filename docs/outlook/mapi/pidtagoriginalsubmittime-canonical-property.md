---
title: Propiedad canónica PidTagOriginalSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubmitTime
api_type:
- COM
ms.assetid: 2e027c0c-2370-437a-ad98-2bbb5e41e525
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 07aea33f54a29d497646b62f1f8bd96a383cbd7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341051"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="0e6ff-103">Propiedad canónica PidTagOriginalSubmitTime</span><span class="sxs-lookup"><span data-stu-id="0e6ff-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="0e6ff-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e6ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e6ff-105">Contiene la fecha y hora de envío originales del mensaje en el informe.</span><span class="sxs-lookup"><span data-stu-id="0e6ff-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e6ff-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0e6ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e6ff-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="0e6ff-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="0e6ff-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0e6ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e6ff-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="0e6ff-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="0e6ff-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0e6ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e6ff-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="0e6ff-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="0e6ff-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0e6ff-112">Area:</span></span>  <br/> |<span data-ttu-id="0e6ff-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="0e6ff-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e6ff-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e6ff-114">Remarks</span></span>

<span data-ttu-id="0e6ff-115">En el primer envío de un mensaje, una aplicación cliente debe establecer esta propiedad en el valor de la propiedad **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0e6ff-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="0e6ff-116">No se cambia cuando se reenvía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0e6ff-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="0e6ff-117">Esto se usa solo en informes.</span><span class="sxs-lookup"><span data-stu-id="0e6ff-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0e6ff-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e6ff-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e6ff-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="0e6ff-119">Protocol specifications</span></span>

<span data-ttu-id="0e6ff-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e6ff-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e6ff-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="0e6ff-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e6ff-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e6ff-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e6ff-123">Especifica las propiedades y las operaciones permitidas en objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0e6ff-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e6ff-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0e6ff-124">Header files</span></span>

<span data-ttu-id="0e6ff-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e6ff-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e6ff-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0e6ff-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e6ff-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0e6ff-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0e6ff-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0e6ff-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e6ff-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e6ff-129">See also</span></span>



[<span data-ttu-id="0e6ff-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0e6ff-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e6ff-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0e6ff-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e6ff-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0e6ff-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e6ff-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0e6ff-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

