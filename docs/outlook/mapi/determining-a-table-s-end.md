---
title: Determinar el final de una tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 28892e2d351b8dc9aa864c9eff52c94bb0f20e8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420090"
---
# <a name="determining-a-tables-end"></a>Determinar el final de una tabla

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 Un error común es suponer que se ha alcanzado el final de la tabla cuando: 
  
- Se ha llamado al método [IMAPITable:: QueryRows](imapitable-queryrows.md) en un bucle, con el final del bucle determinado por el recuento de filas devuelto por [IMAPITable:: GetRowCount](imapitable-getrowcount.md). El recuento que devuelve **GetRowCount** no siempre representa el número exacto de filas en la tabla; es un recuento aproximado. 
    
- Se ha llamado a **QueryRows** con un número fijo de filas y se devuelven menos filas. No es hasta que **QueryRows** devuelve un conjunto de filas con un recuento de filas igual a cero que no hay más filas que recuperar. 
    
> [!IMPORTANT]
> La única vez que una persona que llama puede suponer que el cursor está situado al final de la tabla para un recuento de filas positivo o al principio de la tabla para un recuento de filas negativo cuando se devuelven las filas de valor S_OK y cero. El valor MAPI_E_NOT_FOUND no se devuelve nunca. 
  
## <a name="see-also"></a>Ver también



[Tablas MAPI](mapi-tables.md)

