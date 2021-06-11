---
title: Propiedad canónica PidTagAttachSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f3e4f19ab43a3da7c4840d762d5131813c83d996
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361092"
---
# <a name="pidtagattachsize-canonical-property"></a><span data-ttu-id="c6b38-103">Propiedad canónica PidTagAttachSize</span><span class="sxs-lookup"><span data-stu-id="c6b38-103">PidTagAttachSize Canonical Property</span></span>

  
  
<span data-ttu-id="c6b38-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6b38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6b38-105">Contiene la suma, en bytes, de los tamaños de todas las propiedades de un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="c6b38-105">Contains the sum, in bytes, of the sizes of all properties on an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6b38-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c6b38-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c6b38-107">PR_ATTACH_SIZE</span><span class="sxs-lookup"><span data-stu-id="c6b38-107">PR_ATTACH_SIZE</span></span>  <br/> |
|<span data-ttu-id="c6b38-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c6b38-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c6b38-109">0x0E20</span><span class="sxs-lookup"><span data-stu-id="c6b38-109">0x0E20</span></span>  <br/> |
|<span data-ttu-id="c6b38-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c6b38-110">Data type:</span></span>  <br/> |<span data-ttu-id="c6b38-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c6b38-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c6b38-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c6b38-112">Area:</span></span>  <br/> |<span data-ttu-id="c6b38-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="c6b38-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6b38-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c6b38-114">Remarks</span></span>

<span data-ttu-id="c6b38-115">Se recomienda que los subobjetos adjuntos **exponán la PR_ATTACH_SIZE** propiedad.</span><span class="sxs-lookup"><span data-stu-id="c6b38-115">It is recommended that attachment subobjects expose the **PR_ATTACH_SIZE** property.</span></span> <span data-ttu-id="c6b38-116">La suma contenida en **PR_ATTACH_SIZE** incluye el tamaño de la propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) o **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c6b38-116">The sum contained in **PR_ATTACH_SIZE** includes the size of the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> <span data-ttu-id="c6b38-117">Por lo tanto, **PR_ATTACH_SIZE** suele ser mayor que el contenido de los datos adjuntos solo.</span><span class="sxs-lookup"><span data-stu-id="c6b38-117">Accordingly, **PR_ATTACH_SIZE** is usually larger than the contents of the attachment alone.</span></span> 
  
<span data-ttu-id="c6b38-118">Esta propiedad se puede usar para comprobar el tamaño aproximado de los datos adjuntos antes de realizar una transferencia remota por módem y para mostrar indicadores de progreso al guardar los datos adjuntos en el disco.</span><span class="sxs-lookup"><span data-stu-id="c6b38-118">This property can be used to check the approximate size of the attachment before performing a remote transfer by modem and to display progress indicators when saving the attachment to disk.</span></span> <span data-ttu-id="c6b38-119">Es especialmente útil con objetos OLE adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c6b38-119">It is particularly useful with attached OLE objects.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c6b38-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6b38-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c6b38-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="c6b38-121">Protocol specifications</span></span>

<span data-ttu-id="c6b38-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6b38-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6b38-123">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="c6b38-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c6b38-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c6b38-124">Header files</span></span>

<span data-ttu-id="c6b38-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6b38-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c6b38-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c6b38-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c6b38-127">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c6b38-127">mapitags.h</span></span>
  
> <span data-ttu-id="c6b38-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c6b38-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6b38-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6b38-129">See also</span></span>



[<span data-ttu-id="c6b38-130">Propiedad canónica PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="c6b38-130">PidTagMessageSize Canonical Property</span></span>](pidtagmessagesize-canonical-property.md)


[<span data-ttu-id="c6b38-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c6b38-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c6b38-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c6b38-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c6b38-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c6b38-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c6b38-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c6b38-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

