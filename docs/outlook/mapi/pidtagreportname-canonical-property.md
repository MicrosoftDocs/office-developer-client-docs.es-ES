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
ms.openlocfilehash: 33a7545f9b2719615617d46e2d5ed1f6952b5522
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422316"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="f4a23-103">Propiedad canónica PidTagReportName</span><span class="sxs-lookup"><span data-stu-id="f4a23-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="f4a23-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4a23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4a23-105">Contiene el nombre para mostrar del destinatario que debe obtener informes para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4a23-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4a23-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f4a23-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4a23-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="f4a23-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="f4a23-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f4a23-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4a23-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="f4a23-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="f4a23-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f4a23-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4a23-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f4a23-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f4a23-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f4a23-112">Area:</span></span>  <br/> |<span data-ttu-id="f4a23-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="f4a23-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4a23-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4a23-114">Remarks</span></span>

<span data-ttu-id="f4a23-115">Estas propiedades son ejemplos de las propiedades de dirección del destinatario que el remitente ha delegado para recibir los informes generados para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4a23-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="f4a23-116">Una aplicación cliente que deba enrutar informes a otro usuario debe establecer estas propiedades en la hora de envío del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4a23-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="f4a23-117">Si no se establecen, los informes se envían al remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4a23-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f4a23-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4a23-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f4a23-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f4a23-119">Header files</span></span>

<span data-ttu-id="f4a23-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f4a23-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4a23-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f4a23-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4a23-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f4a23-122">Mapitags.h</span></span>
  
> <span data-ttu-id="f4a23-123">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f4a23-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4a23-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="f4a23-124">See also</span></span>



[<span data-ttu-id="f4a23-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f4a23-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4a23-126">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f4a23-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4a23-127">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f4a23-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4a23-128">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f4a23-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

