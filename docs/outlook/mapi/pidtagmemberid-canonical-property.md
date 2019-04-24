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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342640"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="7674d-103">Propiedad canónica PidTagMemberId</span><span class="sxs-lookup"><span data-stu-id="7674d-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="7674d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7674d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7674d-105">Contiene el identificador de un miembro de tabla que tiene los derechos descritos en una carpeta o buzón de correo de Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7674d-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7674d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7674d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7674d-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="7674d-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="7674d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7674d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7674d-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="7674d-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="7674d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7674d-110">Data type:</span></span>  <br/> |<span data-ttu-id="7674d-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="7674d-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="7674d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7674d-112">Area:</span></span>  <br/> |<span data-ttu-id="7674d-113">Control de acceso</span><span class="sxs-lookup"><span data-stu-id="7674d-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7674d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7674d-114">Remarks</span></span>

<span data-ttu-id="7674d-115">Esta propiedad devuelve un identificador único para la tabla.</span><span class="sxs-lookup"><span data-stu-id="7674d-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="7674d-116">Un identificador de usuario de directorio está asociado a cada identificador de miembro y es proporcionado por esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7674d-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="7674d-117">Esta propiedad se usa en la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) para recuperar el identificador de entrada de directorio de un miembro con derechos explícitos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="7674d-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7674d-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7674d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7674d-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7674d-119">Protocol specifications</span></span>

<span data-ttu-id="7674d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7674d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7674d-121">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7674d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7674d-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7674d-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7674d-123">Controla la recuperación de listas de permisos de carpetas que se almacenan en el servidor.</span><span class="sxs-lookup"><span data-stu-id="7674d-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7674d-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7674d-124">Header files</span></span>

<span data-ttu-id="7674d-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7674d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7674d-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7674d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="7674d-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7674d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="7674d-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7674d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7674d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7674d-129">See also</span></span>



[<span data-ttu-id="7674d-130">Propiedad canónica PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="7674d-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="7674d-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7674d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7674d-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="7674d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7674d-133">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7674d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7674d-134">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7674d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

