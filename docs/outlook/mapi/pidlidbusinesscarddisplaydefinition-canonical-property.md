---
title: Propiedad canónica PidLidBusinessCardDisplayDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f25f8a538ff61bc7e04c234efd7404b1c866d64d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342038"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a><span data-ttu-id="74c86-103">Propiedad canónica PidLidBusinessCardDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="74c86-103">PidLidBusinessCardDisplayDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="74c86-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74c86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74c86-105">Contiene los detalles de personalización del usuario para mostrar un contacto como una tarjeta de presentación.</span><span class="sxs-lookup"><span data-stu-id="74c86-105">Contains user-customization details for displaying a contact as a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74c86-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="74c86-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74c86-107">dispidBCDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="74c86-107">dispidBCDisplayDefinition</span></span>  <br/> |
|<span data-ttu-id="74c86-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="74c86-108">Property set:</span></span>  <br/> |<span data-ttu-id="74c86-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="74c86-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="74c86-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="74c86-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="74c86-111">0x00008040</span><span class="sxs-lookup"><span data-stu-id="74c86-111">0x00008040</span></span>  <br/> |
|<span data-ttu-id="74c86-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="74c86-112">Data type:</span></span>  <br/> |<span data-ttu-id="74c86-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="74c86-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="74c86-114">Área:</span><span class="sxs-lookup"><span data-stu-id="74c86-114">Area:</span></span>  <br/> |<span data-ttu-id="74c86-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="74c86-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74c86-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74c86-116">Remarks</span></span>

<span data-ttu-id="74c86-117">El diseño de una tarjeta de presentación se puede representar como una imagen y varios campos de texto.</span><span class="sxs-lookup"><span data-stu-id="74c86-117">The layout of a business card can be represented as an image and a number of text fields.</span></span> <span data-ttu-id="74c86-118">La imagen puede ser una foto de contacto o una imagen de tarjeta.</span><span class="sxs-lookup"><span data-stu-id="74c86-118">The image can be either a contact photo, or a card picture.</span></span> <span data-ttu-id="74c86-119">Los campos de texto constan de un valor de otra propiedad establecida en el contacto y una cadena de etiqueta personalizada opcional proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="74c86-119">Text fields consist of a value from another property set on the contact and an optional customized label string provided by the user.</span></span> <span data-ttu-id="74c86-120">Ten en cuenta que los valores de varios bytes se almacenan en formato little-endian en el búfer.</span><span class="sxs-lookup"><span data-stu-id="74c86-120">Note that multi-byte values are stored in little-endian format in the buffer.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="74c86-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="74c86-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74c86-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="74c86-122">Protocol specifications</span></span>

<span data-ttu-id="74c86-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74c86-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74c86-124">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="74c86-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="74c86-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74c86-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74c86-126">Especifica las propiedades y operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="74c86-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74c86-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="74c86-127">Header files</span></span>

<span data-ttu-id="74c86-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74c86-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="74c86-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="74c86-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74c86-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="74c86-130">See also</span></span>



[<span data-ttu-id="74c86-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="74c86-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74c86-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="74c86-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74c86-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="74c86-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74c86-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="74c86-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

