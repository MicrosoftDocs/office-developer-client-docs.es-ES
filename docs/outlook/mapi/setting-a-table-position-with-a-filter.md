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
ms.openlocfilehash: 6c4db9c67fc712143657fe66b86ea33ef2b9c272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565595"
---
# <a name="setting-a-table-position-with-a-filter"></a>Establecer una posición de tabla con un filtro

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los usuarios de la tabla pueden mover el cursor a una fila que coincide con un conjunto de criterios de filtro. Los filtros se pueden basar en una gran variedad de instrucciones, como los valores de propiedad de columna, máscaras de bits o subobjetos. Los filtros se especifican en MAPI mediante una estructura de [SRestriction](srestriction.md) . 
  
 **Para colocar una tabla a la primera fila que coincide con los criterios establecidos en una restricción**
  
- Llame al método [IMAPITable:: FindRow](imapitable-findrow.md) . A partir de la fila representada por un marcador determinado, **FindRow** busca en una dirección hacia delante o hacia atrás para localizar una fila que coincide con los criterios especificados en la restricción. **FindRow** puede ser útil para implementar una barra de desplazamiento que se basa en las cadenas de caracteres, en lugar de valores fraccionarias. Por ejemplo, un cliente puede llamar a implementación de MAPI de **FindRow** cuando se realicen búsquedas a través de la libreta de direcciones integrada para permitir que un usuario, escribiendo uno o más caracteres, para buscar el nombre que comienza con los caracteres especificados. 
    
## <a name="see-also"></a>Recursos adicionales



[Tablas MAPI](mapi-tables.md)

