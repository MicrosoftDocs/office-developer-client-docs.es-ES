---
title: Propiedad canónica PidLidContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContacts
api_type:
- COM
ms.assetid: 709e701f-b24e-4cd5-8c55-3f9e67f67a4a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 10dd12522a635098908285f1a9ee16c93d96f728
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319463"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="34ffb-103">Propiedad canónica PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="34ffb-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="34ffb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34ffb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34ffb-105">Contiene los nombres de los contactos asociados con el elemento.</span><span class="sxs-lookup"><span data-stu-id="34ffb-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="34ffb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="34ffb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="34ffb-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="34ffb-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="34ffb-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="34ffb-108">Property set:</span></span>  <br/> |<span data-ttu-id="34ffb-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="34ffb-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="34ffb-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="34ffb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="34ffb-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="34ffb-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="34ffb-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="34ffb-112">Data type:</span></span>  <br/> |<span data-ttu-id="34ffb-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="34ffb-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="34ffb-114">Área:</span><span class="sxs-lookup"><span data-stu-id="34ffb-114">Area:</span></span>  <br/> |<span data-ttu-id="34ffb-115">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="34ffb-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34ffb-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="34ffb-116">Remarks</span></span>

<span data-ttu-id="34ffb-117">Esta propiedad contiene la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de cada **EntryID** de la libreta de direcciones a la que se hace referencia en el valor de la propiedad **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="34ffb-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="34ffb-118">Puede incluir nombres a los que no se hace referencia en **dispidContactLinkEntry**.</span><span class="sxs-lookup"><span data-stu-id="34ffb-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="34ffb-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="34ffb-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="34ffb-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="34ffb-120">Protocol specifications</span></span>

<span data-ttu-id="34ffb-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34ffb-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34ffb-122">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="34ffb-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="34ffb-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34ffb-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34ffb-124">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="34ffb-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="34ffb-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34ffb-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34ffb-126">Especifica las propiedades y operaciones que se admiten para los diarios.</span><span class="sxs-lookup"><span data-stu-id="34ffb-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="34ffb-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34ffb-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34ffb-128">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="34ffb-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="34ffb-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="34ffb-129">Header files</span></span>

<span data-ttu-id="34ffb-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="34ffb-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="34ffb-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="34ffb-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34ffb-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="34ffb-132">See also</span></span>



[<span data-ttu-id="34ffb-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="34ffb-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="34ffb-134">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="34ffb-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="34ffb-135">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="34ffb-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="34ffb-136">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="34ffb-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

