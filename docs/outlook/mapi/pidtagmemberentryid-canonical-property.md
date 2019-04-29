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
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="cba33-103">Propiedad canónica PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="cba33-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="cba33-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cba33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cba33-105">Contiene el identificador de entrada de objeto de directorio de un miembro de tabla de lista de control de acceso de sistema (SACL).</span><span class="sxs-lookup"><span data-stu-id="cba33-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cba33-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cba33-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cba33-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cba33-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="cba33-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cba33-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cba33-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="cba33-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="cba33-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cba33-110">Data type:</span></span>  <br/> |<span data-ttu-id="cba33-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cba33-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cba33-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cba33-112">Area:</span></span>  <br/> |<span data-ttu-id="cba33-113">Reglas del lado servidor</span><span class="sxs-lookup"><span data-stu-id="cba33-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cba33-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cba33-114">Remarks</span></span>

<span data-ttu-id="cba33-115">Esta propiedad se usa en la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) para identificar de forma única a una persona o función a la que se aplica la SACL.</span><span class="sxs-lookup"><span data-stu-id="cba33-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="cba33-116">Una vez que se crea un miembro en la tabla SACL, no se puede cambiar la propiedad **EntryID** .</span><span class="sxs-lookup"><span data-stu-id="cba33-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="cba33-117">Para cambiarlo, debe eliminar el miembro de tabla y volver a crearlo con un **EntryID**diferente.</span><span class="sxs-lookup"><span data-stu-id="cba33-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cba33-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cba33-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cba33-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cba33-119">Header files</span></span>

<span data-ttu-id="cba33-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cba33-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="cba33-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cba33-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="cba33-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="cba33-122">Mapitags.h</span></span>
  
> <span data-ttu-id="cba33-123">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cba33-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cba33-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="cba33-124">See also</span></span>



[<span data-ttu-id="cba33-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cba33-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cba33-126">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="cba33-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cba33-127">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cba33-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cba33-128">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="cba33-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

