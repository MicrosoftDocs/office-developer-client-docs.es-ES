---
title: Propiedad canónica PidTagMemberId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberId
api_type:
- HeaderDef
ms.assetid: 64faef3c-27b2-49d2-9d0c-8b9d33f1cb71
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b5d1d4456856f1640bbed8589fc0583060cd2520
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391748"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="692af-103">Propiedad canónica PidTagMemberId</span><span class="sxs-lookup"><span data-stu-id="692af-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="692af-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="692af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="692af-105">Contiene el identificador de un miembro de la tabla que tiene los derechos que se describe en una carpeta de Microsoft Exchange Server o el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="692af-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="692af-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="692af-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="692af-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="692af-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="692af-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="692af-108">Identifier:</span></span>  <br/> |<span data-ttu-id="692af-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="692af-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="692af-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="692af-110">Data type:</span></span>  <br/> |<span data-ttu-id="692af-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="692af-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="692af-112">Área:</span><span class="sxs-lookup"><span data-stu-id="692af-112">Area:</span></span>  <br/> |<span data-ttu-id="692af-113">Control de acceso</span><span class="sxs-lookup"><span data-stu-id="692af-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="692af-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="692af-114">Remarks</span></span>

<span data-ttu-id="692af-115">Esta propiedad devuelve un identificador único para la tabla.</span><span class="sxs-lookup"><span data-stu-id="692af-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="692af-116">Un identificador de usuario de Active directory está asociado con cada identificador de miembro y viene dado por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="692af-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="692af-117">Esta propiedad se usa en la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) para recuperar el identificador de entrada de Active directory de un miembro con derechos explícitos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="692af-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="692af-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="692af-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="692af-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="692af-119">Protocol specifications</span></span>

<span data-ttu-id="692af-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="692af-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="692af-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="692af-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="692af-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="692af-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="692af-123">Controla la recuperación de listas de permisos de carpeta que se almacenan en el servidor.</span><span class="sxs-lookup"><span data-stu-id="692af-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="692af-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="692af-124">Header files</span></span>

<span data-ttu-id="692af-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="692af-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="692af-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="692af-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="692af-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="692af-127">Mapitags.h</span></span>
  
> <span data-ttu-id="692af-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="692af-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="692af-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="692af-129">See also</span></span>



[<span data-ttu-id="692af-130">Propiedad canónica PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="692af-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="692af-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="692af-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="692af-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="692af-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="692af-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="692af-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="692af-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="692af-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

