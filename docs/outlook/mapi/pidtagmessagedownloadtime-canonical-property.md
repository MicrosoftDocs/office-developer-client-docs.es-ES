---
title: Propiedad canónica PidTagMessageDownloadTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325679"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="8328e-103">Propiedad canónica PidTagMessageDownloadTime</span><span class="sxs-lookup"><span data-stu-id="8328e-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="8328e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8328e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8328e-105">Contiene el tiempo estimado para descargar un mensaje desde un servidor remoto a un almacén de mensajes local.</span><span class="sxs-lookup"><span data-stu-id="8328e-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8328e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8328e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8328e-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="8328e-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="8328e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8328e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8328e-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="8328e-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="8328e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8328e-110">Data type:</span></span>  <br/> |<span data-ttu-id="8328e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8328e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8328e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8328e-112">Area:</span></span>  <br/> |<span data-ttu-id="8328e-113">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="8328e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8328e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8328e-114">Remarks</span></span>

<span data-ttu-id="8328e-115">Esta propiedad se expresa en segundos y representa la mejor estimación del tiempo que tardaría un proveedor de transporte remoto en descargar un mensaje determinado desde su ubicación actual a un almacén de mensajes local hasta que el cliente vea la carpeta de encabezado.</span><span class="sxs-lookup"><span data-stu-id="8328e-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="8328e-116">El proveedor de transporte remoto normalmente calcula el valor de esta propiedad dividiendo el valor de la propiedad **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) por la velocidad del vínculo de comunicaciones en bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="8328e-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="8328e-117">Si el proveedor no puede calcular el tiempo de descarga, por ejemplo, si no conoce la velocidad del vínculo, debe proporcionar un valor **PT_ERROR** como **MAPI_E_NO_SUPPORT** para esta columna en la tabla contenido de la carpeta de encabezado.</span><span class="sxs-lookup"><span data-stu-id="8328e-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8328e-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8328e-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8328e-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8328e-119">Header files</span></span>

<span data-ttu-id="8328e-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8328e-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="8328e-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8328e-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="8328e-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8328e-122">Mapitags.h</span></span>
  
> <span data-ttu-id="8328e-123">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8328e-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8328e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8328e-124">See also</span></span>



[<span data-ttu-id="8328e-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8328e-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8328e-126">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="8328e-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8328e-127">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8328e-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8328e-128">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8328e-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

