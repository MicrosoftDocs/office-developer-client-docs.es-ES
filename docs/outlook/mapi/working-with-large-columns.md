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
ms.openlocfilehash: a191a8551d425d7e8b3b9a281936a4a0e2dfd587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820974"
---
# <a name="working-with-large-columns"></a>Trabajar con columnas de gran tamaño

  
  
**Hace referencia a**: Outlook 
  
Columnas con datos de propiedad de cadena o binario pueden ser grandes, posiblemente varios miles de bytes de longitud. Debido a que a menudo es práctico incluir una o varias columnas con cientos de bytes en una vista, MAPI permite a los implementadores de tabla truncar el valor, con más frecuencia a 255 bytes y con menos frecuencia a 510 bytes. Siempre que sea posible, los implementadores de tabla deben incluir el valor completo de una propiedad en una columna de tabla. La alternativa recomendada es incluir sólo los primeros 255 bytes.
  
Los clientes no se pueden saber de antemano si una tabla que utilicen trunca columnas de gran tamaño. Debe asumir que una columna representa una propiedad truncada si la longitud de la columna es de 255 o 510 bytes. Si es necesario, los clientes pueden recuperar directamente el valor completo de una columna truncada desde el objeto llamando al método del objeto [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
Creación de restricciones con propiedades de gran tamaño de los clientes deben tener en cuenta que es responsabilidad del implementador de tabla sobre cómo estas restricciones operar. Algunos implementadores tabla permiten las restricciones que se crean con una columna truncada a ser según el tamaño truncado mientras que otros usuarios basar en el valor completo. 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

