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
ms.openlocfilehash: 7cbf11f16948d582ba36a0b4d20411549b723b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816664"
---
# <a name="determining-a-tables-end"></a>Determinar el final de una tabla

  
  
**Hace referencia a**: Outlook 
  
 Un error común es suponer que se ha alcanzado el final de la tabla cuando: 
  
- Se ha llamado al [IMAPITable:: QueryRows](imapitable-queryrows.md) en un bucle, con el final del bucle determinado por el recuento de filas devuelto por [IMAPITable::GetRowCount](imapitable-getrowcount.md). El número que devuelve **GetRowCount** no siempre representa el número exacto de filas de la tabla; es un recuento aproximado. 
    
- Se ha llamado al **QueryRows** con un número fijo de filas y se devuelven menos filas. Es no hasta que **QueryRows** devuelve un conjunto con un recuento de filas igual a cero que hay no hay más filas para recuperar de filas. 
    
> [!IMPORTANT]
> La única vez que un autor de la llamada puede asumir que se coloca el cursor al final de la tabla para un recuento de filas positivo o al principio de la tabla para un recuento de filas negativo es cuando se devuelven el valor S_OK y cero filas. El valor al nunca se devuelve. 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

