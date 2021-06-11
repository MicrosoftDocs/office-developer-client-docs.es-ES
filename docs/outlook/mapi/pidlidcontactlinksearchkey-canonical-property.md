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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319778"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a><span data-ttu-id="743e5-103">Propiedad canónica PidLidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="743e5-103">PidLidContactLinkSearchKey Canonical Property</span></span>

<span data-ttu-id="743e5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="743e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="743e5-105">Contiene la lista de **SearchKeys** para el contacto al que está vinculado este objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="743e5-105">Contains the list of **SearchKeys** for the contact linked to by this message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="743e5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="743e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="743e5-107">dispidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="743e5-107">dispidContactLinkSearchKey</span></span>  <br/> |
|<span data-ttu-id="743e5-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="743e5-108">Property set:</span></span>  <br/> |<span data-ttu-id="743e5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="743e5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="743e5-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="743e5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="743e5-111">0x00008584</span><span class="sxs-lookup"><span data-stu-id="743e5-111">0x00008584</span></span>  <br/> |
|<span data-ttu-id="743e5-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="743e5-112">Data type:</span></span>  <br/> |<span data-ttu-id="743e5-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="743e5-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="743e5-114">Área:</span><span class="sxs-lookup"><span data-stu-id="743e5-114">Area:</span></span>  <br/> |<span data-ttu-id="743e5-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="743e5-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="743e5-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="743e5-116">Remarks</span></span>

|<span data-ttu-id="743e5-117">**Longitud en bytes**</span><span class="sxs-lookup"><span data-stu-id="743e5-117">**Length in bytes**</span></span>|<span data-ttu-id="743e5-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="743e5-118">**Description**</span></span>|<span data-ttu-id="743e5-119">**Notas**</span><span class="sxs-lookup"><span data-stu-id="743e5-119">**Notes**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="743e5-120">2</span><span class="sxs-lookup"><span data-stu-id="743e5-120">2</span></span>  <br/> |<span data-ttu-id="743e5-121">ContactEntryCount</span><span class="sxs-lookup"><span data-stu-id="743e5-121">ContactEntryCount</span></span>  <br/> |<span data-ttu-id="743e5-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="743e5-122">None</span></span>  <br/> |
|<span data-ttu-id="743e5-123">variable</span><span class="sxs-lookup"><span data-stu-id="743e5-123">variable</span></span>  <br/> |<span data-ttu-id="743e5-124">Datos de SearchKey</span><span class="sxs-lookup"><span data-stu-id="743e5-124">SearchKey data</span></span>  <br/> |<span data-ttu-id="743e5-125">Repite contactEntryCount veces</span><span class="sxs-lookup"><span data-stu-id="743e5-125">Repeats ContactEntryCount times</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="743e5-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="743e5-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="743e5-127">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="743e5-127">Protocol specifications</span></span>

<span data-ttu-id="743e5-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="743e5-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="743e5-129">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="743e5-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="743e5-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="743e5-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="743e5-131">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="743e5-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="743e5-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="743e5-132">Header files</span></span>

<span data-ttu-id="743e5-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="743e5-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="743e5-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="743e5-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="743e5-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="743e5-135">See also</span></span>

- [<span data-ttu-id="743e5-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="743e5-136">MAPI Properties</span></span>](mapi-properties.md) 
- [<span data-ttu-id="743e5-137">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="743e5-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="743e5-138">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="743e5-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="743e5-139">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="743e5-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

