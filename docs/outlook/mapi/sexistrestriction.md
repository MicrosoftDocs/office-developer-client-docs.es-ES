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
# <a name="sexistrestriction"></a><span data-ttu-id="7f888-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="7f888-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="7f888-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f888-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f888-105">Describe una restricción existente que se usa para probar si una propiedad determinada existe como columna en la tabla.</span><span class="sxs-lookup"><span data-stu-id="7f888-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f888-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7f888-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f888-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f888-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="7f888-108">Members</span><span class="sxs-lookup"><span data-stu-id="7f888-108">Members</span></span>

 <span data-ttu-id="7f888-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="7f888-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="7f888-110">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7f888-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="7f888-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="7f888-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="7f888-112">Etiqueta de propiedad que identifica la columna que se va a probar para la existencia en cada fila.</span><span class="sxs-lookup"><span data-stu-id="7f888-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="7f888-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="7f888-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="7f888-114">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7f888-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f888-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f888-115">Remarks</span></span>

<span data-ttu-id="7f888-116">La restricción exist se usa para garantizar resultados significativos para otros tipos de restricciones que implican propiedades, como las restricciones de propiedades y contenido.</span><span class="sxs-lookup"><span data-stu-id="7f888-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="7f888-117">Cuando una restricción que implica una propiedad se pasa a [IMAPITable::Restrict](imapitable-restrict.md) o [IMAPITable::FindRow](imapitable-findrow.md) y la propiedad no existe, los resultados de la restricción son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="7f888-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="7f888-118">Al crear una **restricción AND** que une la restricción de propiedad con una restricción existente, se puede garantizar a un autor de la llamada resultados precisos.</span><span class="sxs-lookup"><span data-stu-id="7f888-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="7f888-119">Las restricciones existentes no se pueden usar con propiedades de sub object que tengan PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="7f888-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="7f888-120">Para obtener más información acerca **de la estructura SExistRestriction,** vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="7f888-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7f888-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f888-121">See also</span></span>



[<span data-ttu-id="7f888-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="7f888-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="7f888-123">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="7f888-123">MAPI Structures</span></span>](mapi-structures.md)

