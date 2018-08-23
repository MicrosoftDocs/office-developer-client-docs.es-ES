---
title: Propiedad canónica PidTagReportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportName
api_type:
- COM
ms.assetid: 4ec3100f-7cf1-4702-b326-e6da586a7bb2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3c1a848eec84c7d81792a95baa3f47fa6779e95f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569585"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="e66a2-103">Propiedad canónica PidTagReportName</span><span class="sxs-lookup"><span data-stu-id="e66a2-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="e66a2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e66a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e66a2-105">Contiene el nombre para mostrar para el destinatario que debería obtener informes para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="e66a2-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e66a2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e66a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e66a2-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e66a2-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e66a2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e66a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e66a2-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="e66a2-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="e66a2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e66a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="e66a2-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e66a2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e66a2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e66a2-112">Area:</span></span>  <br/> |<span data-ttu-id="e66a2-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="e66a2-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e66a2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e66a2-114">Remarks</span></span>

<span data-ttu-id="e66a2-115">Estas propiedades son ejemplos de las propiedades de dirección para el destinatario que el remitente ha delegado para recibir los informes generados para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="e66a2-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="e66a2-116">Una aplicación cliente que se debe enrutar informes a otro usuario debe establecer estas propiedades en tiempo de envío de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e66a2-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="e66a2-117">Si no se establecen, los informes se envían al remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e66a2-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e66a2-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e66a2-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e66a2-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e66a2-119">Header files</span></span>

<span data-ttu-id="e66a2-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e66a2-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="e66a2-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e66a2-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="e66a2-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e66a2-122">Mapitags.h</span></span>
  
> <span data-ttu-id="e66a2-123">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e66a2-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e66a2-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e66a2-124">See also</span></span>



[<span data-ttu-id="e66a2-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e66a2-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e66a2-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e66a2-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e66a2-127">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e66a2-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e66a2-128">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e66a2-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

