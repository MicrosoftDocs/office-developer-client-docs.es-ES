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
ms.openlocfilehash: 889b823a55c39ebc19e52c8cc9a1d078a5732a01
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395549"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="a6e37-103">Propiedad canónica PidNameRightsManagementLicense</span><span class="sxs-lookup"><span data-stu-id="a6e37-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="a6e37-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6e37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6e37-105">Almacena en caché la licencia de uso para el mensaje de correo electrónico con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="a6e37-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a6e37-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="a6e37-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="a6e37-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a6e37-107">None</span></span>  <br/> |
|<span data-ttu-id="a6e37-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="a6e37-108">Property set:</span></span>  <br/> |<span data-ttu-id="a6e37-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="a6e37-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="a6e37-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="a6e37-110">Property name:</span></span>  <br/> |<span data-ttu-id="a6e37-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="a6e37-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="a6e37-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a6e37-112">Data type:</span></span>  <br/> |<span data-ttu-id="a6e37-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="a6e37-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="a6e37-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a6e37-114">Area:</span></span>  <br/> |<span data-ttu-id="a6e37-115">Mensajería segura</span><span class="sxs-lookup"><span data-stu-id="a6e37-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6e37-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a6e37-116">Remarks</span></span>

<span data-ttu-id="a6e37-117">Si la propiedad está presente en un mensaje de correo electrónico con derechos administrados, el primer valor de esta propiedad binario varios debe contener la licencia de uso comprimido ZLIB (tal y como se especifica en [RFC1950]) para el mensaje de correo electrónico con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="a6e37-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a6e37-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6e37-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a6e37-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a6e37-119">Protocol specifications</span></span>

<span data-ttu-id="a6e37-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6e37-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6e37-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a6e37-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a6e37-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6e37-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6e37-123">Especifica las propiedades de mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="a6e37-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a6e37-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a6e37-124">Header files</span></span>

<span data-ttu-id="a6e37-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a6e37-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a6e37-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a6e37-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6e37-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6e37-127">See also</span></span>



[<span data-ttu-id="a6e37-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a6e37-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a6e37-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a6e37-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a6e37-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a6e37-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a6e37-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a6e37-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

