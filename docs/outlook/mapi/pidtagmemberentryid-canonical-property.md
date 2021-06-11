---
title: Propiedad canónica PidTagMemberEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433041"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="cb5cf-103">Propiedad canónica PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="cb5cf-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="cb5cf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb5cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb5cf-105">Contiene el identificador de entrada de objeto de directorio de un miembro de tabla de lista de control de acceso del sistema (SACL).</span><span class="sxs-lookup"><span data-stu-id="cb5cf-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb5cf-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cb5cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb5cf-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cb5cf-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="cb5cf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cb5cf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cb5cf-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="cb5cf-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="cb5cf-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cb5cf-110">Data type:</span></span>  <br/> |<span data-ttu-id="cb5cf-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cb5cf-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cb5cf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cb5cf-112">Area:</span></span>  <br/> |<span data-ttu-id="cb5cf-113">Reglas del lado servidor</span><span class="sxs-lookup"><span data-stu-id="cb5cf-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb5cf-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb5cf-114">Remarks</span></span>

<span data-ttu-id="cb5cf-115">La interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) usa esta propiedad para identificar de forma única a una persona o rol a los que se aplica el SACL.</span><span class="sxs-lookup"><span data-stu-id="cb5cf-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="cb5cf-116">Después de crear un miembro en la tabla SACL, **el ENTRYID** no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="cb5cf-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="cb5cf-117">Para cambiarlo, debe eliminar el miembro de la tabla y volver a crearlo con un **ENTRYID diferente.**</span><span class="sxs-lookup"><span data-stu-id="cb5cf-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cb5cf-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb5cf-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cb5cf-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cb5cf-119">Header files</span></span>

<span data-ttu-id="cb5cf-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb5cf-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb5cf-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cb5cf-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="cb5cf-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cb5cf-122">Mapitags.h</span></span>
  
> <span data-ttu-id="cb5cf-123">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cb5cf-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb5cf-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb5cf-124">See also</span></span>



[<span data-ttu-id="cb5cf-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cb5cf-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb5cf-126">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="cb5cf-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb5cf-127">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cb5cf-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb5cf-128">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="cb5cf-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

