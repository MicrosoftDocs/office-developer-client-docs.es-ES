---
title: Sección del archivo de configuración de formulario [Propiedades]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f25d6b2db00f5629a9bf88499f9f4e080422ac29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585650"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="bacbc-103">Sección del archivo de configuración de formulario [Propiedades]</span><span class="sxs-lookup"><span data-stu-id="bacbc-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="bacbc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bacbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bacbc-105">La sección **[Propiedades]** enumera todo el conjunto de propiedades que utiliza el formulario y se publica; es decir, las propiedades que crea en sus mensajes personalizados que el cliente MAPI aplicaciones pueden utilizarla al mostrar columnas, tablas de contenido, configuración de carpetas de resultados de búsqueda, el filtrado y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="bacbc-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="bacbc-106">Cada entrada de esta lista (propiedad) hace referencia a una posterior **[propiedad.**</span><span class="sxs-lookup"><span data-stu-id="bacbc-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="bacbc-107">_cadena_ sección de **]** como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="bacbc-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="bacbc-108">**[Propiedades]**</span><span class="sxs-lookup"><span data-stu-id="bacbc-108">**[Properties]**</span></span>
  
 <span data-ttu-id="bacbc-109">**Propiedad.**</span><span class="sxs-lookup"><span data-stu-id="bacbc-109">**Property.**</span></span> <span data-ttu-id="bacbc-110">_cadena_ =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="bacbc-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="bacbc-111">El formato de una [ **(propiedad).**</span><span class="sxs-lookup"><span data-stu-id="bacbc-111">The format of a [ **Property.**</span></span> <span data-ttu-id="bacbc-112">_cadena_] sección es:</span><span class="sxs-lookup"><span data-stu-id="bacbc-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="bacbc-113">**[(Propiedad).**</span><span class="sxs-lookup"><span data-stu-id="bacbc-113">**[Property.**</span></span> <span data-ttu-id="bacbc-114">_cadena_ **]**</span><span class="sxs-lookup"><span data-stu-id="bacbc-114">_string_ **]**</span></span>
  
 <span data-ttu-id="bacbc-115">**Tipo de** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="bacbc-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="bacbc-116">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="bacbc-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="bacbc-117">**NmidString** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="bacbc-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="bacbc-118">**NmidInteger** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="bacbc-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="bacbc-119">**DisplayName** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="bacbc-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="bacbc-120">**Marcas de** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="bacbc-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="bacbc-121">**SpecialType** = 0 | 1</span><span class="sxs-lookup"><span data-stu-id="bacbc-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="bacbc-122">**Enum1** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="bacbc-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="bacbc-123">Cada **[propiedad.**</span><span class="sxs-lookup"><span data-stu-id="bacbc-123">Each **[Property.**</span></span> <span data-ttu-id="bacbc-124">_cadena_ **]** sección describe una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="bacbc-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="bacbc-125">El **tipo** de entrada especifica el tipo de propiedad MAPI, por ejemplo 3 (PT_I4), de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bacbc-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="bacbc-126">La entrada **NmidPropset** es opcional; junto con la entrada **NmidString** o en la entrada **NmidInteger** , la entrada de **NmidPropset** proporciona el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bacbc-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="bacbc-127">**NmidString** proporciona el nombre de la propiedad, mientras que **NmidInteger** permite el identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bacbc-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="bacbc-128">**NmidString** y **NmidInteger** son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="bacbc-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="bacbc-129">Si set, **NmidPropset** debe contener el nombre del conjunto de propiedades; Si está ausente, **NmidPropset** se establece en un valor predeterminado en función de la siguiente regla: si **NmidInteger** está presente y su valor es menor que 0 x 8000, **NmidPropset** se establece en PS_MAPI.</span><span class="sxs-lookup"><span data-stu-id="bacbc-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="bacbc-130">Si el valor de **NmidInteger** se establece en un número entero mayor que 0 x 8000, o si está presente, **NmidPropset** se establece en PS_PUBLIC_STRINGS.</span><span class="sxs-lookup"><span data-stu-id="bacbc-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="bacbc-131">La entrada **DisplayName** contiene la etiqueta de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bacbc-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="bacbc-132">La entrada **SpecialType** , si está presente y distinto de cero indica que esta propiedad es una propiedad especial.</span><span class="sxs-lookup"><span data-stu-id="bacbc-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="bacbc-133">En la actualidad, el tipo de propiedad especial sólo definido es **SpecialType** = 1, que indica las propiedades de la cadena enumerada.</span><span class="sxs-lookup"><span data-stu-id="bacbc-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="bacbc-134">Si **SpecialType** está establecida en 1, hace referencia la entrada de **Enum1** la **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="bacbc-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="bacbc-135">_cadena_ sección **]** .</span><span class="sxs-lookup"><span data-stu-id="bacbc-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="bacbc-136">A continuación se incluye un ejemplo de una sección **[Propiedades]** y un **[Propiedades.**</span><span class="sxs-lookup"><span data-stu-id="bacbc-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="bacbc-137">_cadena_ sección **]** .</span><span class="sxs-lookup"><span data-stu-id="bacbc-137">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="bacbc-138">La entrada **Enum1** en las referencias del ejemplo anterior a una posterior **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="bacbc-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="bacbc-139">_cadena_ sección **]** que describe una enumeración de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="bacbc-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="bacbc-140">Una de estas enumeraciones asocia la primera propiedad de la **[propiedad.**</span><span class="sxs-lookup"><span data-stu-id="bacbc-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="bacbc-141">_cadena_ sección de **]** con una propiedad de entero, denominado el índice.</span><span class="sxs-lookup"><span data-stu-id="bacbc-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="bacbc-142">Una de estas enumeraciones también contiene una lista de los valores posibles que puede asumir el par de índice de la presentación.</span><span class="sxs-lookup"><span data-stu-id="bacbc-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="bacbc-143">No es necesario especificar un tipo de propiedad para la enumeración porque según la definición de una entrada de **Enum1** siempre tiene el tipo de PT_I4.</span><span class="sxs-lookup"><span data-stu-id="bacbc-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="bacbc-144">El formato para el **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="bacbc-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="bacbc-145">_cadena_ sección **]** es:</span><span class="sxs-lookup"><span data-stu-id="bacbc-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="bacbc-146">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="bacbc-146">**[Enum1.**</span></span> <span data-ttu-id="bacbc-147">_cadena_ **]**</span><span class="sxs-lookup"><span data-stu-id="bacbc-147">_string_ **]**</span></span>
  
 <span data-ttu-id="bacbc-148">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="bacbc-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="bacbc-149">**NmidString** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="bacbc-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="bacbc-150">**NmidInteger** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="bacbc-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="bacbc-151">**EnumCount** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="bacbc-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="bacbc-152">**Val.**</span><span class="sxs-lookup"><span data-stu-id="bacbc-152">**Val.**</span></span> <span data-ttu-id="bacbc-153">_número entero_ **. Para mostrar** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="bacbc-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="bacbc-154">**Val.**</span><span class="sxs-lookup"><span data-stu-id="bacbc-154">**Val.**</span></span> <span data-ttu-id="bacbc-155">_número entero_ **. Índice** =  _entero_</span><span class="sxs-lookup"><span data-stu-id="bacbc-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="bacbc-156">La siguiente es una definición de propiedad de ejemplo para una propiedad enumerada denominada riesgo de incendio con valores posibles de baja, Media y alta.</span><span class="sxs-lookup"><span data-stu-id="bacbc-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
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

 <span data-ttu-id="bacbc-157">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="bacbc-157">**[Enum1.**</span></span> <span data-ttu-id="bacbc-158">_cadena_ se pueden usar en las secciones **]** por las aplicaciones para dos fines: para acelerar el filtrado de propiedades mediante el índice en lugar de la cadena y para ordenar por un orden diferente que el orden de los valores de cadena con caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="bacbc-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="bacbc-159">Por ejemplo, la ordenación puede realizarse en función de orden bajo, medio, alto en lugar de orden alto medio bajo.</span><span class="sxs-lookup"><span data-stu-id="bacbc-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

