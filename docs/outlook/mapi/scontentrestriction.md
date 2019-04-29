---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423667"
---
# <a name="scontentrestriction"></a><span data-ttu-id="b7032-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="b7032-103">SContentRestriction</span></span>
 
<span data-ttu-id="b7032-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7032-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7032-105">Describe una restricción de contenido, que se usa para limitar una vista de tabla a sólo las filas que incluyen una columna con el contenido que coincide con una cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b7032-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7032-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b7032-106">Header file:</span></span>  <br/> |<span data-ttu-id="b7032-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b7032-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="b7032-108">Members</span><span class="sxs-lookup"><span data-stu-id="b7032-108">Members</span></span>

<span data-ttu-id="b7032-109">**ulFuzzyLevel**</span><span class="sxs-lookup"><span data-stu-id="b7032-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="b7032-110">Opciones que definen el nivel de precisión que debe cumplir la restricción de contenido cuando se comprueba si coinciden.</span><span class="sxs-lookup"><span data-stu-id="b7032-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="b7032-111">Los **16 bits inferiores** del miembro **ulFuzzyLevel** se aplican a las propiedades del tipo PT_BINARY y PT_STRING8 y deben establecerse en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7032-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="b7032-112">FL_FULLSTRING: para que se cumpla, la cadena de búsqueda **lpProp** debe estar contenida en la propiedad identificada por **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="b7032-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="b7032-113">FL_PREFIX: para que se cumpla, la cadena de búsqueda **lpProp** debe aparecer al principio de la propiedad identificada por **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="b7032-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="b7032-114">Las dos cadenas solo deben compararse hasta la longitud de la cadena de búsqueda indicada por **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="b7032-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="b7032-115">FL_SUBSTRING: para que se cumpla, la cadena de búsqueda **lpProp** debe estar contenida en cualquier parte de la propiedad identificada por **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="b7032-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="b7032-116">Los **16 bits superiores** del miembro **ulFuzzyLevel** solo se aplican a propiedades de tipo PT_STRING8 y se pueden establecer en cualquier combinación de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="b7032-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="b7032-117">FL_IGNORECASE: la comparación debe realizarse sin tener en cuenta el caso.</span><span class="sxs-lookup"><span data-stu-id="b7032-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="b7032-118">FL_IGNORENONSPACE: la comparación debe omitir los caracteres no de espaciado definidos en Unicode, como las marcas diacríticas.</span><span class="sxs-lookup"><span data-stu-id="b7032-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="b7032-119">FL_LOOSE: la comparación debe darle una coincidencia siempre que sea posible, sin tener en cuenta los caracteres de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b7032-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="b7032-120">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="b7032-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="b7032-121">Etiqueta de propiedad que identifica la propiedad de cadena que se va a comprobar para comprobar si se ha encontrado la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b7032-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="b7032-122">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="b7032-122">**lpProp**</span></span>
  
> <span data-ttu-id="b7032-123">Puntero a una estructura de valor de propiedad que contiene el valor de cadena que se va a usar como cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b7032-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7032-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7032-124">Remarks</span></span>

<span data-ttu-id="b7032-125">Hay dos etiquetas de propiedad en una estructura **SContentRestriction** : una en el miembro **ulPropTag** y otra en el miembro **ulPropTag** de la estructura **SPropValue** a la que apunta **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="b7032-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="b7032-126">En ambas etiquetas, MAPI solo requiere el campo de tipo de propiedad y omite el campo de identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="b7032-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="b7032-127">Sin embargo, los dos tipos de propiedad deben coincidir o, de lo contrario, se devuelve el valor de error MAPI_E_TOO_COMPLEX cuando se usa la restricción en una llamada a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="b7032-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="b7032-128">Los valores FL_FULLSTRING, FL_PREFIX y FL_SUBSTRING se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="b7032-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="b7032-129">Solo se puede establecer una de ellas y se debe establecer una de ellas.</span><span class="sxs-lookup"><span data-stu-id="b7032-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="b7032-130">Los significados son fijos y el proveedor debe implementarlos exactamente como están definidos.</span><span class="sxs-lookup"><span data-stu-id="b7032-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="b7032-131">El proveedor debe devolver MAPI_E_TOO_COMPLEX si no puede admitir estos valores.</span><span class="sxs-lookup"><span data-stu-id="b7032-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="b7032-132">Los valores FL_IGNORECASE, FL_IGNORENONSPACE y FL_LOOSE son independientes.</span><span class="sxs-lookup"><span data-stu-id="b7032-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="b7032-133">Se puede establecer cualquier parte de cero a los tres.</span><span class="sxs-lookup"><span data-stu-id="b7032-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="b7032-134">Sus definiciones se proporcionan solo como guía y el proveedor es gratuito para implementar su propio significado específico de cada marca.</span><span class="sxs-lookup"><span data-stu-id="b7032-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="b7032-135">El proveedor no debe devolver ninguna indicación de error si no tiene ninguna implementación de un indicador especificado.</span><span class="sxs-lookup"><span data-stu-id="b7032-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="b7032-136">El resultado de una restricción de contenido impuesta a una propiedad no está definido cuando la propiedad no existe.</span><span class="sxs-lookup"><span data-stu-id="b7032-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="b7032-137">Cuando un cliente requiere un comportamiento bien definido para dicha restricción y no está seguro de si la propiedad existe por ejemplo, no es una columna obligatoria de una tabla, por lo que debe crear una restricción **and** para unirse a la restricción de contenido con una restricción exist.</span><span class="sxs-lookup"><span data-stu-id="b7032-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="b7032-138">Use una estructura [SExistRestriction](sexistrestriction.md) para definir la restricción EXISTS y una estructura [SAndRestriction](sandrestriction.md) para definir la restricción **and** .</span><span class="sxs-lookup"><span data-stu-id="b7032-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="b7032-139">Para obtener más información acerca de las restricciones y la estructura **SContentRestriction** en general, consulte [About Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="b7032-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b7032-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="b7032-140">See also</span></span>

- [<span data-ttu-id="b7032-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b7032-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="b7032-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="b7032-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="b7032-143">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="b7032-143">MAPI Structures</span></span>](mapi-structures.md)

