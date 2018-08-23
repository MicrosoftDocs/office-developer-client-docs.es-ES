---
title: Devolver convención de nomenclatura de valor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4d7a95e4681370e1aaf4f8b4c4b7ca0814b3aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581849"
---
# <a name="return-value-naming-convention"></a>Devolver convención de nomenclatura de valor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El MAPICODE. Archivo de encabezado de H contiene muchos de los valores que un proveedor de cliente o servicio podría devolver desde una implementación de método de interfaz o es posible que vea devuelto desde una llamada.
  
Los códigos que representan las condiciones de error y advertencia siguen una convención de nomenclatura diferente que comienza con el prefijo de MAPI, un carácter de subrayado y una W o una E para indicar el tipo de código. El resto del código es una cadena corta de caracteres para describir la condición. Cada palabra en la cadena viene separada por un carácter de subrayado. Por ejemplo, el valor de error MAPI_E_TOO_COMPLEX indica que la implementación no pudo controlar lo que se solicitó en la llamada. El valor de advertencia MAPI_W_PARTIAL_COMPLETION indica que la llamada se ha realizado correctamente, pero que se han producido problemas. Sólo una parte de la operación se completó correctamente.
  

