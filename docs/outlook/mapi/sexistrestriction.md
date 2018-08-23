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
ms.openlocfilehash: 218238bea277a2d57c77fcc9d71cd622f7da42fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571951"
---
# <a name="sexistrestriction"></a><span data-ttu-id="265dd-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="265dd-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="265dd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="265dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="265dd-105">Describe una restricción existente que se usa para comprobar si una propiedad determinada existe como una columna en la tabla.</span><span class="sxs-lookup"><span data-stu-id="265dd-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="265dd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="265dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="265dd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="265dd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="265dd-108">Members</span><span class="sxs-lookup"><span data-stu-id="265dd-108">Members</span></span>

 <span data-ttu-id="265dd-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="265dd-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="265dd-110">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="265dd-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="265dd-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="265dd-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="265dd-112">Etiqueta de la propiedad que identifica la columna que se va a la existencia de cada fila.</span><span class="sxs-lookup"><span data-stu-id="265dd-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="265dd-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="265dd-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="265dd-114">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="265dd-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="265dd-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="265dd-115">Remarks</span></span>

<span data-ttu-id="265dd-116">La restricción de existen se usa para garantizar resultados significativos para otros tipos de restricciones que impliquen propiedades, por ejemplo, restricciones de propiedad y contenido.</span><span class="sxs-lookup"><span data-stu-id="265dd-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="265dd-117">Cuando se pasa una restricción que implica una propiedad a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md) y la propiedad no existe, no están definidos los resultados de la restricción.</span><span class="sxs-lookup"><span data-stu-id="265dd-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="265dd-118">Mediante la creación de una restricción **y** que se une a la restricción de propiedad con una restricción existe, un autor de la llamada se pueda garantizar resultados precisos.</span><span class="sxs-lookup"><span data-stu-id="265dd-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="265dd-119">Existen restricciones no se puede usar con las propiedades del objeto subcaracterística que tienen tipo pt Object.</span><span class="sxs-lookup"><span data-stu-id="265dd-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="265dd-120">Para obtener más información acerca de la estructura **SExistRestriction** , vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="265dd-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="265dd-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="265dd-121">See also</span></span>



[<span data-ttu-id="265dd-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="265dd-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="265dd-123">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="265dd-123">MAPI Structures</span></span>](mapi-structures.md)

