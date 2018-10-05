---
title: Propiedad canónica PidLidContactLinkSearchKey
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ea815631f63b5585a3f2705cfbd2639b8c655e6e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387499"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a><span data-ttu-id="164bd-103">Propiedad canónica PidLidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="164bd-103">PidLidContactLinkSearchKey Canonical Property</span></span>

<span data-ttu-id="164bd-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="164bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="164bd-105">Contiene la lista de **SearchKeys** para el contacto vinculado a este objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="164bd-105">Contains the list of **SearchKeys** for the contact linked to by this message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="164bd-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="164bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="164bd-107">dispidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="164bd-107">dispidContactLinkSearchKey</span></span>  <br/> |
|<span data-ttu-id="164bd-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="164bd-108">Property set:</span></span>  <br/> |<span data-ttu-id="164bd-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="164bd-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="164bd-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="164bd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="164bd-111">0x00008584</span><span class="sxs-lookup"><span data-stu-id="164bd-111">0x00008584</span></span>  <br/> |
|<span data-ttu-id="164bd-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="164bd-112">Data type:</span></span>  <br/> |<span data-ttu-id="164bd-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="164bd-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="164bd-114">Área:</span><span class="sxs-lookup"><span data-stu-id="164bd-114">Area:</span></span>  <br/> |<span data-ttu-id="164bd-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="164bd-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="164bd-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="164bd-116">Remarks</span></span>

|<span data-ttu-id="164bd-117">**Longitud en bytes**</span><span class="sxs-lookup"><span data-stu-id="164bd-117">**Length in bytes**</span></span>|<span data-ttu-id="164bd-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="164bd-118">**Description**</span></span>|<span data-ttu-id="164bd-119">**Notas**</span><span class="sxs-lookup"><span data-stu-id="164bd-119">**Notes**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="164bd-120">2</span><span class="sxs-lookup"><span data-stu-id="164bd-120">2</span></span>  <br/> |<span data-ttu-id="164bd-121">ContactEntryCount</span><span class="sxs-lookup"><span data-stu-id="164bd-121">ContactEntryCount</span></span>  <br/> |<span data-ttu-id="164bd-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="164bd-122">None</span></span>  <br/> |
|<span data-ttu-id="164bd-123">variable</span><span class="sxs-lookup"><span data-stu-id="164bd-123">variable</span></span>  <br/> |<span data-ttu-id="164bd-124">Datos de SearchKey</span><span class="sxs-lookup"><span data-stu-id="164bd-124">SearchKey data</span></span>  <br/> |<span data-ttu-id="164bd-125">Repite ContactEntryCount veces</span><span class="sxs-lookup"><span data-stu-id="164bd-125">Repeats ContactEntryCount times</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="164bd-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="164bd-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="164bd-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="164bd-127">Protocol specifications</span></span>

<span data-ttu-id="164bd-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="164bd-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="164bd-129">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="164bd-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="164bd-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="164bd-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="164bd-131">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="164bd-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="164bd-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="164bd-132">Header files</span></span>

<span data-ttu-id="164bd-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="164bd-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="164bd-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="164bd-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="164bd-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="164bd-135">See also</span></span>

- [<span data-ttu-id="164bd-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="164bd-136">MAPI Properties</span></span>](mapi-properties.md) 
- [<span data-ttu-id="164bd-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="164bd-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="164bd-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="164bd-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="164bd-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="164bd-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

