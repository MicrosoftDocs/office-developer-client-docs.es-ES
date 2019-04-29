---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418942"
---
# <a name="sexistrestriction"></a><span data-ttu-id="fd41a-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="fd41a-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="fd41a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd41a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd41a-105">Describe una restricción exist que se usa para comprobar si una propiedad determinada existe como una columna en la tabla.</span><span class="sxs-lookup"><span data-stu-id="fd41a-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd41a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="fd41a-106">Header file:</span></span>  <br/> |<span data-ttu-id="fd41a-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fd41a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="fd41a-108">Members</span><span class="sxs-lookup"><span data-stu-id="fd41a-108">Members</span></span>

 <span data-ttu-id="fd41a-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="fd41a-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="fd41a-110">Reserve debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fd41a-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="fd41a-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="fd41a-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="fd41a-112">Etiqueta de propiedad que identifica la columna que se va a probar para la existencia en cada fila.</span><span class="sxs-lookup"><span data-stu-id="fd41a-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="fd41a-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="fd41a-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="fd41a-114">Reserve debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fd41a-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd41a-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fd41a-115">Remarks</span></span>

<span data-ttu-id="fd41a-116">La restricción EXISTS se usa para garantizar resultados significativos para otros tipos de restricciones que implican propiedades, como las restricciones de contenido y propiedades.</span><span class="sxs-lookup"><span data-stu-id="fd41a-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="fd41a-117">Cuando se pasa una restricción que implica una propiedad a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md) y la propiedad no existe, los resultados de la restricción quedan sin definir.</span><span class="sxs-lookup"><span data-stu-id="fd41a-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="fd41a-118">Mediante la creación de una restricción **and** que combina la restricción de propiedad con una restricción exist, una persona que llama puede garantizar resultados precisos.</span><span class="sxs-lookup"><span data-stu-id="fd41a-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="fd41a-119">Las restricciones EXISTS no se pueden usar con propiedades de subobjeto que tienen el tipo PT Object.</span><span class="sxs-lookup"><span data-stu-id="fd41a-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="fd41a-120">Para obtener más información acerca de la estructura **SExistRestriction** , consulte [About Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="fd41a-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd41a-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="fd41a-121">See also</span></span>



[<span data-ttu-id="fd41a-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="fd41a-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="fd41a-123">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="fd41a-123">MAPI Structures</span></span>](mapi-structures.md)

