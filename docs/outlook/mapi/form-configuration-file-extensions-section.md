---
title: Sección Archivo de configuración de formulario [Extensiones]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423758"
---
# <a name="form-configuration-file-extensions-section"></a>Sección Archivo de configuración de formulario [Extensiones]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La **sección [Extensiones]** enumera los atributos extendidos del formulario, normalmente un conjunto de propiedades con nombre, que son atributos que van más allá de los básicos enumerados en la sección **[Descripción]** del archivo de configuración del formulario. Los atributos extendidos son propiedades devueltas de llamadas al método **GetProps** del objeto **IMAPIFormInfo** con el bit alto establecido en la etiqueta de propiedad. Las aplicaciones cliente pueden determinar los atributos extendidos de un formulario, si los hay, recuperando estas etiquetas. Para ello, los clientes llaman al método [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md) pasando los nombres de las propiedades del formulario y llaman al método [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener las propiedades. 
  
 **[Extensiones]**
  
 **Extensión.** _string1_  =   _string2_
  
Cada sección de propiedad de extensión define un atributo de extensión mediante la sintaxis de propiedad con nombre MAPI. El tipo de propiedad debe ser PT_LONG o PT_STRING8. No se admiten los conjuntos de propiedades que contienen cadenas con nombre. El formato de la **sección [Extensión]** es: 
  
 **[Extensión.** _string2_ **]**
  
 **Tipo**  =   _integer_
  
 **NmidPropset**  =   _guid_
  
 **NmidInteger**  =   _integer_
  
 **Valor**  =   _string_  |   _integer_
  
A continuación se muestra un ejemplo de una sección **[Extensions]** y una sección relacionada posterior. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


