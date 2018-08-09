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
ms.openlocfilehash: 4a8cf9ac24f275d8b9cdbe03b5a90477771a2ab4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818585"
---
# <a name="pidlidbirthdayevententryid-canonical-property"></a><span data-ttu-id="b4420-103">Propiedad canónica PidLidBirthdayEventEntryId</span><span class="sxs-lookup"><span data-stu-id="b4420-103">PidLidBirthdayEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="b4420-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4420-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4420-105">Especifica la **propiedad EntryId** de una cita opcional que representa el cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="b4420-105">Specifies the **EntryId** of an optional appointment that represents the contact's birthday.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4420-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b4420-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4420-107">dispidBirthdayEventEID</span><span class="sxs-lookup"><span data-stu-id="b4420-107">dispidBirthdayEventEID</span></span>  <br/> |
|<span data-ttu-id="b4420-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="b4420-108">Property set:</span></span>  <br/> |<span data-ttu-id="b4420-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="b4420-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="b4420-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="b4420-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b4420-111">0x0000804D</span><span class="sxs-lookup"><span data-stu-id="b4420-111">0x0000804D</span></span>  <br/> |
|<span data-ttu-id="b4420-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b4420-112">Data type:</span></span>  <br/> |<span data-ttu-id="b4420-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b4420-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b4420-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b4420-114">Area:</span></span>  <br/> |<span data-ttu-id="b4420-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="b4420-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4420-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b4420-116">Remarks</span></span>

<span data-ttu-id="b4420-117">La cita se especifica por esta propiedad debe estar vinculada a este contacto mediante el uso de la **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) y ** dispidContactLinkName** propiedades ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)), como especifica en [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b4420-117">The appointment this is specified by this property must be linked to this contact by using the **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as specified in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b4420-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4420-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4420-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b4420-119">Protocol specifications</span></span>

<span data-ttu-id="b4420-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4420-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4420-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b4420-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b4420-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4420-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4420-123">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="b4420-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4420-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b4420-124">Header files</span></span>

<span data-ttu-id="b4420-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4420-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4420-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b4420-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4420-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4420-127">See also</span></span>



[<span data-ttu-id="b4420-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b4420-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4420-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b4420-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4420-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b4420-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4420-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b4420-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

