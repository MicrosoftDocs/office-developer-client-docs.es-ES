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
ms.openlocfilehash: 7d588380ccc84f51fe58bb0f092d5287b12b4270
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586539"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="8706b-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="8706b-103">SPropertyRestriction</span></span>

<span data-ttu-id="8706b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8706b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8706b-105">Describe una restricción de propiedad que se usa para que coincida con una constante con el valor de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="8706b-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8706b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8706b-106">Header file:</span></span>  <br/> |<span data-ttu-id="8706b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8706b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="8706b-108">Members</span><span class="sxs-lookup"><span data-stu-id="8706b-108">Members</span></span>

<span data-ttu-id="8706b-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="8706b-109">**relop**</span></span>
  
> <span data-ttu-id="8706b-110">Operador relacional que se usará en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8706b-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="8706b-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8706b-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="8706b-112">RELOP_GE: Se realiza la comparación basándose en el primer valor mayor o igual.</span><span class="sxs-lookup"><span data-stu-id="8706b-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="8706b-113">RELOP_GT: Se realiza la comparación basándose en un valor mayor de primera.</span><span class="sxs-lookup"><span data-stu-id="8706b-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="8706b-114">RELOP_LE: Se realiza la comparación basándose en el primer valor menor o igual.</span><span class="sxs-lookup"><span data-stu-id="8706b-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="8706b-115">RELOP_LT: Se realiza la comparación basándose en un valor menor de primera.</span><span class="sxs-lookup"><span data-stu-id="8706b-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="8706b-116">RELOP_NE: Se realiza la comparación basándose en valores desiguales.</span><span class="sxs-lookup"><span data-stu-id="8706b-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="8706b-117">RELOP_RE: La comparación se realiza en función de como valores (expresión regular).</span><span class="sxs-lookup"><span data-stu-id="8706b-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="8706b-118">RELOP_EQ: Se realiza la comparación basándose en valores iguales.</span><span class="sxs-lookup"><span data-stu-id="8706b-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="8706b-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="8706b-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="8706b-120">Etiqueta de la propiedad que identifica la propiedad que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="8706b-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="8706b-121">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="8706b-121">**lpProp**</span></span>
  
> <span data-ttu-id="8706b-122">Puntero a una estructura [SPropValue](spropvalue.md) que contiene el valor constante que se utilizará en la comparación.</span><span class="sxs-lookup"><span data-stu-id="8706b-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8706b-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8706b-123">Remarks</span></span>

<span data-ttu-id="8706b-124">Hay dos etiquetas de propiedad en una estructura **SPropertyRestriction** .</span><span class="sxs-lookup"><span data-stu-id="8706b-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="8706b-125">Uno se encuentra en el miembro **ulPropTag** y la otra es en el miembro **ulPropTag** de la estructura **SPropValue** que señala **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="8706b-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="8706b-126">MAPI requiere el campo de identificador de la propiedad y el campo de tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8706b-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="8706b-127">El **ulPropTag** en **SPropertyRestriction** es la propiedad que coincida, y el puntero de **lpProp** de la **SPropertyRestriction** a la **ulPropTag**del tipo de la **SPropValue** indica cómo el valor de los miembros de la Unión de **lpProp** se interpretan.</span><span class="sxs-lookup"><span data-stu-id="8706b-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="8706b-128">Deben coincidir con los tipos de dos propiedades, o bien el valor de error MAPI_E_TOO_COMPLEX se devuelve cuando se utiliza la restricción de una llamada a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="8706b-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="8706b-129">El orden de comparación es _(valor de la propiedad) (operador relacional) (valor constante)_.</span><span class="sxs-lookup"><span data-stu-id="8706b-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="8706b-130">Cuando una restricción de propiedad se pasa al **IMAPITable:: Restrict** o **IMAPITable:: FindRow** y la propiedad de destino no existe, no están definidos los resultados de la restricción.</span><span class="sxs-lookup"><span data-stu-id="8706b-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="8706b-131">Mediante la creación de una restricción **y** que se une a la restricción de propiedad con una restricción **existe** , un autor de la llamada se pueda garantizar resultados precisos.</span><span class="sxs-lookup"><span data-stu-id="8706b-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="8706b-132">Usar una estructura [SExistRestriction](sexistrestriction.md) para definir la restricción **existe** y una estructura [SAndRestriction](sandrestriction.md) para definir la restricción de **y** .</span><span class="sxs-lookup"><span data-stu-id="8706b-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="8706b-133">Etiquetas de varios valores de propiedad se pueden usar en restricciones de propiedad si el proveedor de servicios de implementación de la tabla es compatible con ellos.</span><span class="sxs-lookup"><span data-stu-id="8706b-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="8706b-134">Si se admite, se pueden usar etiquetas de varios valores de propiedad en cualquier lugar se pueden usar las etiquetas de propiedad de un solo valor.</span><span class="sxs-lookup"><span data-stu-id="8706b-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="8706b-135">Etiquetas de propiedad de varios valores se pueden usar en los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="8706b-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="8706b-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="8706b-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="8706b-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="8706b-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="8706b-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="8706b-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="8706b-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="8706b-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="8706b-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="8706b-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="8706b-141">Un caso notable cuando no coinciden con las etiquetas de dos propiedades es si restricción en una propiedad de varios valor.</span><span class="sxs-lookup"><span data-stu-id="8706b-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="8706b-142">En este caso lo siguiente debe ser true.</span><span class="sxs-lookup"><span data-stu-id="8706b-142">In this case the following must be true.</span></span> <span data-ttu-id="8706b-143">> Si el tipo de propiedad de la **ulPropTag** de **SPropertyRestriction** contiene el indicador de bits de tipo de propiedad de valor múltiple MV_FLAG (0 x 1000), el tipo de propiedad de la **ulPropTag** de **SPropValue** debe coincidir con la primera menos el MV_ Indicador de bits de indicador, es decir, su inversa.</span><span class="sxs-lookup"><span data-stu-id="8706b-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="8706b-144">> Por ejemplo, para restringir el uso de una propiedad de cadena personalizada de varios valores, como una categoría con una etiqueta de propiedad para la propiedad 0x8012101f, es decir, PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012)), el correspondiente **SPropertyRestriction** aparecería como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="8706b-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="8706b-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Tenga en cuenta que si el tipo de propiedad de la **ulPropTag** de **SPropValue** contiene el indicador de bits MV_FLAG, la devolución probablemente es MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="8706b-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Note that if the property type of the **ulPropTag** of **SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="8706b-146">Para obtener más información acerca de la estructura **SPropertyRestriction** , vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="8706b-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8706b-147">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8706b-147">See also</span></span>

- [<span data-ttu-id="8706b-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="8706b-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="8706b-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="8706b-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="8706b-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8706b-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="8706b-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="8706b-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="8706b-152">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="8706b-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="8706b-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="8706b-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="8706b-154">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="8706b-154">MAPI Structures</span></span>](mapi-structures.md)

