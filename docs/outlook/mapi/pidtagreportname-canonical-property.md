---
title: Propiedad canónico PidTagReportName
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 4d3a38f55fa2869df3f8afa1301cf1ad0c7b0737
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820100"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="4216a-103">Propiedad canónico PidTagReportName</span><span class="sxs-lookup"><span data-stu-id="4216a-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="4216a-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4216a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4216a-105">Contiene el nombre para mostrar para el destinatario que debería obtener informes para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="4216a-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4216a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4216a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4216a-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="4216a-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="4216a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4216a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4216a-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="4216a-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="4216a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4216a-110">Data type:</span></span>  <br/> |<span data-ttu-id="4216a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4216a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4216a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4216a-112">Area:</span></span>  <br/> |<span data-ttu-id="4216a-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="4216a-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4216a-114">Notas</span><span class="sxs-lookup"><span data-stu-id="4216a-114">Remarks</span></span>

<span data-ttu-id="4216a-115">Estas propiedades son ejemplos de las propiedades de dirección para el destinatario que el remitente ha delegado para recibir los informes generados para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="4216a-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="4216a-116">Una aplicación cliente que se debe enrutar informes a otro usuario debe establecer estas propiedades en tiempo de envío de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4216a-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="4216a-117">Si no se establecen, los informes se envían al remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4216a-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4216a-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4216a-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4216a-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4216a-119">Header files</span></span>

<span data-ttu-id="4216a-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4216a-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="4216a-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4216a-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="4216a-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4216a-122">Mapitags.h</span></span>
  
> <span data-ttu-id="4216a-123">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4216a-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4216a-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="4216a-124">See also</span></span>



[<span data-ttu-id="4216a-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4216a-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4216a-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4216a-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4216a-127">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="4216a-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4216a-128">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4216a-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

