---
title: Propiedad canónica PidLidRemoteTransport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b0f86b2260299d2d0294598628f2895c50ed9452
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818901"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="bc2c6-103">Propiedad canónica PidLidRemoteTransport</span><span class="sxs-lookup"><span data-stu-id="bc2c6-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="bc2c6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc2c6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc2c6-105">Identifica el elemento de encabezado de qué cuenta está asociado, principalmente para implementar la deje de POP en la funcionalidad del servidor.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc2c6-106">Propiedades asociadas</span><span class="sxs-lookup"><span data-stu-id="bc2c6-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="bc2c6-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="bc2c6-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="bc2c6-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="bc2c6-108">Property set:</span></span>  <br/> |<span data-ttu-id="bc2c6-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="bc2c6-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="bc2c6-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="bc2c6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bc2c6-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="bc2c6-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="bc2c6-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="bc2c6-112">Data type:</span></span>  <br/> |<span data-ttu-id="bc2c6-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="bc2c6-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="bc2c6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="bc2c6-114">Area:</span></span>  <br/> |<span data-ttu-id="bc2c6-115">Mensaje remoto</span><span class="sxs-lookup"><span data-stu-id="bc2c6-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc2c6-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc2c6-116">Remarks</span></span>

<span data-ttu-id="bc2c6-117">Esta propiedad sólo es relevante en los mensajes que tienen una clase de mensaje IPM. Remoto.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="bc2c6-118">Microsoft Outlook mantiene una asignación de varias cuentas que va a descargar en un almacén determinado en un mensaje de información de asociados de carpeta (FAI), pero también puede mantener esta información en el registro.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bc2c6-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc2c6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bc2c6-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="bc2c6-120">Protocol specifications</span></span>

<span data-ttu-id="bc2c6-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="bc2c6-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="bc2c6-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc2c6-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="bc2c6-123">Header files</span></span>

<span data-ttu-id="bc2c6-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc2c6-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc2c6-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bc2c6-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc2c6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc2c6-126">See also</span></span>



[<span data-ttu-id="bc2c6-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bc2c6-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc2c6-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="bc2c6-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc2c6-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="bc2c6-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc2c6-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="bc2c6-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

