---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430612"
---
# <a name="scommentrestriction"></a><span data-ttu-id="a06b1-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="a06b1-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="a06b1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a06b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a06b1-105">Describe una restricción de comentario, que se usa para anotar una restricción.</span><span class="sxs-lookup"><span data-stu-id="a06b1-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a06b1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a06b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="a06b1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a06b1-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="a06b1-108">Members</span><span class="sxs-lookup"><span data-stu-id="a06b1-108">Members</span></span>

 <span data-ttu-id="a06b1-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="a06b1-109">**cValues**</span></span>
  
> <span data-ttu-id="a06b1-110">Recuento de valores de propiedad en la matriz apuntada por el **miembro lpProp.**</span><span class="sxs-lookup"><span data-stu-id="a06b1-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="a06b1-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="a06b1-111">**lpRes**</span></span>
  
> <span data-ttu-id="a06b1-112">Puntero a una [estructura SRestriction.](srestriction.md)</span><span class="sxs-lookup"><span data-stu-id="a06b1-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="a06b1-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="a06b1-113">**lpProp**</span></span>
  
> <span data-ttu-id="a06b1-114">Puntero a una matriz de [estructuras SPropValue,](spropvalue.md) cada una que contiene la etiqueta de propiedad y el valor de una propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="a06b1-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a06b1-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a06b1-115">Remarks</span></span>

<span data-ttu-id="a06b1-116">La **estructura SCommentRestriction** asocia un objeto con un conjunto de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="a06b1-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="a06b1-117">Las restricciones de comentarios son distintas de otras restricciones porque no se evalúan.</span><span class="sxs-lookup"><span data-stu-id="a06b1-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="a06b1-118">Es decir, el método [IMAPITable::Restrict](imapitable-restrict.md) los omite.</span><span class="sxs-lookup"><span data-stu-id="a06b1-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="a06b1-119">No hay ningún efecto en las filas devueltas por el método [IMAPITable::QueryRows](imapitable-queryrows.md) después de realizar una llamada **IMAPITable::Restrict.**</span><span class="sxs-lookup"><span data-stu-id="a06b1-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="a06b1-120">La **estructura SCommentRestriction** se puede usar para mantener la información específica de la aplicación con una restricción cuando se guarda en disco.</span><span class="sxs-lookup"><span data-stu-id="a06b1-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="a06b1-121">Por ejemplo, un cliente que guarda el nombre de una propiedad con nombre usada en una restricción de propiedad puede hacerlo en una **estructura SCommentRestriction.**</span><span class="sxs-lookup"><span data-stu-id="a06b1-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="a06b1-122">No es posible guardar un nombre de propiedad en una restricción de propiedad porque la estructura [SPropertyRestriction](spropertyrestriction.md) asociada solo contiene la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a06b1-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="a06b1-123">Para obtener más información acerca de **la estructura de SCommentRestriction** y las restricciones en general, vea [About Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="a06b1-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a06b1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a06b1-124">See also</span></span>



[<span data-ttu-id="a06b1-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a06b1-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="a06b1-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="a06b1-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="a06b1-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="a06b1-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="a06b1-128">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="a06b1-128">MAPI Structures</span></span>](mapi-structures.md)

