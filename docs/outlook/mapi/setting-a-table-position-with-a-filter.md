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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425473"
---
# <a name="setting-a-table-position-with-a-filter"></a>Establecer una posición de tabla con un filtro

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los usuarios de tabla pueden mover el cursor a una fila que coincida con un conjunto de criterios de filtro. Los filtros pueden basarse en una variedad de directrices, como valores de propiedad de columna, máscaras de bits o subobjetos. Los filtros se especifican en MAPI mediante una [estructura SRestriction.](srestriction.md) 
  
 **Para colocar una tabla en la primera fila que coincida con los criterios establecidos en una restricción**
  
- Llame al [método IMAPITable::FindRow.](imapitable-findrow.md) A partir de la fila representada por un marcador determinado, **FindRow** busca en una dirección hacia delante o hacia atrás para buscar una fila que coincida con los criterios especificados en la restricción. **FindRow** puede ser útil para implementar una barra de desplazamiento basada en cadenas de caracteres, en lugar de valores fraccionados. Por ejemplo, un cliente puede llamar a la implementación de **FindRow** de MAPI al buscar en la libreta de direcciones integrada para permitir que un usuario, al escribir uno o varios caracteres, busque el primer nombre que comienza con los caracteres especificados. 
    
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

