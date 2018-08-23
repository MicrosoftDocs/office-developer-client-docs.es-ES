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
ms.openlocfilehash: 27659b69e0ae050206de18c1258ee593737fbd3b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592951"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="29aef-103">Propiedad canónica PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="29aef-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="29aef-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29aef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29aef-105">Contiene el identificador de entrada de objeto de Active directory de un miembro de tabla del sistema (SACL) de la lista de control de acceso.</span><span class="sxs-lookup"><span data-stu-id="29aef-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="29aef-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="29aef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29aef-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="29aef-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="29aef-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="29aef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="29aef-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="29aef-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="29aef-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="29aef-110">Data type:</span></span>  <br/> |<span data-ttu-id="29aef-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="29aef-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="29aef-112">Área:</span><span class="sxs-lookup"><span data-stu-id="29aef-112">Area:</span></span>  <br/> |<span data-ttu-id="29aef-113">Reglas del servidor</span><span class="sxs-lookup"><span data-stu-id="29aef-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29aef-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29aef-114">Remarks</span></span>

<span data-ttu-id="29aef-115">Esta propiedad se usa con la interfaz de [IExchangeModifyTable](iexchangemodifytableiunknown.md) para identificar de forma exclusiva una persona o la función a la que se aplica la SACL.</span><span class="sxs-lookup"><span data-stu-id="29aef-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="29aef-116">Una vez creado un miembro de la tabla SACL, no se puede cambiar la **propiedad ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="29aef-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="29aef-117">Para cambiarlo, debe eliminar al miembro de la tabla y volver a crearlo con una **propiedad ENTRYID**de diferentes.</span><span class="sxs-lookup"><span data-stu-id="29aef-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="29aef-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="29aef-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="29aef-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="29aef-119">Header files</span></span>

<span data-ttu-id="29aef-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29aef-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="29aef-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="29aef-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="29aef-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="29aef-122">Mapitags.h</span></span>
  
> <span data-ttu-id="29aef-123">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="29aef-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29aef-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="29aef-124">See also</span></span>



[<span data-ttu-id="29aef-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="29aef-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="29aef-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="29aef-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29aef-127">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="29aef-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29aef-128">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="29aef-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

