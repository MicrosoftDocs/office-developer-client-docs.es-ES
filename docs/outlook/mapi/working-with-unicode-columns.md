---
title: Trabajar con columnas de Unicode
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 9f1fd2d4e4bfdc9ccbbb771fedf1141769c8c8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820975"
---
# <a name="working-with-unicode-columns"></a>Trabajar con columnas de Unicode

  
  
**Se aplica a**: Outlook 
  
Las cadenas de caracteres en las tablas se pueden representar mediante caracteres de 8 bits estándar, que son el tipo de propiedad PT_STRING8, o caracteres Unicode de 16 bits, que son propiedad de tipo PT_UNICODE. Los implementadores de tabla son libres de elegir si sus tablas admiten cadenas Unicode. Como Unicode agrega valor para los clientes y proveedores de servicios de ampliando el conjunto de características, se recomienda la compatibilidad con Unicode siempre que sea posible. 
  
Muchos métodos de tabla aceptan una marca que determina si los valores de propiedad de cadena se prevé que Unicode. En la entrada, si se especifica el indicador MAPI_UNICODE indica para el implementador de tabla que todos los valores de propiedad de cadena pasados con la llamada son cadenas Unicode y tienen tipos de propiedad de PT_UNICODE. En la salida, esta marca indica que todos los valores de propiedad de la cadena devuelta deben ser cadenas Unicode, si es posible. Si el marcador no tiene un significado para la entrada o salida depende del método. Los implementadores de tabla que no admiten Unicode y se pasan el indicador MAPI_UNICODE devolver el valor MAPI_E_BAD_CHAR_WIDTH.
  
## <a name="see-also"></a>Ver también



[Tablas MAPI](mapi-tables.md)

