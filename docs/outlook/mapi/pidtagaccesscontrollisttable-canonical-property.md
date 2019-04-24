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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332007"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a><span data-ttu-id="f1683-103">Propiedad canónica PidTagAccessControlListTable</span><span class="sxs-lookup"><span data-stu-id="f1683-103">PidTagAccessControlListTable Canonical Property</span></span>

  
  
<span data-ttu-id="f1683-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1683-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1683-105">Contiene una tabla que consta de todas las listas de control de acceso al sistema (SACL) que se aplican a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f1683-105">Contains a table that consists of all the system access control lists (SACL) applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1683-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f1683-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1683-107">PR_ACL_TABLE</span><span class="sxs-lookup"><span data-stu-id="f1683-107">PR_ACL_TABLE</span></span>  <br/> |
|<span data-ttu-id="f1683-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f1683-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f1683-109">0x3FE0</span><span class="sxs-lookup"><span data-stu-id="f1683-109">0x3FE0</span></span>  <br/> |
|<span data-ttu-id="f1683-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f1683-110">Data type:</span></span>  <br/> |<span data-ttu-id="f1683-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="f1683-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="f1683-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f1683-112">Area:</span></span>  <br/> |<span data-ttu-id="f1683-113">Control de acceso</span><span class="sxs-lookup"><span data-stu-id="f1683-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1683-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1683-114">Remarks</span></span>

<span data-ttu-id="f1683-115">Esta propiedad está presente en todos los objetos de carpeta de un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f1683-115">This property is present on all folder objects on an Exchange Server.</span></span> <span data-ttu-id="f1683-116">Los valores incluidos en esta propiedad se usan para leer y modificar las listas de control de acceso (ACL) de las carpetas.</span><span class="sxs-lookup"><span data-stu-id="f1683-116">Values included in this property are used for reading and modifying access control lists (ACLs) on folders.</span></span> <span data-ttu-id="f1683-117">Puede usar el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) con el identificador de interfaz **IID_IExchangeModifyTable** para obtener una interfaz [IExchangeModifyTable: IUNKNOWN](iexchangemodifytableiunknown.md) a la tabla de ACL de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f1683-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the ACL table on a folder.</span></span> <span data-ttu-id="f1683-118">Puede usar esta interfaz para leer y modificar estas ACL.</span><span class="sxs-lookup"><span data-stu-id="f1683-118">You can use this interface to read and modify those ACLs.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f1683-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1683-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f1683-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f1683-120">Header files</span></span>

<span data-ttu-id="f1683-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f1683-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1683-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f1683-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="f1683-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f1683-123">Mapitags.h</span></span>
  
> <span data-ttu-id="f1683-124">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="f1683-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1683-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1683-125">See also</span></span>



[<span data-ttu-id="f1683-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f1683-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1683-127">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f1683-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1683-128">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f1683-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1683-129">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f1683-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

