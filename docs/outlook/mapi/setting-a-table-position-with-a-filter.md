---
title: Establecer una posición de tabla con un filtro
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316047"
---
# <a name="setting-a-table-position-with-a-filter"></a>Establecer una posición de tabla con un filtro

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Tabla los usuarios pueden mover el cursor a una fila que coincida con un conjunto de criterios de filtro. Los filtros se pueden basar en una amplia variedad de instrucciones, como valores de propiedades de columna, máscaras de la propiedad o subobjetos. Los filtros se especifican en MAPI con una estructura [SRestriction](srestriction.md) . 
  
 **Para colocar una tabla en la primera fila que coincida con los criterios establecidos en una restricción**
  
- Llame al método [IMAPITable:: FindRow](imapitable-findrow.md) . A partir de la fila representada por un marcador en particular, **FindRow** busca en una dirección hacia delante o hacia atrás para localizar una fila que coincida con los criterios especificados en la restricción. **FindRow** puede ser útil para implementar una barra de desplazamiento basada en cadenas de caracteres, en lugar de valores fraccionarios. Por ejemplo, un cliente puede llamar a la implementación de MAPI de **FindRow** cuando busca en la libreta de direcciones integrada para habilitar a un usuario, escribiendo uno o más caracteres, para encontrar el nombre que comienza con los caracteres especificados. 
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

