---
title: Propiedad canónico PidLidSharingInitiatorEntryId
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6881f5ed54baffd37ff25d26f455b82bf2526d41
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818919"
---
# <a name="pidlidsharinginitiatorentryid-canonical-property"></a><span data-ttu-id="99ec4-103">Propiedad canónico PidLidSharingInitiatorEntryId</span><span class="sxs-lookup"><span data-stu-id="99ec4-103">PidLidSharingInitiatorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="99ec4-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99ec4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99ec4-105">Designa como una propiedad de un mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="99ec4-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="99ec4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="99ec4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="99ec4-107">dispidSharingInitiatorEid</span><span class="sxs-lookup"><span data-stu-id="99ec4-107">dispidSharingInitiatorEid</span></span>  <br/> |
|<span data-ttu-id="99ec4-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="99ec4-108">Property set:</span></span>  <br/> |<span data-ttu-id="99ec4-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="99ec4-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="99ec4-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="99ec4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="99ec4-111">0x00008A09</span><span class="sxs-lookup"><span data-stu-id="99ec4-111">0x00008A09</span></span>  <br/> |
|<span data-ttu-id="99ec4-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="99ec4-112">Data type:</span></span>  <br/> |<span data-ttu-id="99ec4-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="99ec4-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="99ec4-114">Área:</span><span class="sxs-lookup"><span data-stu-id="99ec4-114">Area:</span></span>  <br/> |<span data-ttu-id="99ec4-115">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="99ec4-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99ec4-116">Notas</span><span class="sxs-lookup"><span data-stu-id="99ec4-116">Remarks</span></span>

<span data-ttu-id="99ec4-117">Esta propiedad se debe establecer en el valor de la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para la libreta de direcciones del usuario que ha iniciado la sesión actual (vea [[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)).</span><span class="sxs-lookup"><span data-stu-id="99ec4-117">This property must be set to the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property for the Address Book of the currently logged-on user (see [[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="99ec4-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="99ec4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="99ec4-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="99ec4-119">Protocol specifications</span></span>

<span data-ttu-id="99ec4-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99ec4-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99ec4-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="99ec4-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="99ec4-122">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99ec4-122">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99ec4-123">Comparte las carpetas de buzón de correo entre los clientes.</span><span class="sxs-lookup"><span data-stu-id="99ec4-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="99ec4-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="99ec4-124">Header files</span></span>

<span data-ttu-id="99ec4-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99ec4-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="99ec4-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="99ec4-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99ec4-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="99ec4-127">See also</span></span>



[<span data-ttu-id="99ec4-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="99ec4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="99ec4-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="99ec4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="99ec4-130">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="99ec4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="99ec4-131">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="99ec4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

