---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a2a6d273495df52adb83393dc5549b0872c8f6f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439362"
---
# <a name="srestriction"></a><span data-ttu-id="a59ec-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-103">SRestriction</span></span>

  
  
<span data-ttu-id="a59ec-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a59ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a59ec-105">Describe un filtro para limitar la vista de una tabla a filas específicas.</span><span class="sxs-lookup"><span data-stu-id="a59ec-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a59ec-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a59ec-106">Header file:</span></span>  <br/> |<span data-ttu-id="a59ec-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a59ec-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRestriction
{
  ULONG rt;
  union
  {
    SComparePropsRestriction resCompareProps;
    SAndRestriction resAnd;
    SOrRestriction resOr;
    SNotRestriction resNot;
    SContentRestriction resContent;
    SPropertyRestriction resProperty;
    SBitMaskRestriction resBitMask;
    SSizeRestriction resSize;
    SExistRestriction resExist;
    SSubRestriction resSub;
    SCommentRestriction resComment;
  } res;
} SRestriction;

```

## <a name="members"></a><span data-ttu-id="a59ec-108">Members</span><span class="sxs-lookup"><span data-stu-id="a59ec-108">Members</span></span>

 <span data-ttu-id="a59ec-109">**RT**</span><span class="sxs-lookup"><span data-stu-id="a59ec-109">**rt**</span></span>
  
> <span data-ttu-id="a59ec-110">El tipo de restricción.</span><span class="sxs-lookup"><span data-stu-id="a59ec-110">The restriction type.</span></span> <span data-ttu-id="a59ec-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a59ec-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="a59ec-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="a59ec-112">RES_AND</span></span> 
  
> <span data-ttu-id="a59ec-113">Una restricción **and** , que aplica una operación \*\*\*\* and bit a bit a una restricción.</span><span class="sxs-lookup"><span data-stu-id="a59ec-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="a59ec-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="a59ec-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="a59ec-115">Una restricción de máscara de máscara, que aplica una máscara de máscara a un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a59ec-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="a59ec-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="a59ec-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="a59ec-117">Una restricción de comentario, que asocia un comentario con una restricción.</span><span class="sxs-lookup"><span data-stu-id="a59ec-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="a59ec-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="a59ec-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="a59ec-119">Una restricción de comparación de propiedades, que compara dos valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a59ec-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="a59ec-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="a59ec-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="a59ec-121">Una restricción de contenido, que busca contenido específico en un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a59ec-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="a59ec-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="a59ec-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="a59ec-123">Una restricción EXISTS, que determina si se admite una propiedad.</span><span class="sxs-lookup"><span data-stu-id="a59ec-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="a59ec-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="a59ec-124">RES_NOT</span></span> 
  
> <span data-ttu-id="a59ec-125">Una restricción **Not** que aplica una operación **Not** lógica a una restricción.</span><span class="sxs-lookup"><span data-stu-id="a59ec-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="a59ec-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="a59ec-126">RES_OR</span></span> 
  
> <span data-ttu-id="a59ec-127">Una restricción **or** que aplica una operación OR \*\*\*\* lógica a una restricción.</span><span class="sxs-lookup"><span data-stu-id="a59ec-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="a59ec-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="a59ec-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="a59ec-129">Una restricción de propiedad, que determina si un valor de propiedad coincide con un valor determinado.</span><span class="sxs-lookup"><span data-stu-id="a59ec-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="a59ec-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="a59ec-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="a59ec-131">Una restricción de tamaño, que determina si un valor de propiedad es un tamaño determinado.</span><span class="sxs-lookup"><span data-stu-id="a59ec-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="a59ec-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="a59ec-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="a59ec-133">Una restricción de subobjeto, que aplica una restricción a los datos adjuntos o destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a59ec-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="a59ec-134">**res**</span><span class="sxs-lookup"><span data-stu-id="a59ec-134">**res**</span></span>
  
> <span data-ttu-id="a59ec-135">Unión de estructuras de restricción que describen el filtro que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="a59ec-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="a59ec-136">La estructura específica que se incluye en el miembro **res** depende del valor del miembro **RT** .</span><span class="sxs-lookup"><span data-stu-id="a59ec-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="a59ec-137">La asignación entre el tipo de restricción y la estructura se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a59ec-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="a59ec-138">**Tipo de restricción**</span><span class="sxs-lookup"><span data-stu-id="a59ec-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="a59ec-139">**Estructura de restricción**</span><span class="sxs-lookup"><span data-stu-id="a59ec-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="a59ec-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="a59ec-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="a59ec-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="a59ec-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="a59ec-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="a59ec-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="a59ec-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="a59ec-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="a59ec-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="a59ec-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="a59ec-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="a59ec-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="a59ec-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="a59ec-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="a59ec-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="a59ec-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="a59ec-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="a59ec-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="a59ec-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="a59ec-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="a59ec-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="a59ec-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="a59ec-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="a59ec-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="a59ec-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="a59ec-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="a59ec-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="a59ec-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="a59ec-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="a59ec-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="a59ec-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="a59ec-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="a59ec-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a59ec-162">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a59ec-162">Remarks</span></span>

<span data-ttu-id="a59ec-163">Los clientes usan una estructura **SRestriction** para limitar el número y el tipo de filas en su vista de una tabla y para buscar mensajes específicos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a59ec-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="a59ec-164">Para imponer la limitación en una tabla, los clientes llaman a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="a59ec-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="a59ec-165">Para imponer la limitación en una carpeta, los clientes llaman al método [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a59ec-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="a59ec-166">Para obtener información acerca de cómo usar restricciones con tablas, consulte [About Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="a59ec-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a59ec-167">Ver también</span><span class="sxs-lookup"><span data-stu-id="a59ec-167">See also</span></span>



[<span data-ttu-id="a59ec-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="a59ec-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="a59ec-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="a59ec-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="a59ec-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="a59ec-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="a59ec-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="a59ec-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="a59ec-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="a59ec-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="a59ec-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="a59ec-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="a59ec-179">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="a59ec-179">MAPI Structures</span></span>](mapi-structures.md)

