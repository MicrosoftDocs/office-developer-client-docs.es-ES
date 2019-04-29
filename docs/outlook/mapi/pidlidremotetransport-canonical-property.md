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
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439446"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="52097-103">Propiedad canónica PidLidRemoteTransport</span><span class="sxs-lookup"><span data-stu-id="52097-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="52097-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52097-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52097-105">Identifica la cuenta con la que está asociado el elemento de encabezado, principalmente para implementar la funcionalidad de salida de POP en el servidor.</span><span class="sxs-lookup"><span data-stu-id="52097-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52097-106">Propiedades asociadas</span><span class="sxs-lookup"><span data-stu-id="52097-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="52097-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="52097-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="52097-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="52097-108">Property set:</span></span>  <br/> |<span data-ttu-id="52097-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="52097-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="52097-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="52097-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="52097-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="52097-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="52097-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="52097-112">Data type:</span></span>  <br/> |<span data-ttu-id="52097-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="52097-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="52097-114">Área:</span><span class="sxs-lookup"><span data-stu-id="52097-114">Area:</span></span>  <br/> |<span data-ttu-id="52097-115">Mensaje remoto</span><span class="sxs-lookup"><span data-stu-id="52097-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52097-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52097-116">Remarks</span></span>

<span data-ttu-id="52097-117">Esta propiedad sólo es relevante en los mensajes que tienen una clase de mensaje IPM. Modo.</span><span class="sxs-lookup"><span data-stu-id="52097-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="52097-118">Microsoft Outlook mantiene una asignación de varias cuentas que se descargan a un almacén determinado en un mensaje de información asociada a una carpeta (FAI), pero también puede conservar esta información en el registro.</span><span class="sxs-lookup"><span data-stu-id="52097-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="52097-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="52097-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="52097-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="52097-120">Protocol specifications</span></span>

<span data-ttu-id="52097-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="52097-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="52097-122">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="52097-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="52097-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="52097-123">Header files</span></span>

<span data-ttu-id="52097-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="52097-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="52097-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="52097-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52097-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="52097-126">See also</span></span>



[<span data-ttu-id="52097-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="52097-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52097-128">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="52097-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52097-129">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="52097-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52097-130">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="52097-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

