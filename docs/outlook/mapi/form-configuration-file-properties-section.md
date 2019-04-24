---
title: Sección del archivo de configuración de formulario [propiedades]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 86d2257b821622094ff8d5ad3a5d7b1bfc74942b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328108"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="47ff2-103">Sección del archivo de configuración de formulario [propiedades]</span><span class="sxs-lookup"><span data-stu-id="47ff2-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="47ff2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47ff2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47ff2-105">La sección **[Properties]** muestra el conjunto completo de propiedades que el formulario usa y publica; es decir, las propiedades que crea en sus mensajes personalizados que pueden usar las aplicaciones de cliente MAPI para mostrar columnas, filtrar tablas de contenido, configurar carpetas de resultados de búsqueda, etc.</span><span class="sxs-lookup"><span data-stu-id="47ff2-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="47ff2-106">Cada entrada de esta lista de propiedades hace referencia a una **[propiedad subsiguiente.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="47ff2-107">_cadena_ de **]** tal como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="47ff2-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="47ff2-108"><b0></A1></b0></span><span class="sxs-lookup"><span data-stu-id="47ff2-108">**[Properties]**</span></span>
  
 <span data-ttu-id="47ff2-109">**Inspector.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-109">**Property.**</span></span> <span data-ttu-id="47ff2-110">__ cadena de cadena__  =  </span><span class="sxs-lookup"><span data-stu-id="47ff2-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="47ff2-111">El formato de una [ **Property.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-111">The format of a [ **Property.**</span></span> <span data-ttu-id="47ff2-112">_String_] la sección es:</span><span class="sxs-lookup"><span data-stu-id="47ff2-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="47ff2-113">**Inspector.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-113">**[Property.**</span></span> <span data-ttu-id="47ff2-114">_cadena_ de **]**</span><span class="sxs-lookup"><span data-stu-id="47ff2-114">_string_ **]**</span></span>
  
 <span data-ttu-id="47ff2-115">**Tipo** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="47ff2-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="47ff2-116">\*\*\*\* =  _GUID_ de NmidPropset</span><span class="sxs-lookup"><span data-stu-id="47ff2-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="47ff2-117">\*\*\*\* =  _Cadena_ NmidString</span><span class="sxs-lookup"><span data-stu-id="47ff2-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="47ff2-118">\*\*\*\* =  _Entero_ NmidInteger</span><span class="sxs-lookup"><span data-stu-id="47ff2-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="47ff2-119">\*\*\*\* =  _Cadena_ DisplayName</span><span class="sxs-lookup"><span data-stu-id="47ff2-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="47ff2-120">**Indicadores** =  _enteros_</span><span class="sxs-lookup"><span data-stu-id="47ff2-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="47ff2-121">**SpecialType** = 0 | 1</span><span class="sxs-lookup"><span data-stu-id="47ff2-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="47ff2-122">\*\*\*\* =  _Cadena_ Enum1</span><span class="sxs-lookup"><span data-stu-id="47ff2-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="47ff2-123">Cada **[Property.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-123">Each **[Property.**</span></span> <span data-ttu-id="47ff2-124">_cadena_ de **]** describe una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="47ff2-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="47ff2-125">La entrada **Type** especifica el tipo de propiedad MAPI, por ejemplo, 3 (PT_I4), de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="47ff2-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="47ff2-126">La entrada **NmidPropset** es opcional; junto con la entrada **NmidString** o la entrada **NmidInteger** , la entrada **NmidPropset** da el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="47ff2-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="47ff2-127">**NmidString** proporciona el nombre de la propiedad, mientras que **NmidInteger** proporciona el identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="47ff2-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="47ff2-128">**NmidString** y **NmidInteger** se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="47ff2-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="47ff2-129">Si se establece, **NmidPropset** debe contener el nombre del conjunto de propiedades; Si no está presente, **NmidPropset** se establece en un valor predeterminado según la siguiente regla: Si **NmidInteger** está presente y su valor es menor que 0x8000, **NmidPropset** se establece en PS_MAPI.</span><span class="sxs-lookup"><span data-stu-id="47ff2-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="47ff2-130">Si el valor de **NmidInteger** se establece en un entero mayor que 0x8000 o no está presente, **NmidPropset** se establece en PS_PUBLIC_STRINGS.</span><span class="sxs-lookup"><span data-stu-id="47ff2-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="47ff2-131">La entrada **displayName** contiene la etiqueta de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="47ff2-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="47ff2-132">La entrada **SpecialType** indica que esta propiedad es una propiedad especial, si está presente y no es cero.</span><span class="sxs-lookup"><span data-stu-id="47ff2-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="47ff2-133">Actualmente, el único tipo de propiedad especial definido es **SpecialType** = 1, que indica las propiedades enumeradas de cadena.</span><span class="sxs-lookup"><span data-stu-id="47ff2-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="47ff2-134">Si **SpecialType** se establece en 1, la entrada **Enum1** hace referencia a **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="47ff2-135">_cadena_ de **]** sección.</span><span class="sxs-lookup"><span data-stu-id="47ff2-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="47ff2-136">A continuación se encuentra un ejemplo de una sección **[Properties]** y a **[Properties.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="47ff2-137">_cadena_ de **]** sección.</span><span class="sxs-lookup"><span data-stu-id="47ff2-137">_string_ **]** section.</span></span> 
  
```cpp
[Properties]
Property.1 = Fire Hazard
Property.2 = Safe
[Property.Fire Hazard]
Type = 1
NmidPropSet = {E47F4480-8400-101B-934D-04021C007002]
NmidString = FireHazard
DisplayName = Fire Hazard
SpecialType = 1
Enum1 = HazardEnum

```

<span data-ttu-id="47ff2-138">La entrada **Enum1** en el ejemplo anterior hace referencia a un **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="47ff2-139">_cadena_ de **]** que describe una enumeración de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="47ff2-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="47ff2-140">Esta enumeración asocia la primera propiedad de **[Property.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="47ff2-141">_cadena_ de **]** con una propiedad de entero, llamada índice.</span><span class="sxs-lookup"><span data-stu-id="47ff2-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="47ff2-142">Esta enumeración también contiene una lista de los valores posibles que puede asumir el par display-index.</span><span class="sxs-lookup"><span data-stu-id="47ff2-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="47ff2-143">La especificación de un tipo de propiedad para la enumeración no es necesaria porque, por definición, una entrada **Enum1** siempre tiene el tipo PT_I4.</span><span class="sxs-lookup"><span data-stu-id="47ff2-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="47ff2-144">El formato del **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="47ff2-145">_cadena_ de **]** es:</span><span class="sxs-lookup"><span data-stu-id="47ff2-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="47ff2-146">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-146">**[Enum1.**</span></span> <span data-ttu-id="47ff2-147">_cadena_ de **]**</span><span class="sxs-lookup"><span data-stu-id="47ff2-147">_string_ **]**</span></span>
  
 <span data-ttu-id="47ff2-148">\*\*\*\* =  _GUID_ de NmidPropset</span><span class="sxs-lookup"><span data-stu-id="47ff2-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="47ff2-149">\*\*\*\* =  _Cadena_ NmidString</span><span class="sxs-lookup"><span data-stu-id="47ff2-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="47ff2-150">\*\*\*\* =  _Entero_ NmidInteger</span><span class="sxs-lookup"><span data-stu-id="47ff2-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="47ff2-151">\*\*\*\* =  _Entero_ EnumCount</span><span class="sxs-lookup"><span data-stu-id="47ff2-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="47ff2-152">**Val.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-152">**Val.**</span></span> <span data-ttu-id="47ff2-153">_número entero_ \*\*. \*\* =  _Cadena_ para mostrar</span><span class="sxs-lookup"><span data-stu-id="47ff2-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="47ff2-154">**Val.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-154">**Val.**</span></span> <span data-ttu-id="47ff2-155">_número entero_ \*\*. \*\* =  _Entero_ de índice</span><span class="sxs-lookup"><span data-stu-id="47ff2-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="47ff2-156">A continuación se muestra un ejemplo de definición de propiedad para una propiedad enumerada denominada peligro de incendio con los valores posibles de bajo, medio y alto.</span><span class="sxs-lookup"><span data-stu-id="47ff2-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
```cpp
[Properties]
Property1 = Fire Hazard
[Enum1.HazardEnum]
IdxNmidPropset={E47F4480-8400-101B-934D-04021C007002]
IdxNmidString=FireHazardEnum
EnumCount = 3
Val.1.Display = Low
Val.1.Index = 1
Val.2.Display = Medium
Val.2.Index = 2
Val.3.Display = High
Val.3.Index = 3

```

 <span data-ttu-id="47ff2-157">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="47ff2-157">**[Enum1.**</span></span> <span data-ttu-id="47ff2-158">_cadena_ de **]** las aplicaciones pueden usarlas para dos propósitos: acelerar el filtrado de propiedades mediante el índice en lugar de la cadena y ordenar por un orden diferente al orden alfanumérico de los valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="47ff2-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="47ff2-159">Por ejemplo, la ordenación se podría realizar basándose en el orden bajo-medio-alto en lugar del orden alto-medio-bajo.</span><span class="sxs-lookup"><span data-stu-id="47ff2-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

