---
title: Propiedad canónica PidTagTemplateid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTemplateid
api_type:
- COM
ms.assetid: 1a418c76-ebc7-47f2-ac91-797162e6e099
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 96bcd15606771bd112568ad94133507ab14b2bcd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396396"
---
# <a name="pidtagtemplateid-canonical-property"></a><span data-ttu-id="7321c-103">Propiedad canónica PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="7321c-103">PidTagTemplateid Canonical Property</span></span>

  
  
<span data-ttu-id="7321c-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7321c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7321c-105">Contiene la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expresado como un formato de identificador de entrada permanente.</span><span class="sxs-lookup"><span data-stu-id="7321c-105">Contains the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expressed as a permanent entry ID format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7321c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7321c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7321c-107">PR_TEMPLATEID</span><span class="sxs-lookup"><span data-stu-id="7321c-107">PR_TEMPLATEID</span></span>  <br/> |
|<span data-ttu-id="7321c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7321c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7321c-109">0x3902</span><span class="sxs-lookup"><span data-stu-id="7321c-109">0x3902</span></span>  <br/> |
|<span data-ttu-id="7321c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7321c-110">Data type:</span></span>  <br/> |<span data-ttu-id="7321c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7321c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7321c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7321c-112">Area:</span></span>  <br/> |<span data-ttu-id="7321c-113">Libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="7321c-113">MAPI Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7321c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7321c-114">Remarks</span></span>

<span data-ttu-id="7321c-115">Este valor debe estar presente para todos los objetos de la libreta de direcciones en un servidor de la interfaz de proveedor de servicio de nombres (NSPI), su nombre distintivo (DN) debe coincidir con el valor de **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) y su DN debe seguir el formato DN especificación particular para el tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="7321c-115">This value must be present for all address book objects on an Name Service Provider Interface (NSPI) server, its distinguished name (DN) must match the value for **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and its DN must follow the DN format specification particular to the type of object.</span></span> 
  
<span data-ttu-id="7321c-116">Esta propiedad no está presente en los objetos de una libreta de direcciones sin conexión.</span><span class="sxs-lookup"><span data-stu-id="7321c-116">This property is not present on objects in an offline address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7321c-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7321c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7321c-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7321c-118">Protocol specifications</span></span>

<span data-ttu-id="7321c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7321c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7321c-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7321c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7321c-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7321c-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7321c-122">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="7321c-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7321c-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7321c-123">Header files</span></span>

<span data-ttu-id="7321c-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7321c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="7321c-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7321c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="7321c-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7321c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="7321c-127">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="7321c-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7321c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7321c-128">See also</span></span>



[<span data-ttu-id="7321c-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7321c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7321c-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7321c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7321c-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7321c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7321c-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="7321c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

