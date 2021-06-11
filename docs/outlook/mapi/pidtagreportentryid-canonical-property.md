---
title: Propiedad canónica PidTagReportEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportEntryId
api_type:
- COM
ms.assetid: ea2bcc06-0089-4999-b115-06a14de4a0f1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3b4432650d5c9fc77c4db0bc9aed4234d85e7fdf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346322"
---
# <a name="pidtagreportentryid-canonical-property"></a><span data-ttu-id="c9966-103">Propiedad canónica PidTagReportEntryId</span><span class="sxs-lookup"><span data-stu-id="c9966-103">PidTagReportEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c9966-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9966-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9966-105">Contiene el identificador de entrada del destinatario que debe recibir informes para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="c9966-105">Contains the entry identifier for the recipient who should receive reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9966-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c9966-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9966-107">PR_REPORT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c9966-107">PR_REPORT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c9966-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c9966-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9966-109">0x0045</span><span class="sxs-lookup"><span data-stu-id="c9966-109">0x0045</span></span>  <br/> |
|<span data-ttu-id="c9966-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c9966-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9966-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c9966-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c9966-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c9966-112">Area:</span></span>  <br/> |<span data-ttu-id="c9966-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="c9966-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9966-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9966-114">Remarks</span></span>

<span data-ttu-id="c9966-115">Esta propiedad es una de las propiedades de dirección para el destinatario al que el remitente ha delegado recibir los informes generados para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="c9966-115">This property is one of the address properties for the recipient who the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="c9966-116">Una aplicación cliente que debe enrutar los informes a otro usuario debe establecer esta propiedad en el momento del envío del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c9966-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="c9966-117">Si no se establece, los informes se envían al remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c9966-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c9966-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9966-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c9966-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="c9966-119">Protocol specifications</span></span>

<span data-ttu-id="c9966-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9966-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9966-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="c9966-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c9966-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9966-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9966-123">Especifica las propiedades y las operaciones permitidas en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c9966-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c9966-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c9966-124">Header files</span></span>

<span data-ttu-id="c9966-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9966-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9966-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c9966-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9966-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c9966-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c9966-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c9966-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9966-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9966-129">See also</span></span>



[<span data-ttu-id="c9966-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c9966-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9966-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c9966-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9966-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c9966-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9966-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c9966-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

