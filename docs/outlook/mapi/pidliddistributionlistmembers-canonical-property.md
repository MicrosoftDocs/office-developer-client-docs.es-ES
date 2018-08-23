---
title: Propiedad canónica PidLidDistributionListMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9bfb94b2929f780a428fb932efb3538f94f5aaea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591467"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="74898-103">Propiedad canónica PidLidDistributionListMembers</span><span class="sxs-lookup"><span data-stu-id="74898-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="74898-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74898-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74898-105">Especifica la lista de identificadores de los objetos que corresponden a los miembros de la lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="74898-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74898-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="74898-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74898-107">dispidDLMembers</span><span class="sxs-lookup"><span data-stu-id="74898-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="74898-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="74898-108">Property set:</span></span>  <br/> |<span data-ttu-id="74898-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="74898-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="74898-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="74898-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="74898-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="74898-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="74898-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="74898-112">Data type:</span></span>  <br/> |<span data-ttu-id="74898-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="74898-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="74898-114">Área:</span><span class="sxs-lookup"><span data-stu-id="74898-114">Area:</span></span>  <br/> |<span data-ttu-id="74898-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="74898-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74898-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74898-116">Remarks</span></span>

<span data-ttu-id="74898-117">Los miembros de la lista de distribución personal pueden ser otras listas de distribución personales, las direcciones electrónicas contenidas en un contacto, los usuarios de la lista Global de direcciones o listas de distribución o direcciones de correo electrónico de uso único.</span><span class="sxs-lookup"><span data-stu-id="74898-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="74898-118">El formato de cada propiedad EntryId debe ser un EntryId de uso único, tal como se especifica en [[MS-OXCDATA],](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) o un valor de EntryId ajustado.</span><span class="sxs-lookup"><span data-stu-id="74898-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="74898-119">Al establecer esta propiedad, el cliente o el servidor debe asegurarse de que su tamaño total es inferior a 15.000 bytes.</span><span class="sxs-lookup"><span data-stu-id="74898-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="74898-120">Esta propiedad especifica la lista de identificadores de uso único que corresponden a los miembros de la lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="74898-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="74898-121">Estos identificadores de uso único encapsulan para mostrar los nombres y direcciones de correo electrónico de los miembros de la lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="74898-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="74898-122">Si el cliente o el servidor de establece esta propiedad, se debe sincronizar con esta propiedad **dispidDLMembers** para cada entrada en la propiedad **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), debe haber una entrada en el misma posición en el **dispidDLOneOffMembers**.</span><span class="sxs-lookup"><span data-stu-id="74898-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="74898-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="74898-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74898-124">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="74898-124">Protocol specifications</span></span>

<span data-ttu-id="74898-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74898-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74898-126">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="74898-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="74898-127">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74898-127">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74898-128">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="74898-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74898-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="74898-129">Header files</span></span>

<span data-ttu-id="74898-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74898-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="74898-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="74898-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74898-132">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="74898-132">See also</span></span>



[<span data-ttu-id="74898-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="74898-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74898-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="74898-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74898-135">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="74898-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74898-136">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="74898-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

