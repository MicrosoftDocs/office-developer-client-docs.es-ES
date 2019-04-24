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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328960"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Detiene todas las operaciones asincrónicas que se encuentran en curso para la tabla.
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Parámetros

Ninguno
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se han detenido una o más operaciones asincrónicas.
    
MAPI_E_UNABLE_TO_ABORT 
  
> Una operación asincrónica está en curso y no se puede detener o ya se ha completado.
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: ABORT** detiene cualquier operación asincrónica que esté actualmente en curso. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para averiguar si una operación asincrónica está en curso, llame al método [IMAPITable:: getStatus](imapitable-getstatus.md) . 
  
Si **Abort** detiene el procesamiento de una llamada al método [IMAPITable:: Restrict](imapitable-restrict.md) , el estado de la tabla será el que se encontraba en el momento en que se procesa la llamada a **Abort** . 
  
Si **Abort** detiene el procesamiento de una llamada al método [IMAPITable:: SortTable](imapitable-sorttable.md) , el criterio de ordenación de la tabla no se ve afectado y permanece como era antes de la llamada a **SortTable** . 
  
## <a name="see-also"></a>Vea también



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

