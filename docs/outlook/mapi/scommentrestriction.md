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
ms.openlocfilehash: 84fb79b1922669db9c8e5d518a833a6866f11cea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589185"
---
# <a name="scommentrestriction"></a><span data-ttu-id="006c5-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="006c5-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="006c5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="006c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="006c5-105">Describe una restricción de comentario, que se usa para realizar anotaciones en una restricción.</span><span class="sxs-lookup"><span data-stu-id="006c5-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="006c5-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="006c5-106">Header file:</span></span>  <br/> |<span data-ttu-id="006c5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="006c5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="006c5-108">Members</span><span class="sxs-lookup"><span data-stu-id="006c5-108">Members</span></span>

 <span data-ttu-id="006c5-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="006c5-109">**cValues**</span></span>
  
> <span data-ttu-id="006c5-110">Recuento de valores de propiedad en la matriz indicada por el miembro **lpProp** .</span><span class="sxs-lookup"><span data-stu-id="006c5-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="006c5-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="006c5-111">**lpRes**</span></span>
  
> <span data-ttu-id="006c5-112">Puntero a una estructura [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="006c5-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="006c5-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="006c5-113">**lpProp**</span></span>
  
> <span data-ttu-id="006c5-114">Puntero a una matriz de estructuras [SPropValue](spropvalue.md) , cada uno con la etiqueta de la propiedad y el valor de una propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="006c5-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="006c5-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="006c5-115">Remarks</span></span>

<span data-ttu-id="006c5-116">La estructura **SCommentRestriction** asocia un objeto junto con un conjunto de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="006c5-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="006c5-117">Restricciones de comentario son a diferencia de otras restricciones debido a que no se evalúan.</span><span class="sxs-lookup"><span data-stu-id="006c5-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="006c5-118">Es decir, se tendrán en cuenta en el método [IMAPITable:: Restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="006c5-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="006c5-119">No hay ningún efecto en las filas devueltas por el método [IMAPITable:: QueryRows](imapitable-queryrows.md) después de que se ha realizado una llamada **IMAPITable:: Restrict** .</span><span class="sxs-lookup"><span data-stu-id="006c5-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="006c5-120">La estructura de **SCommentRestriction** puede usarse para mantener la información específica de la aplicación con una restricción de cuando se guarda en el disco.</span><span class="sxs-lookup"><span data-stu-id="006c5-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="006c5-121">Por ejemplo, un cliente de guardar el nombre de una propiedad con nombre que se usa en una restricción de propiedad puede hacerlo en una estructura **SCommentRestriction** .</span><span class="sxs-lookup"><span data-stu-id="006c5-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="006c5-122">Guardar un nombre de propiedad no es posible en una restricción de propiedad debido a que la estructura [SPropertyRestriction](spropertyrestriction.md) asociada contiene sólo la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="006c5-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="006c5-123">Para obtener más información sobre la estructura de **SCommentRestriction** y restricciones en general, vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="006c5-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="006c5-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="006c5-124">See also</span></span>



[<span data-ttu-id="006c5-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="006c5-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="006c5-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="006c5-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="006c5-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="006c5-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="006c5-128">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="006c5-128">MAPI Structures</span></span>](mapi-structures.md)

