---
title: Propiedad canónica PidLidOtherAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOtherAddress
api_type:
- COM
ms.assetid: 2b8acb69-4c84-4075-8457-d7aadce26c73
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0b05e83e48bf144ca317a64f90fb533f6d7d1c24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359076"
---
# <a name="pidlidotheraddress-canonical-property"></a><span data-ttu-id="854aa-103">Propiedad canónica PidLidOtherAddress</span><span class="sxs-lookup"><span data-stu-id="854aa-103">PidLidOtherAddress Canonical Property</span></span>

  
  
<span data-ttu-id="854aa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="854aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="854aa-105">Especifica la dirección completa de la otra dirección del contacto.</span><span class="sxs-lookup"><span data-stu-id="854aa-105">Specifies the complete address of the contact's other address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="854aa-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="854aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="854aa-107">dispidOtherAddress</span><span class="sxs-lookup"><span data-stu-id="854aa-107">dispidOtherAddress</span></span>  <br/> |
|<span data-ttu-id="854aa-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="854aa-108">Property set:</span></span>  <br/> |<span data-ttu-id="854aa-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="854aa-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="854aa-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="854aa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="854aa-111">0x0000801C</span><span class="sxs-lookup"><span data-stu-id="854aa-111">0x0000801C</span></span>  <br/> |
|<span data-ttu-id="854aa-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="854aa-112">Data type:</span></span>  <br/> |<span data-ttu-id="854aa-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="854aa-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="854aa-114">Área:</span><span class="sxs-lookup"><span data-stu-id="854aa-114">Area:</span></span>  <br/> |<span data-ttu-id="854aa-115">Contact</span><span class="sxs-lookup"><span data-stu-id="854aa-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="854aa-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="854aa-116">Remarks</span></span>

<span data-ttu-id="854aa-117">Esta propiedad debe ser una combinación de otras propiedades de dirección física y se basa en la configuración regional del cliente.</span><span class="sxs-lookup"><span data-stu-id="854aa-117">This property should be a combination of other physical address properties, and is based on client locale.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="854aa-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="854aa-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="854aa-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="854aa-119">Protocol specifications</span></span>

<span data-ttu-id="854aa-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="854aa-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="854aa-121">Proporciona definición de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="854aa-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="854aa-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="854aa-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="854aa-123">Especifica las propiedades y operaciones que se admiten para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="854aa-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="854aa-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="854aa-124">Header files</span></span>

<span data-ttu-id="854aa-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="854aa-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="854aa-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="854aa-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="854aa-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="854aa-127">See also</span></span>



[<span data-ttu-id="854aa-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="854aa-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="854aa-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="854aa-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="854aa-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="854aa-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="854aa-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="854aa-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

