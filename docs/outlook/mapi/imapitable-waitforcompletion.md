---
title: IMAPITableWaitForCompletion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407063"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Suspende el procesamiento hasta que se hayan completado una o varias operaciones asincrónicas en curso en la tabla.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> Reservado; debe ser cero.
    
 _ulTimeout_
  
> [entrada] Número máximo de milisegundos que hay que esperar a que se complete la operación asincrónica o las operaciones. Para esperar indefinidamente hasta que se produzca la finalización,  _establezca ulTimeout_ en 0xFFFFFFFF. 
    
 _lpulTableStatus_
  
> [entrada, salida] En la entrada, un puntero válido o NULL. En el resultado,  _si lpulTableStatus es_ un puntero válido, apunta al estado más reciente de la tabla. Si  _lpulTableStatus es_ NULL, no se devuelve información de estado. Si **WaitForCompletion devuelve** un valor HRESULT fallido, el contenido de  _lpulTableStatus_ no está definido. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de espera se ha realizado correctamente.
    
MAPI_E_NO_SUPPORT 
  
> La tabla no admite esperar a que se completen las operaciones asincrónicas.
    
MAPI_E_TIMEOUT 
  
> La operación asincrónica o las operaciones no se completaron en la hora especificada.
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::WaitForCompletion** suspende el procesamiento hasta que se completen las operaciones asincrónicas actualmente en curso para la tabla. **WaitForCompletion** puede permitir que las operaciones asincrónicas se completen completamente o se ejecuten durante un determinado número de milisegundos, como se indica en  _ulTimeout_, antes de ser interrumpidas. Para detectar operaciones asincrónicas en curso, llame al [método IMAPITable::GetStatus.](imapitable-getstatus.md) 
  
## <a name="see-also"></a>Consulte también



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

