---
title: Propiedad canónico PidLidContacts
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6182c9dfc0c4de24bd587e626fe74d02ed23968b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818610"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="bd9bc-103">Propiedad canónico PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="bd9bc-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="bd9bc-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd9bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd9bc-105">Contiene los nombres de los contactos asociados con el elemento.</span><span class="sxs-lookup"><span data-stu-id="bd9bc-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd9bc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="bd9bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd9bc-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="bd9bc-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="bd9bc-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="bd9bc-108">Property set:</span></span>  <br/> |<span data-ttu-id="bd9bc-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="bd9bc-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="bd9bc-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="bd9bc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bd9bc-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="bd9bc-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="bd9bc-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="bd9bc-112">Data type:</span></span>  <br/> |<span data-ttu-id="bd9bc-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bd9bc-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bd9bc-114">Área:</span><span class="sxs-lookup"><span data-stu-id="bd9bc-114">Area:</span></span>  <br/> |<span data-ttu-id="bd9bc-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="bd9bc-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd9bc-116">Notas</span><span class="sxs-lookup"><span data-stu-id="bd9bc-116">Remarks</span></span>

<span data-ttu-id="bd9bc-117">Esta propiedad contiene la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de cada **propiedad EntryID** de la libreta de direcciones que se hace referencia en el valor de propiedad de **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bd9bc-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="bd9bc-118">Puede incluir los nombres que no se hace referencia en **dispidContactLinkEntry**.</span><span class="sxs-lookup"><span data-stu-id="bd9bc-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bd9bc-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd9bc-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd9bc-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="bd9bc-120">Protocol specifications</span></span>

<span data-ttu-id="bd9bc-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd9bc-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd9bc-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="bd9bc-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bd9bc-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd9bc-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd9bc-124">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd9bc-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="bd9bc-125">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd9bc-125">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd9bc-126">Especifica las propiedades y operaciones que se permiten para diarios.</span><span class="sxs-lookup"><span data-stu-id="bd9bc-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="bd9bc-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd9bc-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd9bc-128">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="bd9bc-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bd9bc-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="bd9bc-129">Header files</span></span>

<span data-ttu-id="bd9bc-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd9bc-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd9bc-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bd9bc-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd9bc-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="bd9bc-132">See also</span></span>



[<span data-ttu-id="bd9bc-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bd9bc-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd9bc-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="bd9bc-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd9bc-135">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="bd9bc-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd9bc-136">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="bd9bc-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

