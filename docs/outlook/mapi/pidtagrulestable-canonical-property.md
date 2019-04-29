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
ms.openlocfilehash: e1c670cd566e838104ae3d5480c2297f8632d899
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428504"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="b5def-103">Propiedad canónica PidTagRulesTable</span><span class="sxs-lookup"><span data-stu-id="b5def-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="b5def-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5def-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5def-105">Contiene una tabla con todas las reglas aplicadas a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b5def-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5def-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b5def-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5def-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="b5def-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="b5def-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b5def-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5def-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="b5def-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="b5def-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b5def-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5def-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="b5def-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="b5def-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b5def-112">Area:</span></span>  <br/> |<span data-ttu-id="b5def-113">Reglas del lado servidor</span><span class="sxs-lookup"><span data-stu-id="b5def-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5def-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5def-114">Remarks</span></span>

<span data-ttu-id="b5def-115">Esta propiedad está presente en todos los objetos de carpeta de un servidor de Exchange que tienen reglas.</span><span class="sxs-lookup"><span data-stu-id="b5def-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="b5def-116">Los valores incluidos en esta propiedad se usan para leer y modificar las reglas.</span><span class="sxs-lookup"><span data-stu-id="b5def-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="b5def-117">Puede usar el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) con el identificador de interfaz **IID_IExchangeModifyTable** para obtener una interfaz [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) a la tabla de reglas de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b5def-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="b5def-118">Puede usar esta interfaz para leer y modificar estas reglas.</span><span class="sxs-lookup"><span data-stu-id="b5def-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b5def-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5def-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b5def-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b5def-120">Header files</span></span>

<span data-ttu-id="b5def-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b5def-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5def-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b5def-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5def-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b5def-123">Mapitags.h</span></span>
  
> <span data-ttu-id="b5def-124">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="b5def-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b5def-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="b5def-125">See also</span></span>



[<span data-ttu-id="b5def-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b5def-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="b5def-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="b5def-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="b5def-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b5def-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5def-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="b5def-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5def-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b5def-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5def-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="b5def-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

