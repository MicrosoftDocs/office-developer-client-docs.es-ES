---
title: Propiedad canónica PidLidBusinessCardCardPicture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardCardPicture
api_type:
- COM
ms.assetid: 2c7af147-f7eb-41ef-8403-93584a2041ba
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1b83316b599ea9ee62bde78cbd734dfb6b2d8b80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588499"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a><span data-ttu-id="7ba46-103">Propiedad canónica PidLidBusinessCardCardPicture</span><span class="sxs-lookup"><span data-stu-id="7ba46-103">PidLidBusinessCardCardPicture Canonical Property</span></span>

  
  
<span data-ttu-id="7ba46-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ba46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ba46-105">Contiene la imagen que se va a usar en una tarjeta de presentación.</span><span class="sxs-lookup"><span data-stu-id="7ba46-105">Contains the image to use on a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7ba46-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7ba46-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7ba46-107">dispidBCCardPicture</span><span class="sxs-lookup"><span data-stu-id="7ba46-107">dispidBCCardPicture</span></span>  <br/> |
|<span data-ttu-id="7ba46-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="7ba46-108">Property set:</span></span>  <br/> |<span data-ttu-id="7ba46-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="7ba46-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="7ba46-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="7ba46-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7ba46-111">0x00008041</span><span class="sxs-lookup"><span data-stu-id="7ba46-111">0x00008041</span></span>  <br/> |
|<span data-ttu-id="7ba46-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7ba46-112">Data type:</span></span>  <br/> |<span data-ttu-id="7ba46-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7ba46-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7ba46-114">Área:</span><span class="sxs-lookup"><span data-stu-id="7ba46-114">Area:</span></span>  <br/> |<span data-ttu-id="7ba46-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="7ba46-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ba46-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ba46-116">Remarks</span></span>

<span data-ttu-id="7ba46-117">El valor de esta propiedad debe ser un gráficos de red portátiles (PNG) o una secuencia JPEG.</span><span class="sxs-lookup"><span data-stu-id="7ba46-117">The value of this property must be either a portable network graphics (PNG) or JPEG stream.</span></span> <span data-ttu-id="7ba46-118">Esta propiedad debe usarse junto con la propiedad **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) como se indica a continuación: **dispidBCCardPicture** no debe estar presente en un contacto if ** dispidBCDisplayDefinition** no está presente.</span><span class="sxs-lookup"><span data-stu-id="7ba46-118">This property should be used in conjunction with the **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) property as follows: **dispidBCCardPicture** should not be present on a contact if **dispidBCDisplayDefinition** is not present.</span></span> <span data-ttu-id="7ba46-119">Esta propiedad también debería no estar presente si los datos de **dispidBCCardPicture** no requieren una imagen de la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="7ba46-119">This property also should not be present if the data in **dispidBCCardPicture** does not require a card image.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7ba46-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ba46-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7ba46-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7ba46-121">Protocol specifications</span></span>

<span data-ttu-id="7ba46-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ba46-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7ba46-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7ba46-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7ba46-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ba46-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7ba46-125">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="7ba46-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7ba46-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7ba46-126">Header files</span></span>

<span data-ttu-id="7ba46-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7ba46-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="7ba46-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7ba46-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7ba46-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="7ba46-129">See also</span></span>



[<span data-ttu-id="7ba46-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7ba46-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7ba46-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7ba46-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7ba46-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7ba46-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7ba46-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="7ba46-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

