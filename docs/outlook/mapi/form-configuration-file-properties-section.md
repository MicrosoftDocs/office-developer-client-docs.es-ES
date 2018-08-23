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
# <a name="form-configuration-file-properties-section"></a>Sección del archivo de configuración de formulario [Propiedades]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La sección **[Propiedades]** enumera todo el conjunto de propiedades que utiliza el formulario y se publica; es decir, las propiedades que crea en sus mensajes personalizados que el cliente MAPI aplicaciones pueden utilizarla al mostrar columnas, tablas de contenido, configuración de carpetas de resultados de búsqueda, el filtrado y así sucesivamente. Cada entrada de esta lista (propiedad) hace referencia a una posterior **[propiedad.** _cadena_ sección de **]** como se muestra a continuación. 
  
 **[Propiedades]**
  
 **Propiedad.** _cadena_ =  _cadena_
  
El formato de una [ **(propiedad).** _cadena_] sección es: 
  
 **[(Propiedad).** _cadena_ **]**
  
 **Tipo de** =  _entero_
  
 **NmidPropset** =  _guid_
  
 **NmidString** =  _cadena_
  
 **NmidInteger** =  _entero_
  
 **DisplayName** =  _cadena_
  
 **Marcas de** =  _entero_
  
 **SpecialType** = 0 | 1 
  
 **Enum1** =  _cadena_
  
Cada **[propiedad.** _cadena_ **]** sección describe una sola propiedad. El **tipo** de entrada especifica el tipo de propiedad MAPI, por ejemplo 3 (PT_I4), de la propiedad. La entrada **NmidPropset** es opcional; junto con la entrada **NmidString** o en la entrada **NmidInteger** , la entrada de **NmidPropset** proporciona el nombre de la propiedad. **NmidString** proporciona el nombre de la propiedad, mientras que **NmidInteger** permite el identificador de la propiedad. **NmidString** y **NmidInteger** son mutuamente excluyentes. 
  
Si set, **NmidPropset** debe contener el nombre del conjunto de propiedades; Si está ausente, **NmidPropset** se establece en un valor predeterminado en función de la siguiente regla: si **NmidInteger** está presente y su valor es menor que 0 x 8000, **NmidPropset** se establece en PS_MAPI. Si el valor de **NmidInteger** se establece en un número entero mayor que 0 x 8000, o si está presente, **NmidPropset** se establece en PS_PUBLIC_STRINGS. 
  
La entrada **DisplayName** contiene la etiqueta de la propiedad. La entrada **SpecialType** , si está presente y distinto de cero indica que esta propiedad es una propiedad especial. En la actualidad, el tipo de propiedad especial sólo definido es **SpecialType** = 1, que indica las propiedades de la cadena enumerada. Si **SpecialType** está establecida en 1, hace referencia la entrada de **Enum1** la **[Enum1.** _cadena_ sección **]** . 
  
A continuación se incluye un ejemplo de una sección **[Propiedades]** y un **[Propiedades.** _cadena_ sección **]** . 
  
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

La entrada **Enum1** en las referencias del ejemplo anterior a una posterior **[Enum1.** _cadena_ sección **]** que describe una enumeración de un tipo determinado. Una de estas enumeraciones asocia la primera propiedad de la **[propiedad.** _cadena_ sección de **]** con una propiedad de entero, denominado el índice. Una de estas enumeraciones también contiene una lista de los valores posibles que puede asumir el par de índice de la presentación. No es necesario especificar un tipo de propiedad para la enumeración porque según la definición de una entrada de **Enum1** siempre tiene el tipo de PT_I4. El formato para el **[Enum1.** _cadena_ sección **]** es: 
  
 **[Enum1.** _cadena_ **]**
  
 **NmidPropset** =  _guid_
  
 **NmidString** =  _cadena_
  
 **NmidInteger** =  _entero_
  
 **EnumCount** =  _entero_
  
 **Val.** _número entero_ **. Para mostrar** =  _cadena_
  
 **Val.** _número entero_ **. Índice** =  _entero_
  
La siguiente es una definición de propiedad de ejemplo para una propiedad enumerada denominada riesgo de incendio con valores posibles de baja, Media y alta.
  
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

 **[Enum1.** _cadena_ se pueden usar en las secciones **]** por las aplicaciones para dos fines: para acelerar el filtrado de propiedades mediante el índice en lugar de la cadena y para ordenar por un orden diferente que el orden de los valores de cadena con caracteres alfanuméricos. Por ejemplo, la ordenación puede realizarse en función de orden bajo, medio, alto en lugar de orden alto medio bajo. 
  

