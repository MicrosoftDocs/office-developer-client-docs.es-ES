---
title: Propiedad canónica PidTagRulesTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4b4b60084b8cb53a0a245b502b8fe70241fb4eb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591696"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="c169e-103">Propiedad canónica PidTagRulesTable</span><span class="sxs-lookup"><span data-stu-id="c169e-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="c169e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c169e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c169e-105">Contiene una tabla con todas las reglas que se aplica a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c169e-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c169e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c169e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c169e-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="c169e-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="c169e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c169e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c169e-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="c169e-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="c169e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c169e-110">Data type:</span></span>  <br/> |<span data-ttu-id="c169e-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="c169e-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="c169e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c169e-112">Area:</span></span>  <br/> |<span data-ttu-id="c169e-113">Reglas del servidor</span><span class="sxs-lookup"><span data-stu-id="c169e-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c169e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c169e-114">Remarks</span></span>

<span data-ttu-id="c169e-115">Esta propiedad está presente en todos los objetos de carpeta en un servidor de Exchange que tienen las reglas.</span><span class="sxs-lookup"><span data-stu-id="c169e-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="c169e-116">Los valores incluidos en esta propiedad se usan para leer y modificar las reglas.</span><span class="sxs-lookup"><span data-stu-id="c169e-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="c169e-117">Puede usar el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con el identificador de la interfaz **IID_IExchangeModifyTable** para obtener un [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) interfaz a la tabla de reglas en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c169e-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="c169e-118">Puede usar esta interfaz para leer y modificar las reglas.</span><span class="sxs-lookup"><span data-stu-id="c169e-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c169e-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c169e-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c169e-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c169e-120">Header files</span></span>

<span data-ttu-id="c169e-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c169e-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="c169e-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c169e-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="c169e-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c169e-123">Mapitags.h</span></span>
  
> <span data-ttu-id="c169e-124">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="c169e-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c169e-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c169e-125">See also</span></span>



[<span data-ttu-id="c169e-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c169e-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="c169e-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="c169e-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="c169e-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c169e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c169e-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c169e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c169e-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c169e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c169e-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c169e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

