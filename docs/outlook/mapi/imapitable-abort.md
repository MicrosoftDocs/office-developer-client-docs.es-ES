---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 74c307fca27f1adec18d236792f8a58d97e33ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406153"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Detiene las operaciones asincrónicas actualmente en curso para la tabla.
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Parámetros

Ninguno
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se han detenido una o varias operaciones asincrónicas.
    
MAPI_E_UNABLE_TO_ABORT 
  
> Una operación asincrónica está en curso y no se puede detener o ya se ha completado.
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::Abort** detiene cualquier operación asincrónica que esté en curso. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para averiguar si hay una operación asincrónica en curso, llame al [método IMAPITable::GetStatus.](imapitable-getstatus.md) 
  
Si **Abort** detiene el procesamiento de una llamada al método [IMAPITable::Restrict,](imapitable-restrict.md) el estado de  la tabla será el mismo que en el momento en que se procese la llamada de anulación. 
  
Si **Abort** detiene el procesamiento de una llamada al método [IMAPITable::SortTable,](imapitable-sorttable.md) el criterio de ordenación de la tabla no se verán afectados y permanecerá igual que antes de la llamada **a SortTable.** 
  
## <a name="see-also"></a>Consulte también



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

