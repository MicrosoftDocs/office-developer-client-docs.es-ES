---
title: Devolver Convención de nomenclatura de valor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279828"
---
# <a name="return-value-naming-convention"></a>Devolver Convención de nomenclatura de valor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPICODE. H contiene muchos de los valores que un cliente o proveedor de servicios puede devolver desde una implementación de método de interfaz o puede que vea devuelto desde una llamada.
  
Los códigos que representan las condiciones de advertencia y error siguen una Convención de nomenclatura diferente que comienza con el prefijo MAPI, un guión bajo y una W o una E para indicar el tipo de código. El resto del código es una cadena de caracteres corta para describir la condición. Cada palabra de la cadena está separada por un carácter de subrayado. Por ejemplo, el valor de error MAPI_E_TOO_COMPLEX indica que la implementación no pudo controlar lo que se solicitó en la llamada. El valor de advertencia MAPI_W_PARTIAL_COMPLETION indica que la llamada se ha realizado correctamente, pero que se han producido problemas. Solo parte de la operación se completó correctamente.
  

