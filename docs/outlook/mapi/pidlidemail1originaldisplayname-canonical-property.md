---
title: Propiedad canónica PidLidEmail1OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail1OriginalDisplayName
api_type:
- COM
ms.assetid: 991c2969-0180-4c7d-95ee-e62fd24d67ef
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a20ae8e3f19073bfb88d58db516a0e5f93d91445
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335045"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a><span data-ttu-id="96fda-103">Propiedad canónica PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="96fda-103">PidLidEmail1OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="96fda-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96fda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96fda-105">Especifica el primer nombre para mostrar que corresponde a la dirección de correo electrónico especificada para el contacto.</span><span class="sxs-lookup"><span data-stu-id="96fda-105">Specifies the first display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96fda-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="96fda-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96fda-107">dispidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="96fda-107">dispidEmail1OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="96fda-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="96fda-108">Property set:</span></span>  <br/> |<span data-ttu-id="96fda-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="96fda-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="96fda-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="96fda-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="96fda-111">0x00008084</span><span class="sxs-lookup"><span data-stu-id="96fda-111">0x00008084</span></span>  <br/> |
|<span data-ttu-id="96fda-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="96fda-112">Data type:</span></span>  <br/> |<span data-ttu-id="96fda-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="96fda-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="96fda-114">Área:</span><span class="sxs-lookup"><span data-stu-id="96fda-114">Area:</span></span>  <br/> |<span data-ttu-id="96fda-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="96fda-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96fda-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96fda-116">Remarks</span></span>

<span data-ttu-id="96fda-117">Si el valor de la propiedad **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) es "SMTP", el valor de la propiedad **dispidEmail1OriginalDisplayName** correspondiente debe ser igual al valor de la propiedad **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) respectiva.</span><span class="sxs-lookup"><span data-stu-id="96fda-117">If the value of the **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail1OriginalDisplayName** property should equal the value of the respective **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="96fda-118">Esta propiedad muestra una dirección alternativa fácil de usar que equivale a la de la **propiedad dispidEmail1EmailAddress.**</span><span class="sxs-lookup"><span data-stu-id="96fda-118">This property displays an alternative user-friendly address that is equivalent to the one in the **dispidEmail1EmailAddress** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="96fda-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="96fda-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="96fda-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="96fda-120">Protocol specifications</span></span>

<span data-ttu-id="96fda-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96fda-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96fda-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="96fda-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="96fda-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96fda-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96fda-124">Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="96fda-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="96fda-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="96fda-125">Header files</span></span>

<span data-ttu-id="96fda-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96fda-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="96fda-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="96fda-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96fda-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="96fda-128">See also</span></span>



[<span data-ttu-id="96fda-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="96fda-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96fda-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="96fda-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96fda-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="96fda-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96fda-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="96fda-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

