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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315025"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="99035-103">Propiedad canónica PidNameRightsManagementLicense</span><span class="sxs-lookup"><span data-stu-id="99035-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="99035-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99035-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99035-105">Almacena en caché la licencia de uso del mensaje de correo electrónico administrado por derechos.</span><span class="sxs-lookup"><span data-stu-id="99035-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="99035-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="99035-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="99035-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="99035-107">None</span></span>  <br/> |
|<span data-ttu-id="99035-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="99035-108">Property set:</span></span>  <br/> |<span data-ttu-id="99035-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="99035-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="99035-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="99035-110">Property name:</span></span>  <br/> |<span data-ttu-id="99035-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="99035-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="99035-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="99035-112">Data type:</span></span>  <br/> |<span data-ttu-id="99035-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="99035-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="99035-114">Área:</span><span class="sxs-lookup"><span data-stu-id="99035-114">Area:</span></span>  <br/> |<span data-ttu-id="99035-115">Mensajería segura</span><span class="sxs-lookup"><span data-stu-id="99035-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99035-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99035-116">Remarks</span></span>

<span data-ttu-id="99035-117">Si la propiedad está presente en un mensaje de correo electrónico administrado con derechos, el primer valor de esta propiedad binaria múltiple debe contener la licencia de uso comprimido ZLIB (como se especifica en [RFC1950]) para el mensaje de correo electrónico administrado por derechos.</span><span class="sxs-lookup"><span data-stu-id="99035-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="99035-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="99035-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="99035-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="99035-119">Protocol specifications</span></span>

<span data-ttu-id="99035-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99035-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99035-121">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="99035-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="99035-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99035-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99035-123">Especifica las propiedades de los mensajes codificados con derechos administrados.</span><span class="sxs-lookup"><span data-stu-id="99035-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="99035-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="99035-124">Header files</span></span>

<span data-ttu-id="99035-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99035-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="99035-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="99035-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99035-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="99035-127">See also</span></span>



[<span data-ttu-id="99035-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="99035-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="99035-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="99035-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="99035-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="99035-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="99035-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="99035-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

