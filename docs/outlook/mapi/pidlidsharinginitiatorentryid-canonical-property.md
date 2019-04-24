---
title: Propiedad canónica PidLidSharingInitiatorEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorEntryId
api_type:
- COM
ms.assetid: 47f00706-83df-49cb-bda7-ef572d76a020
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bfe682fc3263278c6e1d02a29a8b6432f41ac79e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309530"
---
# <a name="pidlidsharinginitiatorentryid-canonical-property"></a><span data-ttu-id="3faf0-103">Propiedad canónica PidLidSharingInitiatorEntryId</span><span class="sxs-lookup"><span data-stu-id="3faf0-103">PidLidSharingInitiatorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="3faf0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3faf0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3faf0-105">Designa como una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="3faf0-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3faf0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3faf0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3faf0-107">dispidSharingInitiatorEid</span><span class="sxs-lookup"><span data-stu-id="3faf0-107">dispidSharingInitiatorEid</span></span>  <br/> |
|<span data-ttu-id="3faf0-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="3faf0-108">Property set:</span></span>  <br/> |<span data-ttu-id="3faf0-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="3faf0-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="3faf0-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="3faf0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3faf0-111">0x00008A09</span><span class="sxs-lookup"><span data-stu-id="3faf0-111">0x00008A09</span></span>  <br/> |
|<span data-ttu-id="3faf0-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3faf0-112">Data type:</span></span>  <br/> |<span data-ttu-id="3faf0-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3faf0-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3faf0-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3faf0-114">Area:</span></span>  <br/> |<span data-ttu-id="3faf0-115">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="3faf0-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3faf0-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3faf0-116">Remarks</span></span>

<span data-ttu-id="3faf0-117">Esta propiedad debe establecerse en el valor de la \*\*\*\* propiedad OXOABK ([PidTagEntryId](pidtagentryid-canonical-property.md)) para la libreta de direcciones del usuario que ha iniciado la sesión actual (vea [[ms-]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)).</span><span class="sxs-lookup"><span data-stu-id="3faf0-117">This property must be set to the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property for the Address Book of the currently logged-on user (see [[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3faf0-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3faf0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3faf0-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3faf0-119">Protocol specifications</span></span>

<span data-ttu-id="3faf0-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3faf0-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3faf0-121">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3faf0-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3faf0-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3faf0-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3faf0-123">Comparte carpetas de buzones entre clientes.</span><span class="sxs-lookup"><span data-stu-id="3faf0-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3faf0-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3faf0-124">Header files</span></span>

<span data-ttu-id="3faf0-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3faf0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="3faf0-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3faf0-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3faf0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3faf0-127">See also</span></span>



[<span data-ttu-id="3faf0-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3faf0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3faf0-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="3faf0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3faf0-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3faf0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3faf0-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="3faf0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

