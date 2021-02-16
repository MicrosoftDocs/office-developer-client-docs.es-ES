---
title: Propiedad canónica PidLidBirthdayEventEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBirthdayEventEntryId
api_type:
- COM
ms.assetid: 6807dcfc-d9bd-48a1-a093-3097b2cb107c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 90d1dc8a9ce7f94238e8754cfbcaf88b702928f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342024"
---
# <a name="pidlidbirthdayevententryid-canonical-property"></a><span data-ttu-id="b09cd-103">Propiedad canónica PidLidBirthdayEventEntryId</span><span class="sxs-lookup"><span data-stu-id="b09cd-103">PidLidBirthdayEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="b09cd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b09cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b09cd-105">Especifica el **EntryId de** una cita opcional que representa el cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="b09cd-105">Specifies the **EntryId** of an optional appointment that represents the contact's birthday.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b09cd-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b09cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b09cd-107">dispidBirthdayEventEID</span><span class="sxs-lookup"><span data-stu-id="b09cd-107">dispidBirthdayEventEID</span></span>  <br/> |
|<span data-ttu-id="b09cd-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="b09cd-108">Property set:</span></span>  <br/> |<span data-ttu-id="b09cd-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="b09cd-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="b09cd-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b09cd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b09cd-111">0x0000804D</span><span class="sxs-lookup"><span data-stu-id="b09cd-111">0x0000804D</span></span>  <br/> |
|<span data-ttu-id="b09cd-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b09cd-112">Data type:</span></span>  <br/> |<span data-ttu-id="b09cd-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b09cd-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b09cd-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b09cd-114">Area:</span></span>  <br/> |<span data-ttu-id="b09cd-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="b09cd-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b09cd-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b09cd-116">Remarks</span></span>

<span data-ttu-id="b09cd-117">La cita especificada por esta propiedad debe vincularse a este contacto mediante las propiedades **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) y **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)), tal como se especifica en [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b09cd-117">The appointment this is specified by this property must be linked to this contact by using the **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b09cd-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b09cd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b09cd-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="b09cd-119">Protocol specifications</span></span>

<span data-ttu-id="b09cd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b09cd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b09cd-121">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="b09cd-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b09cd-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b09cd-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b09cd-123">Especifica las propiedades y operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="b09cd-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b09cd-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b09cd-124">Header files</span></span>

<span data-ttu-id="b09cd-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b09cd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b09cd-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b09cd-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b09cd-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b09cd-127">See also</span></span>



[<span data-ttu-id="b09cd-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b09cd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b09cd-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="b09cd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b09cd-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b09cd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b09cd-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="b09cd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

