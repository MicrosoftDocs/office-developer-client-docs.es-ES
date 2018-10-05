---
title: Propiedad canónica PidLidLogFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogFlags
api_type:
- COM
ms.assetid: 3174d931-e045-44db-a203-a27c9c00f4fc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a407c065a51870ba9908fbd9b626d7f287a1df4e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387240"
---
# <a name="pidlidlogflags-canonical-property"></a><span data-ttu-id="f1974-103">Propiedad canónica PidLidLogFlags</span><span class="sxs-lookup"><span data-stu-id="f1974-103">PidLidLogFlags Canonical Property</span></span>

  
  
<span data-ttu-id="f1974-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1974-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1974-105">Contiene metadatos sobre el diario.</span><span class="sxs-lookup"><span data-stu-id="f1974-105">Contains metadata about the journal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1974-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f1974-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1974-107">dispidLogFlags</span><span class="sxs-lookup"><span data-stu-id="f1974-107">dispidLogFlags</span></span>  <br/> |
|<span data-ttu-id="f1974-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="f1974-108">Property set:</span></span>  <br/> |<span data-ttu-id="f1974-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="f1974-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="f1974-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="f1974-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f1974-111">0x0000870C</span><span class="sxs-lookup"><span data-stu-id="f1974-111">0x0000870C</span></span>  <br/> |
|<span data-ttu-id="f1974-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f1974-112">Data type:</span></span>  <br/> |<span data-ttu-id="f1974-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f1974-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f1974-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f1974-114">Area:</span></span>  <br/> |<span data-ttu-id="f1974-115">Journal</span><span class="sxs-lookup"><span data-stu-id="f1974-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1974-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1974-116">Remarks</span></span>

<span data-ttu-id="f1974-117">El campo de bits que contiene metadatos sobre el diario debe ser cero o "0 x 40000000".</span><span class="sxs-lookup"><span data-stu-id="f1974-117">The bit field that contains metadata about the journal must be either zero or "0x40000000".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f1974-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1974-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f1974-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f1974-119">Protocol specifications</span></span>

<span data-ttu-id="f1974-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1974-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1974-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f1974-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f1974-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1974-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1974-123">Especifica las propiedades y operaciones que se permiten para diarios.</span><span class="sxs-lookup"><span data-stu-id="f1974-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f1974-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f1974-124">Header files</span></span>

<span data-ttu-id="f1974-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f1974-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1974-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f1974-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1974-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1974-127">See also</span></span>



[<span data-ttu-id="f1974-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f1974-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1974-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f1974-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1974-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f1974-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1974-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f1974-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

