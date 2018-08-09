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
ms.openlocfilehash: 4b578f287a532475b53fb69cc4499662b6c4b6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817574"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**Hace referencia a**: Outlook 
  
Detiene cualquier operación asincrónica actualmente en curso para la tabla.
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Parámetros

Ninguno
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Uno o más de las operaciones asincrónicas se han detenido.
    
MAPI_E_UNABLE_TO_ABORT 
  
> Una operación asincrónica está en curso y no se puede detener o ya se ha completado.
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable::Abort** detiene cualquier operación asincrónica que está actualmente en curso. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para averiguar si una operación asincrónica está en curso, llame al método [IMAPITable::GetStatus](imapitable-getstatus.md) . 
  
Si los **botones Anular** , se detiene el procesamiento de una llamada al método [IMAPITable:: Restrict](imapitable-restrict.md) , el estado de la tabla será tal como estaba en el momento en que se procesa la llamada **Anular** . 
  
Si los **botones Anular** , se detiene el procesamiento de una llamada al método [SortTable](imapitable-sorttable.md) , criterio de ordenación de la tabla no se ve afectado y permanece tal como estaba antes de la llamada **SortTable** . 
  
## <a name="see-also"></a>Vea también



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

