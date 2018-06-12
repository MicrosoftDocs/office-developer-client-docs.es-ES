---
title: Propiedad canónico PidLidRemoteTransport
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: b0f86b2260299d2d0294598628f2895c50ed9452
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818901"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="38bab-103">Propiedad canónico PidLidRemoteTransport</span><span class="sxs-lookup"><span data-stu-id="38bab-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="38bab-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38bab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38bab-105">Identifica el elemento de encabezado de qué cuenta está asociado, principalmente para implementar la deje de POP en la funcionalidad del servidor.</span><span class="sxs-lookup"><span data-stu-id="38bab-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38bab-106">Propiedades asociadas</span><span class="sxs-lookup"><span data-stu-id="38bab-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="38bab-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="38bab-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="38bab-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="38bab-108">Property set:</span></span>  <br/> |<span data-ttu-id="38bab-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="38bab-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="38bab-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="38bab-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="38bab-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="38bab-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="38bab-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="38bab-112">Data type:</span></span>  <br/> |<span data-ttu-id="38bab-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="38bab-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="38bab-114">Área:</span><span class="sxs-lookup"><span data-stu-id="38bab-114">Area:</span></span>  <br/> |<span data-ttu-id="38bab-115">Mensaje remoto</span><span class="sxs-lookup"><span data-stu-id="38bab-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38bab-116">Notas</span><span class="sxs-lookup"><span data-stu-id="38bab-116">Remarks</span></span>

<span data-ttu-id="38bab-117">Esta propiedad sólo es relevante en los mensajes que tienen una clase de mensaje IPM. Remoto.</span><span class="sxs-lookup"><span data-stu-id="38bab-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="38bab-118">Microsoft Outlook mantiene una asignación de varias cuentas que va a descargar en un almacén determinado en un mensaje de información de asociados de carpeta (FAI), pero también puede mantener esta información en el registro.</span><span class="sxs-lookup"><span data-stu-id="38bab-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="38bab-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="38bab-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38bab-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="38bab-120">Protocol specifications</span></span>

<span data-ttu-id="38bab-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="38bab-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="38bab-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="38bab-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38bab-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="38bab-123">Header files</span></span>

<span data-ttu-id="38bab-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38bab-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="38bab-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="38bab-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38bab-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="38bab-126">See also</span></span>



[<span data-ttu-id="38bab-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="38bab-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38bab-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="38bab-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38bab-129">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="38bab-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38bab-130">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="38bab-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

