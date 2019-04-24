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
# <a name="form-configuration-file-properties-section"></a>Sección del archivo de configuración de formulario [propiedades]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La sección **[Properties]** muestra el conjunto completo de propiedades que el formulario usa y publica; es decir, las propiedades que crea en sus mensajes personalizados que pueden usar las aplicaciones de cliente MAPI para mostrar columnas, filtrar tablas de contenido, configurar carpetas de resultados de búsqueda, etc. Cada entrada de esta lista de propiedades hace referencia a una **[propiedad subsiguiente.** _cadena_ de **]** tal como se muestra a continuación. 
  
 <b0></A1></b0>
  
 **Inspector.** __ cadena de cadena__  =  
  
El formato de una [ **Property.** _String_] la sección es: 
  
 **Inspector.** _cadena_ de **]**
  
 **Tipo** =  _entero_
  
 **** =  _GUID_ de NmidPropset
  
 **** =  _Cadena_ NmidString
  
 **** =  _Entero_ NmidInteger
  
 **** =  _Cadena_ DisplayName
  
 **Indicadores** =  _enteros_
  
 **SpecialType** = 0 | 1 
  
 **** =  _Cadena_ Enum1
  
Cada **[Property.** _cadena_ de **]** describe una sola propiedad. La entrada **Type** especifica el tipo de propiedad MAPI, por ejemplo, 3 (PT_I4), de la propiedad. La entrada **NmidPropset** es opcional; junto con la entrada **NmidString** o la entrada **NmidInteger** , la entrada **NmidPropset** da el nombre de la propiedad. **NmidString** proporciona el nombre de la propiedad, mientras que **NmidInteger** proporciona el identificador de la propiedad. **NmidString** y **NmidInteger** se excluyen mutuamente. 
  
Si se establece, **NmidPropset** debe contener el nombre del conjunto de propiedades; Si no está presente, **NmidPropset** se establece en un valor predeterminado según la siguiente regla: Si **NmidInteger** está presente y su valor es menor que 0x8000, **NmidPropset** se establece en PS_MAPI. Si el valor de **NmidInteger** se establece en un entero mayor que 0x8000 o no está presente, **NmidPropset** se establece en PS_PUBLIC_STRINGS. 
  
La entrada **displayName** contiene la etiqueta de la propiedad. La entrada **SpecialType** indica que esta propiedad es una propiedad especial, si está presente y no es cero. Actualmente, el único tipo de propiedad especial definido es **SpecialType** = 1, que indica las propiedades enumeradas de cadena. Si **SpecialType** se establece en 1, la entrada **Enum1** hace referencia a **[Enum1.** _cadena_ de **]** sección. 
  
A continuación se encuentra un ejemplo de una sección **[Properties]** y a **[Properties.** _cadena_ de **]** sección. 
  
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

La entrada **Enum1** en el ejemplo anterior hace referencia a un **[Enum1.** _cadena_ de **]** que describe una enumeración de un tipo determinado. Esta enumeración asocia la primera propiedad de **[Property.** _cadena_ de **]** con una propiedad de entero, llamada índice. Esta enumeración también contiene una lista de los valores posibles que puede asumir el par display-index. La especificación de un tipo de propiedad para la enumeración no es necesaria porque, por definición, una entrada **Enum1** siempre tiene el tipo PT_I4. El formato del **[Enum1.** _cadena_ de **]** es: 
  
 **[Enum1.** _cadena_ de **]**
  
 **** =  _GUID_ de NmidPropset
  
 **** =  _Cadena_ NmidString
  
 **** =  _Entero_ NmidInteger
  
 **** =  _Entero_ EnumCount
  
 **Val.** _número entero_ **. ** =  _Cadena_ para mostrar
  
 **Val.** _número entero_ **. ** =  _Entero_ de índice
  
A continuación se muestra un ejemplo de definición de propiedad para una propiedad enumerada denominada peligro de incendio con los valores posibles de bajo, medio y alto.
  
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

 **[Enum1.** _cadena_ de **]** las aplicaciones pueden usarlas para dos propósitos: acelerar el filtrado de propiedades mediante el índice en lugar de la cadena y ordenar por un orden diferente al orden alfanumérico de los valores de cadena. Por ejemplo, la ordenación se podría realizar basándose en el orden bajo-medio-alto en lugar del orden alto-medio-bajo. 
  

