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
ms.openlocfilehash: 188424fc67534ea5df6ed5eb209909731e12c73c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818917"
---
# <a name="pidlidsharinginitiatorsmtp-canonical-property"></a><span data-ttu-id="2c8b9-103">Propiedad canónica PidLidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="2c8b9-103">PidLidSharingInitiatorSmtp Canonical Property</span></span>

  
  
<span data-ttu-id="2c8b9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c8b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c8b9-105">Especifica la dirección SMTP del usuario que inició el mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="2c8b9-105">Specifies the SMTP address of the user who initiated the sharing message.</span></span> <span data-ttu-id="2c8b9-106">Esto es una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="2c8b9-106">This is a property of a sharing message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c8b9-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2c8b9-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c8b9-108">dispidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="2c8b9-108">dispidSharingInitiatorSmtp</span></span>  <br/> |
|<span data-ttu-id="2c8b9-109">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="2c8b9-109">Property set:</span></span>  <br/> |<span data-ttu-id="2c8b9-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="2c8b9-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="2c8b9-111">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="2c8b9-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2c8b9-112">0x00008A08</span><span class="sxs-lookup"><span data-stu-id="2c8b9-112">0x00008A08</span></span>  <br/> |
|<span data-ttu-id="2c8b9-113">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2c8b9-113">Data type:</span></span>  <br/> |<span data-ttu-id="2c8b9-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2c8b9-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2c8b9-115">Área:</span><span class="sxs-lookup"><span data-stu-id="2c8b9-115">Area:</span></span>  <br/> |<span data-ttu-id="2c8b9-116">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="2c8b9-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c8b9-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c8b9-117">Remarks</span></span>

<span data-ttu-id="2c8b9-118">Esta propiedad debe estar establecida en el valor de la propiedad **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) de la libreta de direcciones identificado por la propiedad **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) y debe ser pasa por alto.</span><span class="sxs-lookup"><span data-stu-id="2c8b9-118">This property must be set to the value of the **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) property from the Address Book identified by the **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2c8b9-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c8b9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c8b9-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2c8b9-120">Protocol specifications</span></span>

<span data-ttu-id="2c8b9-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c8b9-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c8b9-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2c8b9-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2c8b9-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c8b9-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c8b9-124">Comparte las carpetas de buzón de correo entre los clientes.</span><span class="sxs-lookup"><span data-stu-id="2c8b9-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c8b9-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2c8b9-125">Header files</span></span>

<span data-ttu-id="2c8b9-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c8b9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c8b9-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2c8b9-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c8b9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c8b9-128">See also</span></span>



[<span data-ttu-id="2c8b9-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2c8b9-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c8b9-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2c8b9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c8b9-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2c8b9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c8b9-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="2c8b9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

