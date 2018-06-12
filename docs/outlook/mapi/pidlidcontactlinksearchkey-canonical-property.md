---
title: Propiedad canónico PidLidContactLinkSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactLinkSearchKey
api_type:
- COM
ms.assetid: 82d21d38-a6c6-4e12-85b1-8158b2f5cce7
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 65a54475afe526cce40030cbfd1cdb9e86126554
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818606"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a><span data-ttu-id="fc4b6-103">Propiedad canónico PidLidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="fc4b6-103">PidLidContactLinkSearchKey Canonical Property</span></span>

<span data-ttu-id="fc4b6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc4b6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc4b6-105">Contiene la lista de **SearchKeys** para el contacto vinculado a este objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="fc4b6-105">Contains the list of **SearchKeys** for the contact linked to by this message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc4b6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fc4b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc4b6-107">dispidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="fc4b6-107">dispidContactLinkSearchKey</span></span>  <br/> |
|<span data-ttu-id="fc4b6-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="fc4b6-108">Property set:</span></span>  <br/> |<span data-ttu-id="fc4b6-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fc4b6-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fc4b6-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="fc4b6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fc4b6-111">0x00008584</span><span class="sxs-lookup"><span data-stu-id="fc4b6-111">0x00008584</span></span>  <br/> |
|<span data-ttu-id="fc4b6-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fc4b6-112">Data type:</span></span>  <br/> |<span data-ttu-id="fc4b6-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fc4b6-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fc4b6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fc4b6-114">Area:</span></span>  <br/> |<span data-ttu-id="fc4b6-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="fc4b6-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc4b6-116">Notas</span><span class="sxs-lookup"><span data-stu-id="fc4b6-116">Remarks</span></span>

|<span data-ttu-id="fc4b6-117">**Longitud en bytes**</span><span class="sxs-lookup"><span data-stu-id="fc4b6-117">**Length in bytes**</span></span>|<span data-ttu-id="fc4b6-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc4b6-118">**Description**</span></span>|<span data-ttu-id="fc4b6-119">**Notas**</span><span class="sxs-lookup"><span data-stu-id="fc4b6-119">**Notes**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fc4b6-120">2</span><span class="sxs-lookup"><span data-stu-id="fc4b6-120">2</span></span>  <br/> |<span data-ttu-id="fc4b6-121">ContactEntryCount</span><span class="sxs-lookup"><span data-stu-id="fc4b6-121">ContactEntryCount</span></span>  <br/> |<span data-ttu-id="fc4b6-122">None</span><span class="sxs-lookup"><span data-stu-id="fc4b6-122">None</span></span>  <br/> |
|<span data-ttu-id="fc4b6-123">variable</span><span class="sxs-lookup"><span data-stu-id="fc4b6-123">variable</span></span>  <br/> |<span data-ttu-id="fc4b6-124">Datos de SearchKey</span><span class="sxs-lookup"><span data-stu-id="fc4b6-124">SearchKey data</span></span>  <br/> |<span data-ttu-id="fc4b6-125">Repite ContactEntryCount veces</span><span class="sxs-lookup"><span data-stu-id="fc4b6-125">Repeats ContactEntryCount times</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="fc4b6-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc4b6-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc4b6-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fc4b6-127">Protocol specifications</span></span>

<span data-ttu-id="fc4b6-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc4b6-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc4b6-129">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fc4b6-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fc4b6-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc4b6-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc4b6-131">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="fc4b6-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc4b6-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fc4b6-132">Header files</span></span>

<span data-ttu-id="fc4b6-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc4b6-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc4b6-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fc4b6-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc4b6-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="fc4b6-135">See also</span></span>

- [<span data-ttu-id="fc4b6-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fc4b6-136">MAPI Properties</span></span>](mapi-properties.md) 
- [<span data-ttu-id="fc4b6-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fc4b6-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="fc4b6-138">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="fc4b6-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="fc4b6-139">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fc4b6-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

