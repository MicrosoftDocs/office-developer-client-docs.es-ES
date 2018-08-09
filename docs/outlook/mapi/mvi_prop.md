---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f8f58ee18095dec8a222ae8b5a19cbefbaafa663
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818441"
---
# <a name="mviprop"></a><span data-ttu-id="58f9e-103">MVI_PROP</span><span class="sxs-lookup"><span data-stu-id="58f9e-103">MVI_PROP</span></span>

  
  
<span data-ttu-id="58f9e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58f9e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58f9e-105">Establece el MVI_FLAG para una propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="58f9e-105">Sets the MVI_FLAG for a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58f9e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="58f9e-106">Header file:</span></span>  <br/> |<span data-ttu-id="58f9e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58f9e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="58f9e-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="58f9e-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="58f9e-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="58f9e-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a><span data-ttu-id="58f9e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58f9e-110">Parameters</span></span>

 <span data-ttu-id="58f9e-111">_etiqueta_</span><span class="sxs-lookup"><span data-stu-id="58f9e-111">_tag_</span></span>
  
> <span data-ttu-id="58f9e-112">La etiqueta de propiedad que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="58f9e-112">The property tag to be modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58f9e-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58f9e-113">Remarks</span></span>

<span data-ttu-id="58f9e-114">El MVI_FLAG se combina la configuración de MV_FLAG, que identifica una propiedad como multivalor y MV_INSTANCE, que solicita que se muestre una propiedad con varios valores en una tabla en varias filas.</span><span class="sxs-lookup"><span data-stu-id="58f9e-114">The MVI_FLAG combines the setting of MV_FLAG, identifying a property as multi-valued, and MV_INSTANCE, requesting that a multi-valued property be displayed in a table in multiple rows.</span></span> <span data-ttu-id="58f9e-115">Se modifica el tipo de propiedad de la propiedad afectado, pero el identificador permanece inalterado.</span><span class="sxs-lookup"><span data-stu-id="58f9e-115">The property type of the affected property is modified, but the identifier remains unchanged.</span></span> 
  
<span data-ttu-id="58f9e-116">Por ejemplo, cuando la macro MVI_PROP se aplica a una propiedad de tipo PT_FLOAT, su tipo se cambia a PT_MV_FLOAT.</span><span class="sxs-lookup"><span data-stu-id="58f9e-116">For example, when the MVI_PROP macro is applied to a property of type PT_FLOAT, its type is changed to PT_MV_FLOAT.</span></span> <span data-ttu-id="58f9e-117">Cuando se incluye en una tabla, se usan varias filas para representar la propiedad que tiene una fila para cada valor.</span><span class="sxs-lookup"><span data-stu-id="58f9e-117">When included in a table, multiple rows are used to represent the property that has one row for each value.</span></span> <span data-ttu-id="58f9e-118">Las propiedades de las demás columnas se repiten.</span><span class="sxs-lookup"><span data-stu-id="58f9e-118">The properties for the other columns are repeated.</span></span> 
  
<span data-ttu-id="58f9e-119">Para obtener más información acerca de estos indicadores, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md) y [trabajar con columnas con varios valores](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="58f9e-119">For more information about these flags, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="58f9e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="58f9e-120">See also</span></span>



[<span data-ttu-id="58f9e-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="58f9e-121">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="58f9e-122">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="58f9e-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

