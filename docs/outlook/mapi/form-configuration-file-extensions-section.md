---
title: Sección del archivo de configuración de formulario [Extensiones]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 459c5f5a34421583141028cd9accad5e242d31ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573561"
---
# <a name="form-configuration-file-extensions-section"></a>Sección del archivo de configuración de formulario [Extensiones]

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La sección **[Extensions]** enumera los atributos extendidos del formulario, normalmente un conjunto de propiedades con nombre, que son los atributos más allá de los básicos que aparecen en la sección **[descripción]** del archivo de configuración de formulario. Atributos extendidos no son propiedades devueltas de las llamadas al método **GetProps** del objeto **IMAPIFormInfo** con el bit alto establecido en la etiqueta de propiedad. Las aplicaciones cliente pueden determinar los atributos extendidos de un formulario, si hay alguno, mediante la recuperación de estas etiquetas. Para ello, los clientes de llamar al método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , pasando en los nombres de las propiedades del formulario y llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener las propiedades. 
  
 **[Extensions]**
  
 **Extensión.** _cadena1_ =  _cadena2_
  
Cada sección de la propiedad de extensión define un atributo de extensión mediante la con el nombre de sintaxis de la propiedad MAPI. El tipo de propiedad debe ser PT_LONG o PT_STRING8. No se admiten los conjuntos de propiedades que contiene las cadenas con nombre. El formato de la sección **[extensión]** es: 
  
 **[Extensión.** _cadena2_ **]**
  
 **Tipo de** =  _entero_
  
 **NmidPropset** =  _guid_
  
 **NmidInteger** =  _entero_
  
 **Valor** =  _cadena_ |  _entero_
  
Se muestra un ejemplo de una sección **[Extensions]** y una sección posterior relacionada siguientes. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


