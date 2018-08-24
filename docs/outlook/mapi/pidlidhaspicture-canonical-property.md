---
title: Propiedad canónica PidLidHasPicture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidHasPicture
api_type:
- COM
ms.assetid: c3bea11c-3197-4060-8672-f1b4bf352112
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 30046bd7982d08d99c5581c27d1616162d904dee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577110"
---
# <a name="pidlidhaspicture-canonical-property"></a><span data-ttu-id="3cca6-103">Propiedad canónica PidLidHasPicture</span><span class="sxs-lookup"><span data-stu-id="3cca6-103">PidLidHasPicture Canonical Property</span></span>

  
  
<span data-ttu-id="3cca6-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cca6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cca6-105">Especifica si existe un dato adjunto de foto de un contacto.</span><span class="sxs-lookup"><span data-stu-id="3cca6-105">Specifies whether a photo attachment exists for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3cca6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3cca6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3cca6-107">dispidHasPicture</span><span class="sxs-lookup"><span data-stu-id="3cca6-107">dispidHasPicture</span></span>  <br/> |
|<span data-ttu-id="3cca6-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="3cca6-108">Property set:</span></span>  <br/> |<span data-ttu-id="3cca6-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="3cca6-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="3cca6-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="3cca6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3cca6-111">0x00008015</span><span class="sxs-lookup"><span data-stu-id="3cca6-111">0x00008015</span></span>  <br/> |
|<span data-ttu-id="3cca6-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3cca6-112">Data type:</span></span>  <br/> |<span data-ttu-id="3cca6-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3cca6-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3cca6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3cca6-114">Area:</span></span>  <br/> |<span data-ttu-id="3cca6-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="3cca6-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cca6-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3cca6-116">Remarks</span></span>

<span data-ttu-id="3cca6-117">Si esta propiedad existe y se establece en TRUE, tabla de datos adjuntos del contacto contiene datos adjuntos con la propiedad de **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) establecida en TRUE.</span><span class="sxs-lookup"><span data-stu-id="3cca6-117">If this property exists and is set to TRUE, the contact's attachment table contains an attachment with the **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) property set to TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3cca6-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3cca6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3cca6-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3cca6-119">Protocol specifications</span></span>

<span data-ttu-id="3cca6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cca6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cca6-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3cca6-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3cca6-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cca6-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cca6-123">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="3cca6-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3cca6-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3cca6-124">Header files</span></span>

<span data-ttu-id="3cca6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3cca6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="3cca6-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3cca6-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3cca6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3cca6-127">See also</span></span>



[<span data-ttu-id="3cca6-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3cca6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3cca6-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="3cca6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3cca6-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3cca6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3cca6-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="3cca6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

