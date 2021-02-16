---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 29d392eba530126e06a672c10044c5b4df0618c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406090"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="4f3c3-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="4f3c3-103">SPropertyRestriction</span></span>

<span data-ttu-id="4f3c3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f3c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f3c3-105">Describe una restricción de propiedad que se usa para hacer coincidir una constante con el valor de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f3c3-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4f3c3-106">Header file:</span></span>  <br/> |<span data-ttu-id="4f3c3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f3c3-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="4f3c3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4f3c3-108">Members</span></span>

<span data-ttu-id="4f3c3-109">**reeste**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-109">**relop**</span></span>
  
> <span data-ttu-id="4f3c3-110">Operador relacional que se usará en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="4f3c3-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4f3c3-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="4f3c3-112">RELOP_GE: la comparación se realiza en función de un primer valor mayor o igual.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="4f3c3-113">RELOP_GT: la comparación se realiza en función de un primer valor mayor.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="4f3c3-114">RELOP_LE: la comparación se realiza en función de un primer valor menor o igual.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="4f3c3-115">RELOP_LT: la comparación se realiza en función de un primer valor menor.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="4f3c3-116">RELOP_NE: la comparación se realiza en función de valores no iguales.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="4f3c3-117">RELOP_RE: la comparación se realiza en función de los valores LIKE (expresión regular).</span><span class="sxs-lookup"><span data-stu-id="4f3c3-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="4f3c3-118">RELOP_EQ: la comparación se realiza en función de valores iguales.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="4f3c3-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="4f3c3-120">Etiqueta de propiedad que identifica la propiedad que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="4f3c3-121">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-121">**lpProp**</span></span>
  
> <span data-ttu-id="4f3c3-122">Puntero a una [estructura SPropValue](spropvalue.md) que contiene el valor constante que se usará en la comparación.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4f3c3-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f3c3-123">Remarks</span></span>

<span data-ttu-id="4f3c3-124">Hay dos etiquetas de propiedad en una **estructura SPropertyRestriction.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="4f3c3-125">Una está en el **miembro ulPropTag** y la otra está en el miembro **ulPropTag** de la estructura **SPropValue** a la que apunta **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="4f3c3-126">MAPI requiere tanto el campo de identificador de propiedad como el campo de tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="4f3c3-127">El **ulPropTag** en **SPropertyRestriction** es la propiedad que se debe hacer coincidir y el puntero **lpProp** de **SPropertyRestriction** al tipo **de ulPropTag**'del **SPropValue** indica cómo se interpreta el valor de los miembros de la unión **lpProp.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="4f3c3-128">Los dos tipos de propiedad deben coincidir o, de lo contrario, se devuelve el valor de error MAPI_E_TOO_COMPLEX cuando se usa la restricción en una llamada a [IMAPITable::Restrict](imapitable-restrict.md) o [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="4f3c3-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="4f3c3-129">El orden de comparación _es (valor de propiedad) (operador relacional) (valor constante)._</span><span class="sxs-lookup"><span data-stu-id="4f3c3-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="4f3c3-130">Cuando se pasa una restricción de propiedad a **IMAPITable::Restrict** o **IMAPITable::FindRow** y la propiedad de destino no existe, los resultados de la restricción son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="4f3c3-131">Al crear una **restricción AND** que une la restricción de propiedad con una restricción **EXIST,** el autor de la llamada puede garantizar resultados precisos.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="4f3c3-132">Use una [estructura SExistRestriction](sexistrestriction.md) para definir la restricción **EXIST** y una estructura [SAndRestriction](sandrestriction.md) para definir la **restricción AND.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="4f3c3-133">Las etiquetas de propiedad de varios valores se pueden usar en restricciones de propiedad si el proveedor de servicios que implementa la tabla las admite.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="4f3c3-134">Si se admite, las etiquetas de propiedad de varios valores se pueden usar en cualquier lugar donde se puedan usar etiquetas de propiedad de un solo valor.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="4f3c3-135">Las etiquetas de propiedad de varios valores se pueden usar en los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4f3c3-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="4f3c3-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="4f3c3-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="4f3c3-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="4f3c3-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="4f3c3-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="4f3c3-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="4f3c3-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="4f3c3-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="4f3c3-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="4f3c3-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="4f3c3-141">Un caso notable cuando las dos etiquetas de propiedad no coinciden es si se restringe en una propiedad de varios valores.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="4f3c3-142">En este caso, lo siguiente debe ser verdadero.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-142">In this case the following must be true.</span></span> <span data-ttu-id="4f3c3-143">> Si el tipo de propiedad **de ulPropTag** de **SPropertyRestriction** contiene la marca de bits de tipo de propiedad multivalor MV_FLAG (0x1000), el tipo de propiedad **de ulPropTag** de **SPropValue** debe coincidir con el primero menos la marca de bits MV_FLAG, es decir, su inversa.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="4f3c3-144">> Por ejemplo, para restringir el uso de una propiedad de cadena personalizada de varios valores, como una categoría con una etiqueta de propiedad para la propiedad 0x8012101f, es decir, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), la **propiedad SPropertyRestriction** correspondiente aparecería de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="4f3c3-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> tenga en cuenta que si el tipo de propiedad **de ulPropTag** de **SPropValue** contiene la marca de MV_FLAG bits, es probable que se devuelva MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Note that if the property type of the **ulPropTag** of **SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="4f3c3-146">Para obtener más información acerca **de la estructura SPropertyRestriction,** vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="4f3c3-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f3c3-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4f3c3-147">See also</span></span>

- [<span data-ttu-id="4f3c3-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="4f3c3-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="4f3c3-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="4f3c3-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="4f3c3-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4f3c3-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="4f3c3-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="4f3c3-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="4f3c3-152">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="4f3c3-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="4f3c3-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="4f3c3-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="4f3c3-154">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="4f3c3-154">MAPI Structures</span></span>](mapi-structures.md)

