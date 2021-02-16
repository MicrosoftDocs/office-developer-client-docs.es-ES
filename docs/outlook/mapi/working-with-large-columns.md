---
title: Trabajar con columnas grandes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9ca3c5e7a0d1b4a6ac09dcfcc7db10ec76ecb224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420426"
---
# <a name="working-with-large-columns"></a>Trabajar con columnas grandes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las columnas con datos de propiedad binaria o de cadena pueden ser grandes, posiblemente muchos miles de bytes de longitud. Dado que incluir una o más columnas con cientos de bytes en una vista suele ser poco práctico, MAPI permite a los implementadores de tablas truncar el valor, con más frecuencia a 255 bytes y menos a 510 bytes. Siempre que sea posible, los implementadores de tablas deben incluir el valor completo de una propiedad en una columna de tabla. La alternativa recomendada es incluir solo los primeros 255 bytes.
  
Los clientes no pueden saber de antemano si una tabla que usan trunca columnas grandes. Deben suponer que una columna representa una propiedad truncada si la longitud de la columna es de 255 o 510 bytes. Si es necesario, los clientes pueden recuperar directamente el valor completo de una columna truncada del objeto llamando al método [IMAPIProp::GetProps del](imapiprop-getprops.md) objeto. 
  
Los clientes que construyen restricciones con propiedades de gran tamaño deben tener en cuenta que es el implementador de tabla el que debe saber cómo funcionan estas restricciones. Algunos implementadores de tablas permiten que las restricciones creadas con una columna truncada se basen en el tamaño truncado, mientras que otros la basan en el valor completo. 
  
## <a name="see-also"></a>Consulte también



[Tablas MAPI](mapi-tables.md)

