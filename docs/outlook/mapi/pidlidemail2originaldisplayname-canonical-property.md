---
title: Propiedad canónica PidLidEmail2OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7fb7e5afa6a1c050a5d91274bc4f82439fb98640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337964"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a><span data-ttu-id="5c4b7-103">Propiedad canónica PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="5c4b7-103">PidLidEmail2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="5c4b7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c4b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c4b7-105">Especifica el segundo nombre para mostrar que corresponde a la dirección de correo electrónico especificada para el contacto.</span><span class="sxs-lookup"><span data-stu-id="5c4b7-105">Specifies the second display name that corresponds to the email address specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c4b7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5c4b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c4b7-107">dispidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="5c4b7-107">dispidEmail2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="5c4b7-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="5c4b7-108">Property set:</span></span>  <br/> |<span data-ttu-id="5c4b7-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="5c4b7-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="5c4b7-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5c4b7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5c4b7-111">0x00008094</span><span class="sxs-lookup"><span data-stu-id="5c4b7-111">0x00008094</span></span>  <br/> |
|<span data-ttu-id="5c4b7-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5c4b7-112">Data type:</span></span>  <br/> |<span data-ttu-id="5c4b7-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5c4b7-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5c4b7-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5c4b7-114">Area:</span></span>  <br/> |<span data-ttu-id="5c4b7-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="5c4b7-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c4b7-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5c4b7-116">Remarks</span></span>

<span data-ttu-id="5c4b7-117">Si el valor de la propiedad **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) es "SMTP", el valor de la propiedad **PidLidEmail2OriginalDisplayName** correspondiente debe ser igual al valor de la propiedad **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) respectiva.</span><span class="sxs-lookup"><span data-stu-id="5c4b7-117">If the value of the **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) property is "SMTP", the value of the respective **PidLidEmail2OriginalDisplayName** property should equal the value of the respective **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="5c4b7-118">El propósito de esta propiedad es mostrar una dirección alternativa fácil de usar que es equivalente a la de **dispidEmail2EmailAddress**.</span><span class="sxs-lookup"><span data-stu-id="5c4b7-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail2EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5c4b7-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c4b7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5c4b7-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="5c4b7-120">Protocol specifications</span></span>

<span data-ttu-id="5c4b7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c4b7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c4b7-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="5c4b7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5c4b7-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c4b7-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c4b7-124">Especifica las propiedades y operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="5c4b7-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5c4b7-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5c4b7-125">Header files</span></span>

<span data-ttu-id="5c4b7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c4b7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c4b7-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5c4b7-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c4b7-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5c4b7-128">See also</span></span>



[<span data-ttu-id="5c4b7-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5c4b7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c4b7-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="5c4b7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c4b7-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5c4b7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c4b7-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5c4b7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

