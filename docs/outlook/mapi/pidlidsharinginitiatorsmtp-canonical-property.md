---
title: Propiedad canónica PidLidSharingInitiatorSmtp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorSmtp
api_type:
- COM
ms.assetid: 4fb7d91d-4c51-41c1-9cb6-7b837dd12f11
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eb699b2312064f8ed330238962dd86992c046139
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337124"
---
# <a name="pidlidsharinginitiatorsmtp-canonical-property"></a><span data-ttu-id="54f2b-103">Propiedad canónica PidLidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="54f2b-103">PidLidSharingInitiatorSmtp Canonical Property</span></span>

  
  
<span data-ttu-id="54f2b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54f2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54f2b-105">Especifica la dirección SMTP del usuario que inició el mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="54f2b-105">Specifies the SMTP address of the user who initiated the sharing message.</span></span> <span data-ttu-id="54f2b-106">Esta es una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="54f2b-106">This is a property of a sharing message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54f2b-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="54f2b-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="54f2b-108">dispidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="54f2b-108">dispidSharingInitiatorSmtp</span></span>  <br/> |
|<span data-ttu-id="54f2b-109">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="54f2b-109">Property set:</span></span>  <br/> |<span data-ttu-id="54f2b-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="54f2b-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="54f2b-111">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="54f2b-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="54f2b-112">0x00008A08</span><span class="sxs-lookup"><span data-stu-id="54f2b-112">0x00008A08</span></span>  <br/> |
|<span data-ttu-id="54f2b-113">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="54f2b-113">Data type:</span></span>  <br/> |<span data-ttu-id="54f2b-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="54f2b-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="54f2b-115">Área:</span><span class="sxs-lookup"><span data-stu-id="54f2b-115">Area:</span></span>  <br/> |<span data-ttu-id="54f2b-116">Compartir</span><span class="sxs-lookup"><span data-stu-id="54f2b-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54f2b-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54f2b-117">Remarks</span></span>

<span data-ttu-id="54f2b-118">Esta propiedad debe establecerse en el valor de la propiedad **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) de la libreta de direcciones identificada por la propiedad **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) y debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="54f2b-118">This property must be set to the value of the **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) property from the Address Book identified by the **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="54f2b-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="54f2b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="54f2b-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="54f2b-120">Protocol specifications</span></span>

<span data-ttu-id="54f2b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54f2b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54f2b-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="54f2b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="54f2b-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54f2b-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54f2b-124">Comparte carpetas de buzones entre clientes.</span><span class="sxs-lookup"><span data-stu-id="54f2b-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="54f2b-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="54f2b-125">Header files</span></span>

<span data-ttu-id="54f2b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54f2b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="54f2b-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="54f2b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54f2b-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="54f2b-128">See also</span></span>



[<span data-ttu-id="54f2b-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="54f2b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54f2b-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="54f2b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54f2b-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="54f2b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54f2b-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="54f2b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

