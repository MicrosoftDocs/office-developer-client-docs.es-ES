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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 34177aee48adad7eecb40836a247705fc22d2a32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820594"
---
# <a name="scontentrestriction"></a><span data-ttu-id="d2f54-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="d2f54-103">SContentRestriction</span></span>
 
<span data-ttu-id="d2f54-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2f54-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2f54-105">Describe una restricción de contenido, que se usa para limitar una vista de tabla a sólo las filas en las que incluyen una columna con contenido que coinciden con una cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d2f54-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2f54-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d2f54-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2f54-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2f54-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="d2f54-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d2f54-108">Members</span></span>

<span data-ttu-id="d2f54-109">**ulFuzzyLevel**</span><span class="sxs-lookup"><span data-stu-id="d2f54-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="d2f54-110">Configuración de opción definir el nivel de precisión que se debe aplicar la restricción de contenido al comprobar una coincidencia.</span><span class="sxs-lookup"><span data-stu-id="d2f54-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="d2f54-111">Los **16 bits inferiores** del miembro **ulFuzzyLevel** se aplican a las propiedades de tipo PT_BINARY y PT_STRING8 y debe establecerse en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="d2f54-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="d2f54-112">FL_FULLSTRING: Para hacer coincidir, la cadena de búsqueda **lpProp** debe estar incluida en la propiedad identificada por **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="d2f54-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="d2f54-113">FL_PREFIX: Para hacer coincidir, la cadena de búsqueda **lpProp** debe aparecer al principio de la propiedad identificada por **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="d2f54-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="d2f54-114">Las dos cadenas deben compararse sólo hasta la longitud de la cadena de búsqueda indicada por **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="d2f54-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="d2f54-115">FL_SUBSTRING: Para hacer coincidir, la cadena de búsqueda **lpProp** debe estar incluida en cualquier lugar en la propiedad identificada por **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="d2f54-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="d2f54-116">Los **16 bits superiores** del miembro **ulFuzzyLevel** sólo se aplican a las propiedades de tipo PT_STRING8 y se puede establecer en los siguientes valores en cualquier combinación:</span><span class="sxs-lookup"><span data-stu-id="d2f54-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="d2f54-117">FL_IGNORECASE: La comparación debe realizarse sin tener en cuenta el caso.</span><span class="sxs-lookup"><span data-stu-id="d2f54-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="d2f54-118">FL_IGNORENONSPACE: La comparación debe omitir definidas en Unicode caracteres sin espacios, como los signos diacríticos.</span><span class="sxs-lookup"><span data-stu-id="d2f54-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="d2f54-119">FL_LOOSE: La comparación debería proporcionarle a una coincidencia siempre que sea posible, se omite caso y caracteres sin espacios.</span><span class="sxs-lookup"><span data-stu-id="d2f54-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="d2f54-120">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="d2f54-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="d2f54-121">Etiqueta de la propiedad que identifica la propiedad de cadena para buscar la aparición de la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d2f54-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="d2f54-122">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="d2f54-122">**lpProp**</span></span>
  
> <span data-ttu-id="d2f54-123">Puntero a una estructura de valor de propiedad que contiene el valor de cadena que se utilizará como la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d2f54-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2f54-124">Notas</span><span class="sxs-lookup"><span data-stu-id="d2f54-124">Remarks</span></span>

<span data-ttu-id="d2f54-125">Hay dos etiquetas de propiedad en una estructura de **SContentRestriction** : uno en el miembro **ulPropTag** y la otra en el miembro **ulPropTag** de la estructura **SPropValue** apunta a **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="d2f54-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="d2f54-126">En ambas etiquetas, MAPI requiere sólo el campo de tipo de propiedad y omite el campo de identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d2f54-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="d2f54-127">Sin embargo, deben coincidir con los tipos de dos propiedades, o bien el valor de error MAPI_E_TOO_COMPLEX se devuelve cuando se utiliza la restricción de una llamada a [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="d2f54-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="d2f54-128">Los valores FL_FULLSTRING, FL_PREFIX y FL_SUBSTRING son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="d2f54-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="d2f54-129">Se puede establecer sólo uno de ellos y uno de ellos se debe establecer.</span><span class="sxs-lookup"><span data-stu-id="d2f54-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="d2f54-130">Se corrigen sus significados, y debe implementar el proveedor exactamente como se definió.</span><span class="sxs-lookup"><span data-stu-id="d2f54-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="d2f54-131">El proveedor debe devolver MAPI_E_TOO_COMPLEX si no es capaz de admitir estos valores.</span><span class="sxs-lookup"><span data-stu-id="d2f54-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="d2f54-132">Los valores FL_IGNORECASE, FL_IGNORENONSPACE y FL_LOOSE son independientes.</span><span class="sxs-lookup"><span data-stu-id="d2f54-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="d2f54-133">En cualquier lugar de cero a las tres de ellos se puede establecer.</span><span class="sxs-lookup"><span data-stu-id="d2f54-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="d2f54-134">Sus definiciones se proporcionan sólo como orientación, y el proveedor es libre de implementar su propio significado específico de cada indicador.</span><span class="sxs-lookup"><span data-stu-id="d2f54-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="d2f54-135">El proveedor no debe devolver cualquier indicación de error si no tiene implementación de un indicador especificado.</span><span class="sxs-lookup"><span data-stu-id="d2f54-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="d2f54-136">El resultado de una restricción de contenido impuesta con respecto a una propiedad no está definido cuando la propiedad no existe.</span><span class="sxs-lookup"><span data-stu-id="d2f54-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="d2f54-137">Cuando un cliente requiere un comportamiento bien definido para esta restricción y no está seguro de si la propiedad existe por ejemplo, no es una columna de una tabla necesaria debe crear una restricción **y** para unirse a la restricción de contenido con una restricción existe.</span><span class="sxs-lookup"><span data-stu-id="d2f54-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="d2f54-138">Usar una estructura [SExistRestriction](sexistrestriction.md) para definir la restricción existe y una estructura [SAndRestriction](sandrestriction.md) para definir la restricción de **y** .</span><span class="sxs-lookup"><span data-stu-id="d2f54-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="d2f54-139">Para obtener más información sobre la estructura de **SContentRestriction** y restricciones en general, vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="d2f54-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2f54-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="d2f54-140">See also</span></span>

- [<span data-ttu-id="d2f54-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d2f54-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="d2f54-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="d2f54-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="d2f54-143">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d2f54-143">MAPI Structures</span></span>](mapi-structures.md)

