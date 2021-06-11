---
title: Propiedad canónica PidTagAccessControlListTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9c71a2b806b810906c13ea4750e5491b1544f640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424507"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a><span data-ttu-id="ff7f4-103">Propiedad canónica PidTagAccessControlListTable</span><span class="sxs-lookup"><span data-stu-id="ff7f4-103">PidTagAccessControlListTable Canonical Property</span></span>

  
  
<span data-ttu-id="ff7f4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff7f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff7f4-105">Contiene una tabla que consta de todas las listas de control de acceso del sistema (SACL) aplicadas a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ff7f4-105">Contains a table that consists of all the system access control lists (SACL) applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff7f4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ff7f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff7f4-107">PR_ACL_TABLE</span><span class="sxs-lookup"><span data-stu-id="ff7f4-107">PR_ACL_TABLE</span></span>  <br/> |
|<span data-ttu-id="ff7f4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ff7f4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff7f4-109">0x3FE0</span><span class="sxs-lookup"><span data-stu-id="ff7f4-109">0x3FE0</span></span>  <br/> |
|<span data-ttu-id="ff7f4-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ff7f4-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff7f4-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="ff7f4-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="ff7f4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ff7f4-112">Area:</span></span>  <br/> |<span data-ttu-id="ff7f4-113">Control de acceso</span><span class="sxs-lookup"><span data-stu-id="ff7f4-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff7f4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ff7f4-114">Remarks</span></span>

<span data-ttu-id="ff7f4-115">Esta propiedad está presente en todos los objetos de carpeta de un Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ff7f4-115">This property is present on all folder objects on an Exchange Server.</span></span> <span data-ttu-id="ff7f4-116">Los valores incluidos en esta propiedad se usan para leer y modificar listas de control de acceso (ACL) en carpetas.</span><span class="sxs-lookup"><span data-stu-id="ff7f4-116">Values included in this property are used for reading and modifying access control lists (ACLs) on folders.</span></span> <span data-ttu-id="ff7f4-117">Puede usar el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con el identificador de interfaz IID_IExchangeModifyTable para obtener una [interfaz IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) **para** la tabla ACL de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ff7f4-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the ACL table on a folder.</span></span> <span data-ttu-id="ff7f4-118">Puede usar esta interfaz para leer y modificar esas ACL.</span><span class="sxs-lookup"><span data-stu-id="ff7f4-118">You can use this interface to read and modify those ACLs.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ff7f4-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff7f4-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ff7f4-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ff7f4-120">Header files</span></span>

<span data-ttu-id="ff7f4-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff7f4-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff7f4-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ff7f4-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff7f4-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff7f4-123">Mapitags.h</span></span>
  
> <span data-ttu-id="ff7f4-124">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="ff7f4-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff7f4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff7f4-125">See also</span></span>



[<span data-ttu-id="ff7f4-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ff7f4-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff7f4-127">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ff7f4-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff7f4-128">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ff7f4-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff7f4-129">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ff7f4-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

