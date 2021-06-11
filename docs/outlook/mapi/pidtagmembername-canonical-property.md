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
ms.openlocfilehash: a119cf1446600153e433c4aae99037d9810015c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342486"
---
# <a name="pidtagmembername-canonical-property"></a><span data-ttu-id="e50b0-103">Propiedad canónica PidTagMemberName</span><span class="sxs-lookup"><span data-stu-id="e50b0-103">PidTagMemberName Canonical Property</span></span>

  
  
<span data-ttu-id="e50b0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e50b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e50b0-105">Contiene el nombre para mostrar de un miembro de la tabla de lista de control de acceso (ACL).</span><span class="sxs-lookup"><span data-stu-id="e50b0-105">Contains the display name of a member of the access control list (ACL) table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e50b0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e50b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e50b0-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e50b0-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e50b0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e50b0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e50b0-109">0x6672</span><span class="sxs-lookup"><span data-stu-id="e50b0-109">0x6672</span></span>  <br/> |
|<span data-ttu-id="e50b0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e50b0-110">Data type:</span></span>  <br/> |<span data-ttu-id="e50b0-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="e50b0-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="e50b0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e50b0-112">Area:</span></span>  <br/> |<span data-ttu-id="e50b0-113">Control de acceso</span><span class="sxs-lookup"><span data-stu-id="e50b0-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e50b0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e50b0-114">Remarks</span></span>

<span data-ttu-id="e50b0-115">La interfaz [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) usa estas propiedades para mostrar el nombre de un miembro de una tabla acl, que es una persona o un rol con derechos explícitos en una carpeta o buzón.</span><span class="sxs-lookup"><span data-stu-id="e50b0-115">These properties are used by the [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to display the name of a member of an ACL table, which is a person or role with explicit rights on a folder or mailbox.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e50b0-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e50b0-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e50b0-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="e50b0-117">Protocol specifications</span></span>

<span data-ttu-id="e50b0-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e50b0-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e50b0-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="e50b0-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e50b0-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e50b0-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e50b0-121">Controla la recuperación de listas de permisos de carpetas almacenadas en el servidor.</span><span class="sxs-lookup"><span data-stu-id="e50b0-121">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e50b0-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e50b0-122">Header files</span></span>

<span data-ttu-id="e50b0-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e50b0-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e50b0-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e50b0-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e50b0-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e50b0-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e50b0-126">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="e50b0-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e50b0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e50b0-127">See also</span></span>



[<span data-ttu-id="e50b0-128">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e50b0-128">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="e50b0-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e50b0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e50b0-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e50b0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e50b0-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e50b0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e50b0-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e50b0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

