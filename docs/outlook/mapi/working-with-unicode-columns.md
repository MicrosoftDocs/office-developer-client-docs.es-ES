---
title: Trabajar con columnas Unicode
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 76d1afb750dc81b889ca8e5eb3639145c061bfc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408386"
---
# <a name="working-with-unicode-columns"></a>Trabajar con columnas Unicode

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las cadenas de caracteres de las tablas se pueden representar con caracteres estándar de 8 bits, que son caracteres unicode de tipo de propiedad PT_STRING8 o unicode de 16 bits, que son tipos de propiedad PT_UNICODE. Los implementadores de tablas son libres de elegir si sus tablas admiten cadenas Unicode. Dado que Unicode agrega valor tanto a los clientes como a los proveedores de servicios mediante la extensión del conjunto de características, se recomienda admitir Unicode siempre que sea posible. 
  
Muchos métodos de tabla aceptan una marca que determina si se espera que los valores de propiedad de cadena sean Unicode. En la entrada, la especificación de la marca MAPI_UNICODE indica al implementador de tabla que todos los valores de propiedad de cadena pasados con la llamada son cadenas Unicode y tienen tipos de propiedad de PT_UNICODE. En el resultado, esta marca indica que todos los valores de propiedad de cadena devueltos deben ser cadenas Unicode, si es posible. Si la marca tiene un significado para entrada o salida depende del método. Los implementadores de tablas que no admiten Unicode y se pasan la marca MAPI_UNICODE devuelven el MAPI_E_BAD_CHAR_WIDTH valor.
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

