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
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335073"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="de9e4-103">Propiedad canónica PidLidDistributionListMembers</span><span class="sxs-lookup"><span data-stu-id="de9e4-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="de9e4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de9e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de9e4-105">Especifica la lista de EntryIds de los objetos que corresponden a los miembros de la lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="de9e4-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de9e4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="de9e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de9e4-107">dispidDLMembers</span><span class="sxs-lookup"><span data-stu-id="de9e4-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="de9e4-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="de9e4-108">Property set:</span></span>  <br/> |<span data-ttu-id="de9e4-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="de9e4-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="de9e4-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="de9e4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="de9e4-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="de9e4-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="de9e4-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="de9e4-112">Data type:</span></span>  <br/> |<span data-ttu-id="de9e4-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="de9e4-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="de9e4-114">Área:</span><span class="sxs-lookup"><span data-stu-id="de9e4-114">Area:</span></span>  <br/> |<span data-ttu-id="de9e4-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="de9e4-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de9e4-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de9e4-116">Remarks</span></span>

<span data-ttu-id="de9e4-117">Los miembros de la lista de distribución personal pueden ser otras listas de distribución personales, direcciones electrónicas contenidas en un contacto, usuarios de la lista global de direcciones o listas de distribución, o direcciones de correo electrónico de uso único.</span><span class="sxs-lookup"><span data-stu-id="de9e4-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="de9e4-118">El formato de cada EntryId debe ser un EntryId de uso único, como se especifica en [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) o un EntryId ajustado.</span><span class="sxs-lookup"><span data-stu-id="de9e4-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="de9e4-119">Al establecer esta propiedad, el cliente o el servidor debe asegurarse de que su tamaño total sea inferior a 15.000 bytes.</span><span class="sxs-lookup"><span data-stu-id="de9e4-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="de9e4-120">Esta propiedad especifica la lista de EntryIds de uso único que corresponden a los miembros de la lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="de9e4-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="de9e4-121">Estos EntryIds únicos encapsulan los nombres para mostrar y las direcciones de correo electrónico de los miembros de la lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="de9e4-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="de9e4-122">Si el cliente o el servidor establecen esta propiedad, debe sincronizarse con esta propiedad **dispidDLMembers** para cada entrada de la propiedad **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), debe haber una entrada en la misma posición en **dispidDLOneOffMembers**.</span><span class="sxs-lookup"><span data-stu-id="de9e4-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="de9e4-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="de9e4-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de9e4-124">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="de9e4-124">Protocol specifications</span></span>

<span data-ttu-id="de9e4-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de9e4-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de9e4-126">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="de9e4-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="de9e4-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de9e4-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de9e4-128">Especifica las propiedades y operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="de9e4-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de9e4-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="de9e4-129">Header files</span></span>

<span data-ttu-id="de9e4-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de9e4-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="de9e4-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="de9e4-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de9e4-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="de9e4-132">See also</span></span>



[<span data-ttu-id="de9e4-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="de9e4-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de9e4-134">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="de9e4-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de9e4-135">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="de9e4-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de9e4-136">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="de9e4-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

