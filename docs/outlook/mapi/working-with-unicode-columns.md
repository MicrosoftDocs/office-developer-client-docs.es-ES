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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325574"
---
# <a name="working-with-unicode-columns"></a>Trabajar con columnas Unicode

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las cadenas de caracteres de las tablas pueden representarse mediante caracteres estándar de 8 bits, que son tipos de propiedades PT_STRING8 o caracteres Unicode de 16 bits, que son tipos de propiedades PT_UNICODE. Los implementadores de tablas pueden elegir libremente si sus tablas admiten cadenas Unicode. Como Unicode agrega un valor a los clientes y a los proveedores de servicios mediante la extensión del conjunto de características, es recomendable admitir Unicode siempre que sea posible. 
  
Muchos métodos de tabla aceptan una marca que indica si se espera que los valores de las propiedades de cadena sean Unicode. En la entrada, al especificar la marca MAPI_UNICODE se indica al implementador de tabla que todos los valores de propiedad de cadena que se pasan con la llamada son cadenas Unicode y tienen tipos de propiedad de PT_UNICODE. En la salida, este indicador indica que todos los valores de propiedad de cadena devueltos deben ser cadenas Unicode, si es posible. Si la marca tiene un significado para la entrada o la salida depende del método. Los implementadores de la tabla que no admiten Unicode y a los que se pasa la marca MAPI_UNICODE devuelven el valor de MAPI_E_BAD_CHAR_WIDTH.
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

