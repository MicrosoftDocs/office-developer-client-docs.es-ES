---
title: Propiedad canónico PidLidDistributionListChecksum
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidDistributionListChecksum
api_type:
- COM
ms.assetid: bd50ab34-caae-4258-8afc-769e3cbc5220
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: bba1e78d79800b1c8e56ad50ce1abb144d4c9aae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818627"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a><span data-ttu-id="eebe9-103">Propiedad canónico PidLidDistributionListChecksum</span><span class="sxs-lookup"><span data-stu-id="eebe9-103">PidLidDistributionListChecksum Canonical Property</span></span>

  
  
<span data-ttu-id="eebe9-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eebe9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eebe9-105">Especifica la suma de comprobación de polinomial de 32 bits de redundancia cíclica (CRC-32) de verificación para obtener una lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="eebe9-105">Specifies the 32-bit cyclic redundancy check (CRC-32) polynomial checksum for a personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eebe9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="eebe9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eebe9-107">dispidDLChecksum</span><span class="sxs-lookup"><span data-stu-id="eebe9-107">dispidDLChecksum</span></span>  <br/> |
|<span data-ttu-id="eebe9-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="eebe9-108">Property set:</span></span>  <br/> |<span data-ttu-id="eebe9-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="eebe9-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="eebe9-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="eebe9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="eebe9-111">0x0000804C</span><span class="sxs-lookup"><span data-stu-id="eebe9-111">0x0000804C</span></span>  <br/> |
|<span data-ttu-id="eebe9-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="eebe9-112">Data type:</span></span>  <br/> |<span data-ttu-id="eebe9-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="eebe9-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="eebe9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="eebe9-114">Area:</span></span>  <br/> |<span data-ttu-id="eebe9-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="eebe9-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eebe9-116">Notas</span><span class="sxs-lookup"><span data-stu-id="eebe9-116">Remarks</span></span>

<span data-ttu-id="eebe9-117">El valor de esta propiedad puede usarse para detectar cuándo se actualizó la propiedad **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) sin actualizar las demás propiedades de miembro de lista de distribución personal calculando la CRC-32 en el existente valor de **dispidDLMembers** y comparar con el valor de la propiedad **dispidDLChecksum** .</span><span class="sxs-lookup"><span data-stu-id="eebe9-117">The value of this property can be used to detect when the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property was updated without updating the other personal distribution list member properties by computing the CRC-32 on the existing value of **dispidDLMembers** and comparing it with the value of the **dispidDLChecksum** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="eebe9-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="eebe9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eebe9-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="eebe9-119">Protocol specifications</span></span>

<span data-ttu-id="eebe9-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eebe9-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eebe9-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="eebe9-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eebe9-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eebe9-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eebe9-123">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="eebe9-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eebe9-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="eebe9-124">Header files</span></span>

<span data-ttu-id="eebe9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eebe9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="eebe9-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="eebe9-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eebe9-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="eebe9-127">See also</span></span>



[<span data-ttu-id="eebe9-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="eebe9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eebe9-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="eebe9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eebe9-130">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="eebe9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eebe9-131">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="eebe9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

