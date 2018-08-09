---
title: Propiedad canónica PidTagMemberName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberName
api_type:
- HeaderDef
ms.assetid: e19129bf-d07c-4d2e-9d4d-edbfda088ea7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 694cc4e4626fb9070927232bb72252f716eb458e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819715"
---
# <a name="pidtagmembername-canonical-property"></a><span data-ttu-id="3d8b4-103">Propiedad canónica PidTagMemberName</span><span class="sxs-lookup"><span data-stu-id="3d8b4-103">PidTagMemberName Canonical Property</span></span>

  
  
<span data-ttu-id="3d8b4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d8b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d8b4-105">Contiene el nombre para mostrar de un miembro de la tabla (ACL) de la lista de control de acceso.</span><span class="sxs-lookup"><span data-stu-id="3d8b4-105">Contains the display name of a member of the access control list (ACL) table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d8b4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3d8b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d8b4-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="3d8b4-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="3d8b4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3d8b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d8b4-109">0x6672</span><span class="sxs-lookup"><span data-stu-id="3d8b4-109">0x6672</span></span>  <br/> |
|<span data-ttu-id="3d8b4-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3d8b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d8b4-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="3d8b4-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="3d8b4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3d8b4-112">Area:</span></span>  <br/> |<span data-ttu-id="3d8b4-113">Control de acceso</span><span class="sxs-lookup"><span data-stu-id="3d8b4-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d8b4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d8b4-114">Remarks</span></span>

<span data-ttu-id="3d8b4-115">Estas propiedades se usan por la [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) interfaz para mostrar el nombre de un miembro de una tabla ACL, que es una persona o la función con derechos explícitos en una carpeta o un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="3d8b4-115">These properties are used by the [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to display the name of a member of an ACL table, which is a person or role with explicit rights on a folder or mailbox.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3d8b4-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d8b4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d8b4-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3d8b4-117">Protocol specifications</span></span>

<span data-ttu-id="3d8b4-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d8b4-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d8b4-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3d8b4-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d8b4-120">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d8b4-120">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d8b4-121">Controla la recuperación de listas de permisos de carpeta que se almacenan en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3d8b4-121">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d8b4-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3d8b4-122">Header files</span></span>

<span data-ttu-id="3d8b4-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d8b4-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d8b4-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3d8b4-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d8b4-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3d8b4-125">Mapitags.h</span></span>
  
> <span data-ttu-id="3d8b4-126">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="3d8b4-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d8b4-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d8b4-127">See also</span></span>



[<span data-ttu-id="3d8b4-128">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3d8b4-128">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="3d8b4-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3d8b4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d8b4-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="3d8b4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d8b4-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3d8b4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d8b4-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="3d8b4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

