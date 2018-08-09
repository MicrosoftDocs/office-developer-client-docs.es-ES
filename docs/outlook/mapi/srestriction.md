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
ms.openlocfilehash: 9748229799641d62b1649491c432f10164b49192
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820752"
---
# <a name="srestriction"></a><span data-ttu-id="f37d8-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-103">SRestriction</span></span>

  
  
<span data-ttu-id="f37d8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f37d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f37d8-105">Describe un filtro para limitar la vista de una tabla a las filas determinadas.</span><span class="sxs-lookup"><span data-stu-id="f37d8-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f37d8-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f37d8-106">Header file:</span></span>  <br/> |<span data-ttu-id="f37d8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f37d8-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="f37d8-108">Members</span><span class="sxs-lookup"><span data-stu-id="f37d8-108">Members</span></span>

 <span data-ttu-id="f37d8-109">**RT**</span><span class="sxs-lookup"><span data-stu-id="f37d8-109">**rt**</span></span>
  
> <span data-ttu-id="f37d8-110">El tipo de restricción.</span><span class="sxs-lookup"><span data-stu-id="f37d8-110">The restriction type.</span></span> <span data-ttu-id="f37d8-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f37d8-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="f37d8-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="f37d8-112">RES_AND</span></span> 
  
> <span data-ttu-id="f37d8-113">Una restricción **y** que se aplica una operación **AND** bit a bit a una restricción.</span><span class="sxs-lookup"><span data-stu-id="f37d8-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="f37d8-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="f37d8-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="f37d8-115">Una restricción de la máscara de bits que se aplica una máscara de bits para un valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f37d8-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="f37d8-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="f37d8-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="f37d8-117">Una restricción de comentario, que asocia un comentario a una restricción.</span><span class="sxs-lookup"><span data-stu-id="f37d8-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="f37d8-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="f37d8-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="f37d8-119">Restricción de comparación de propiedad, que compara dos valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="f37d8-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="f37d8-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="f37d8-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="f37d8-121">Una restricción de contenido, que busca un valor de la propiedad de contenido específico.</span><span class="sxs-lookup"><span data-stu-id="f37d8-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="f37d8-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="f37d8-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="f37d8-123">Una restricción existe, que determina si se admite una propiedad.</span><span class="sxs-lookup"><span data-stu-id="f37d8-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="f37d8-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="f37d8-124">RES_NOT</span></span> 
  
> <span data-ttu-id="f37d8-125">Una **no** restricción, que se aplica una operación **NOT** lógica a una restricción.</span><span class="sxs-lookup"><span data-stu-id="f37d8-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="f37d8-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="f37d8-126">RES_OR</span></span> 
  
> <span data-ttu-id="f37d8-127">Una restricción **o** , que se aplica una operación **OR** lógica a una restricción.</span><span class="sxs-lookup"><span data-stu-id="f37d8-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="f37d8-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="f37d8-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="f37d8-129">Una restricción de propiedad, que determina si un valor de propiedad coincide con un valor determinado.</span><span class="sxs-lookup"><span data-stu-id="f37d8-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="f37d8-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="f37d8-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="f37d8-131">Una restricción de tamaño, que determina si un valor de la propiedad es un determinado tamaño.</span><span class="sxs-lookup"><span data-stu-id="f37d8-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="f37d8-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="f37d8-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="f37d8-133">Una restricción de objeto subcaracterística, que se aplica una restricción a los datos adjuntos o los destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f37d8-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="f37d8-134">**res**</span><span class="sxs-lookup"><span data-stu-id="f37d8-134">**res**</span></span>
  
> <span data-ttu-id="f37d8-135">Unión de las estructuras de restricción que describe el filtro que se aplique.</span><span class="sxs-lookup"><span data-stu-id="f37d8-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="f37d8-136">La estructura específica incluida en el miembro **rec** depende del valor del miembro **rt** .</span><span class="sxs-lookup"><span data-stu-id="f37d8-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="f37d8-137">La asignación entre el tipo de restricción y la estructura se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f37d8-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="f37d8-138">**Tipo de restricción**</span><span class="sxs-lookup"><span data-stu-id="f37d8-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="f37d8-139">**Estructura de restricción**</span><span class="sxs-lookup"><span data-stu-id="f37d8-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="f37d8-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="f37d8-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="f37d8-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="f37d8-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="f37d8-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="f37d8-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="f37d8-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="f37d8-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="f37d8-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="f37d8-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="f37d8-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="f37d8-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="f37d8-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="f37d8-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="f37d8-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="f37d8-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="f37d8-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="f37d8-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="f37d8-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="f37d8-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="f37d8-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="f37d8-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="f37d8-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="f37d8-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="f37d8-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="f37d8-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="f37d8-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="f37d8-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="f37d8-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="f37d8-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="f37d8-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="f37d8-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="f37d8-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f37d8-162">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f37d8-162">Remarks</span></span>

<span data-ttu-id="f37d8-163">Los clientes usan una estructura **SRestriction** para limitar el número y el tipo de filas en la vista de una tabla y para buscar mensajes específicos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f37d8-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="f37d8-164">Para imponer la limitación en una tabla, los clientes llaman [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="f37d8-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="f37d8-165">Para imponer la limitación en una carpeta, los clientes llaman (método) [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f37d8-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="f37d8-166">Para obtener información acerca de cómo usar restricciones con tablas, vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="f37d8-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f37d8-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="f37d8-167">See also</span></span>



[<span data-ttu-id="f37d8-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="f37d8-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="f37d8-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="f37d8-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="f37d8-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="f37d8-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="f37d8-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="f37d8-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="f37d8-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="f37d8-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="f37d8-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="f37d8-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="f37d8-179">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="f37d8-179">MAPI Structures</span></span>](mapi-structures.md)

