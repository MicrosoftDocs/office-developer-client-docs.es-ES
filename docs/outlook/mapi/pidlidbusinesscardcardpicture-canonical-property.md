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
ms.openlocfilehash: fd1ad923acca5a75d06e6b15ae7ae7411edefb92
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342010"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a><span data-ttu-id="6dfd1-103">Propiedad canónica PidLidBusinessCardCardPicture</span><span class="sxs-lookup"><span data-stu-id="6dfd1-103">PidLidBusinessCardCardPicture Canonical Property</span></span>

  
  
<span data-ttu-id="6dfd1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dfd1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dfd1-105">Contiene la imagen que se usará en una tarjeta de presentación.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-105">Contains the image to use on a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6dfd1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6dfd1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6dfd1-107">dispidBCCardPicture</span><span class="sxs-lookup"><span data-stu-id="6dfd1-107">dispidBCCardPicture</span></span>  <br/> |
|<span data-ttu-id="6dfd1-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="6dfd1-108">Property set:</span></span>  <br/> |<span data-ttu-id="6dfd1-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="6dfd1-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="6dfd1-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="6dfd1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6dfd1-111">0x00008041</span><span class="sxs-lookup"><span data-stu-id="6dfd1-111">0x00008041</span></span>  <br/> |
|<span data-ttu-id="6dfd1-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6dfd1-112">Data type:</span></span>  <br/> |<span data-ttu-id="6dfd1-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6dfd1-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6dfd1-114">Área:</span><span class="sxs-lookup"><span data-stu-id="6dfd1-114">Area:</span></span>  <br/> |<span data-ttu-id="6dfd1-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="6dfd1-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6dfd1-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6dfd1-116">Remarks</span></span>

<span data-ttu-id="6dfd1-117">El valor de esta propiedad debe ser una secuencia de gráficos de red portátil (PNG) o JPEG.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-117">The value of this property must be either a portable network graphics (PNG) or JPEG stream.</span></span> <span data-ttu-id="6dfd1-118">Esta propiedad debe usarse junto con la propiedad **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) de la siguiente manera: **dispidBCCardPicture** no debe estar presente en un contacto si **dispidBCDisplayDefinition** no está presente.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-118">This property should be used in conjunction with the **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) property as follows: **dispidBCCardPicture** should not be present on a contact if **dispidBCDisplayDefinition** is not present.</span></span> <span data-ttu-id="6dfd1-119">Esta propiedad tampoco debe estar presente si los datos de **dispidBCCardPicture** no requieren una imagen de tarjeta.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-119">This property also should not be present if the data in **dispidBCCardPicture** does not require a card image.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6dfd1-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6dfd1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6dfd1-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="6dfd1-121">Protocol specifications</span></span>

<span data-ttu-id="6dfd1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6dfd1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6dfd1-123">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6dfd1-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6dfd1-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6dfd1-125">Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6dfd1-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6dfd1-126">Header files</span></span>

<span data-ttu-id="6dfd1-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6dfd1-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6dfd1-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6dfd1-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6dfd1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6dfd1-129">See also</span></span>



[<span data-ttu-id="6dfd1-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6dfd1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6dfd1-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="6dfd1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6dfd1-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6dfd1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6dfd1-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="6dfd1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

