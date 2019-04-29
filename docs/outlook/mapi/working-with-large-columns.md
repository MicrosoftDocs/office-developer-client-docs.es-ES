---
title: Trabajar con columnas de gran tamaño
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
# <a name="working-with-large-columns"></a>Trabajar con columnas de gran tamaño

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las columnas con datos de String o Binary Property pueden ser grandes, posiblemente miles de bytes de longitud. Debido a que la inclusión de una o más columnas con cientos de bytes en una vista es a menudo inviable, MAPI permite que los implementadores de tablas trunquen el valor, con mayor frecuencia a 255 bytes y menos frecuencia a 510 bytes. Siempre que sea posible, los implementadores de tablas deben incluir el valor completo de una propiedad en una columna de tabla. La alternativa recomendada es incluir solo los primeros 255 bytes.
  
Los clientes no pueden saber de antemano si una tabla que usan trunca columnas de gran tamaño. Deben dar por hecho que una columna representa una propiedad truncada si la longitud de la columna es de 255 o de 510 bytes. Si es necesario, los clientes pueden recuperar directamente el valor completo de una columna truncada del objeto llamando al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del objeto. 
  
Los clientes que crean restricciones con propiedades grandes deben tener en cuenta que es el que implementa la tabla en cuanto al funcionamiento de estas restricciones. Algunos implementadores de tablas permiten restricciones que se generan con una columna truncada para basarse en el tamaño truncado mientras que otros basan en el valor completo. 
  
## <a name="see-also"></a>Ver también



[Tablas MAPI](mapi-tables.md)

