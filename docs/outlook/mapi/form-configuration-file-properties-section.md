---
title: Sección Archivo de configuración de formulario [Propiedades]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 86d2257b821622094ff8d5ad3a5d7b1bfc74942b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421294"
---
# <a name="form-configuration-file-properties-section"></a>Sección Archivo de configuración de formulario [Propiedades]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La **sección [Propiedades]** enumera el conjunto completo de propiedades que el formulario usa y publica; es decir, las propiedades que crea en sus mensajes personalizados que las aplicaciones cliente MAPI pueden usar al mostrar columnas, filtrar tablas de contenido, configurar carpetas de resultados de búsqueda, y así sucesivamente. Cada entrada de esta lista de propiedades hace referencia a un **[Property posterior.** _string_ **]** como se muestra a continuación. 
  
 **[Propiedades]**
  
 **Propiedad.** _string_  =   _string_
  
Formato de una propiedad [ **.** _string_] la sección es: 
  
 **[Propiedad.** _string_ **]**
  
 **Tipo**  =   _integer_
  
 **NmidPropset**  =   _guid_
  
 **NmidString**  =   _string_
  
 **NmidInteger**  =   _integer_
  
 **DisplayName**  =   _string_
  
 **Flags**  =   _integer_
  
 **SpecialType** = 0|1 
  
 **Enum1**  =   _string_
  
Cada **[Propiedad.** _la_ **sección string ]** describe una sola propiedad. La **entrada** Type especifica el tipo de propiedad MAPI, por ejemplo 3 (PT_I4), de la propiedad. La **entrada NmidPropset** es opcional; junto con la **entrada NmidString** o la entrada **NmidInteger,** la entrada **NmidPropset** proporciona el nombre de la propiedad. **NmidString** proporciona el nombre de la propiedad, mientras **que NmidInteger** proporciona el identificador de la propiedad. **NmidString y** **NmidInteger** son mutuamente excluyentes. 
  
Si se establece, **NmidPropset** debe contener el nombre del conjunto de propiedades; si no está presente, **NmidPropset** se establece en un valor predeterminado basado en la siguiente regla: si **NmidInteger** está presente y su valor es menor que 0x8000, **NmidPropset** se establece en PS_MAPI. Si el valor de **NmidInteger** se establece en un entero mayor que 0x8000, o si está ausente, **NmidPropset** se establece en PS_PUBLIC_STRINGS. 
  
La **entrada DisplayName** contiene la etiqueta de la propiedad. La **entrada SpecialType,** si está presente y distinta de cero, indica que esta propiedad es una propiedad especial. Actualmente, el único tipo de propiedad especial definido es **SpecialType** = 1, que indica las propiedades enumeradas de cadena. Si **SpecialType** se establece en 1, la **entrada Enum1** hace referencia a **[Enum1.** _string_ **]** section. 
  
A continuación se muestra un ejemplo de **una sección [Propiedades]** y **una [Propiedades.** _string_ **]** section. 
  
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

La **entrada Enum1** del ejemplo de preceeding hace referencia a un **[Enum1 posterior.** _string_ **]** que describe una enumeración de un tipo determinado. Esta enumeración asocia la primera propiedad de **[Property.** _string_ **]** con una propiedad de entero, denominada índice. Esta enumeración también contiene una lista de los valores posibles que el par de índice de visualización puede suponer. No es necesario especificar un tipo de propiedad para la enumeración porque, por definición, una **entrada Enum1** siempre tiene el PT_I4 enumeración. Formato de **[Enum1.** _la_ **sección de cadena ]** es: 
  
 **[Enum1.** _string_ **]**
  
 **NmidPropset**  =   _guid_
  
 **NmidString**  =   _string_
  
 **NmidInteger**  =   _integer_
  
 **EnumCount**  =   _integer_
  
 **Val.** _entero_ **. Cadena de**  =   _visualización_
  
 **Val.** _entero_ **. Entero**  =   _de índice_
  
A continuación se muestra una definición de propiedad de ejemplo para una propiedad enumerada denominada Fire Hazard con posibles valores de Low, Medium y High.
  
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

 **[Enum1.** _las_ secciones de cadena **]** pueden ser usadas por las aplicaciones para dos propósitos: acelerar el filtrado de propiedades mediante el índice en lugar de la cadena y ordenar por un orden diferente al orden alfanumérico de los valores de cadena. Por ejemplo, la ordenación se puede realizar en función del orden Bajo-Medio-Alto en lugar del orden Alto-Medio-Bajo. 
  

