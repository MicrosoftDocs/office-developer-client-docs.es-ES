---
title: Sección del archivo de configuración de formulario [extensiones]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327303"
---
# <a name="form-configuration-file-extensions-section"></a>Sección del archivo de configuración de formulario [extensiones]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La sección **[extensions]** enumera los atributos extendidos del formulario, normalmente un conjunto de propiedades con nombre, que son todos los atributos que se encuentran fuera de los elementos básicos que aparecen en la sección **[Description]** del archivo de configuración del formulario. Los atributos extendidos son propiedades que devuelven las llamadas al método **GetProps** del objeto **IMAPIFormInfo** con el bit alto establecido en la etiqueta de propiedad. Las aplicaciones cliente pueden determinar los atributos extendidos de un formulario, si los hay, mediante la recuperación de estas etiquetas. Para ello, los clientes llaman al método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) , pasando los nombres de las propiedades del formulario y llaman al método [IMAPIProp:: GetProps](imapiprop-getprops.md) para obtener las propiedades. 
  
 **Prórroga**
  
 **Extensión.** _cadena1_ =  _cadena2_
  
Cada sección de propiedad de extensión define un atributo de extensión mediante la sintaxis de propiedad denominada MAPI. El tipo de propiedad debe ser PT_LONG o PT_STRING8. Los conjuntos de propiedades que contienen cadenas con nombre no son compatibles. El formato de la sección **[Extension]** es el siguiente: 
  
 **Extensión.** _cadena2_ **]**
  
 **Tipo** =  _entero_
  
 **** =  _GUID_ de NmidPropset
  
 **** =  _Entero_ NmidInteger
  
 **** =  __ |  _Entero_ de cadena de valor
  
A continuación se muestra un ejemplo de una sección **[extensions]** y una sección relacionada subsiguiente. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


