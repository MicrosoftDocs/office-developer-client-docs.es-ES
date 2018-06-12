---
title: Propiedad canónico PidLidAnniversaryEventEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAnniversaryEventEntryId
api_type:
- COM
ms.assetid: 177b2b87-7a06-4d53-8f03-5bec5632c2dd
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 78096affce8fa03cc3efc8f0ca0c7048c2f9aae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818478"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a><span data-ttu-id="68a96-103">Propiedad canónico PidLidAnniversaryEventEntryId</span><span class="sxs-lookup"><span data-stu-id="68a96-103">PidLidAnniversaryEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="68a96-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68a96-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68a96-105">Especifica el identificador de entrada de la cita que representa el aniversario del contacto.</span><span class="sxs-lookup"><span data-stu-id="68a96-105">Specifies the entry identifier of the appointment that represents the contact's anniversary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68a96-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="68a96-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="68a96-107">dispidAnniversaryEventEID</span><span class="sxs-lookup"><span data-stu-id="68a96-107">dispidAnniversaryEventEID</span></span>  <br/> |
|<span data-ttu-id="68a96-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="68a96-108">Property set:</span></span>  <br/> |<span data-ttu-id="68a96-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="68a96-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="68a96-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="68a96-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="68a96-111">0x0000804E</span><span class="sxs-lookup"><span data-stu-id="68a96-111">0x0000804E</span></span>  <br/> |
|<span data-ttu-id="68a96-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="68a96-112">Data type:</span></span>  <br/> |<span data-ttu-id="68a96-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="68a96-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="68a96-114">Área:</span><span class="sxs-lookup"><span data-stu-id="68a96-114">Area:</span></span>  <br/> |<span data-ttu-id="68a96-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="68a96-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68a96-116">Notas</span><span class="sxs-lookup"><span data-stu-id="68a96-116">Remarks</span></span>

<span data-ttu-id="68a96-117">La cita especificada por la propiedad **dispidAnniversaryEventEID** debe estar vinculada a este contacto mediante el uso de la **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([ PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) y las propiedades de **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)), como detalla en [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="68a96-117">The appointment specified by the **dispidAnniversaryEventEID** property must be linked to this contact by using the **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as detailed in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="68a96-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="68a96-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="68a96-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="68a96-119">Protocol specifications</span></span>

<span data-ttu-id="68a96-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68a96-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68a96-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="68a96-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="68a96-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68a96-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68a96-123">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="68a96-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="68a96-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="68a96-124">Header files</span></span>

<span data-ttu-id="68a96-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="68a96-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="68a96-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="68a96-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68a96-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="68a96-127">See also</span></span>



[<span data-ttu-id="68a96-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="68a96-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68a96-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="68a96-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68a96-130">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="68a96-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68a96-131">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="68a96-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

