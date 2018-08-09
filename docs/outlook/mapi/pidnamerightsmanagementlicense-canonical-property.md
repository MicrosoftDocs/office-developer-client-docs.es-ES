---
title: Propiedad canónica PidNameRightsManagementLicense
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c75cb480b9a1a7ffdcff9c0f9b49aabba746fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819126"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="5f887-103">Propiedad canónica PidNameRightsManagementLicense</span><span class="sxs-lookup"><span data-stu-id="5f887-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="5f887-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f887-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f887-105">Almacena en caché la licencia de uso para el mensaje de correo electrónico con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="5f887-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f887-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="5f887-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="5f887-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5f887-107">None</span></span>  <br/> |
|<span data-ttu-id="5f887-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="5f887-108">Property set:</span></span>  <br/> |<span data-ttu-id="5f887-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="5f887-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="5f887-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="5f887-110">Property name:</span></span>  <br/> |<span data-ttu-id="5f887-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="5f887-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="5f887-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5f887-112">Data type:</span></span>  <br/> |<span data-ttu-id="5f887-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="5f887-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="5f887-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5f887-114">Area:</span></span>  <br/> |<span data-ttu-id="5f887-115">Mensajería segura</span><span class="sxs-lookup"><span data-stu-id="5f887-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f887-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f887-116">Remarks</span></span>

<span data-ttu-id="5f887-117">Si la propiedad está presente en un mensaje de correo electrónico con derechos administrados, el primer valor de esta propiedad binario varios debe contener la licencia de uso comprimido ZLIB (tal y como se especifica en [RFC1950]) para el mensaje de correo electrónico con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="5f887-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f887-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f887-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f887-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5f887-119">Protocol specifications</span></span>

<span data-ttu-id="5f887-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f887-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f887-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5f887-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f887-122">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f887-122">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f887-123">Especifica las propiedades de mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="5f887-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f887-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5f887-124">Header files</span></span>

<span data-ttu-id="5f887-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f887-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f887-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5f887-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f887-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f887-127">See also</span></span>



[<span data-ttu-id="5f887-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5f887-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f887-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5f887-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f887-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5f887-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f887-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5f887-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

