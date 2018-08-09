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
ms.openlocfilehash: d992c7ac43c736e01184e1f12b3ad366587c9b06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819152"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a><span data-ttu-id="b1c51-103">Propiedad canónica PidTagAccessControlListTable</span><span class="sxs-lookup"><span data-stu-id="b1c51-103">PidTagAccessControlListTable Canonical Property</span></span>

  
  
<span data-ttu-id="b1c51-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1c51-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1c51-105">Contiene una tabla que consta de todos los el sistema acceso a listas de control de (SACL) aplicadas a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b1c51-105">Contains a table that consists of all the system access control lists (SACL) applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1c51-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b1c51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1c51-107">PR_ACL_TABLE</span><span class="sxs-lookup"><span data-stu-id="b1c51-107">PR_ACL_TABLE</span></span>  <br/> |
|<span data-ttu-id="b1c51-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b1c51-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b1c51-109">0x3FE0</span><span class="sxs-lookup"><span data-stu-id="b1c51-109">0x3FE0</span></span>  <br/> |
|<span data-ttu-id="b1c51-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b1c51-110">Data type:</span></span>  <br/> |<span data-ttu-id="b1c51-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="b1c51-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="b1c51-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b1c51-112">Area:</span></span>  <br/> |<span data-ttu-id="b1c51-113">Control de acceso</span><span class="sxs-lookup"><span data-stu-id="b1c51-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1c51-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1c51-114">Remarks</span></span>

<span data-ttu-id="b1c51-115">Esta propiedad está presente en todos los objetos de carpeta en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b1c51-115">This property is present on all folder objects on an Exchange Server.</span></span> <span data-ttu-id="b1c51-116">Los valores incluidos en esta propiedad se usan para la lectura y modificación de control de acceso (ACL) enumera en las carpetas.</span><span class="sxs-lookup"><span data-stu-id="b1c51-116">Values included in this property are used for reading and modifying access control lists (ACLs) on folders.</span></span> <span data-ttu-id="b1c51-117">Puede usar el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con el identificador de la interfaz **IID_IExchangeModifyTable** para obtener un [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) interfaz para la tabla de ACL de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b1c51-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the ACL table on a folder.</span></span> <span data-ttu-id="b1c51-118">Puede usar esta interfaz para leer y modificar estas ACL.</span><span class="sxs-lookup"><span data-stu-id="b1c51-118">You can use this interface to read and modify those ACLs.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b1c51-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1c51-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b1c51-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b1c51-120">Header files</span></span>

<span data-ttu-id="b1c51-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1c51-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1c51-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b1c51-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="b1c51-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b1c51-123">Mapitags.h</span></span>
  
> <span data-ttu-id="b1c51-124">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="b1c51-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1c51-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1c51-125">See also</span></span>



[<span data-ttu-id="b1c51-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b1c51-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1c51-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b1c51-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1c51-128">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b1c51-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1c51-129">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b1c51-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

