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
ms.openlocfilehash: a3343381709b7ce3370ba481ad8dbb935c7d4165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586952"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Suspende el procesamiento hasta que han completado una o varias operaciones asincrónicas en curso en la tabla.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> Reservado; debe ser cero.
    
 _ulTimeout_
  
> [entrada] Número máximo de milisegundos de espera para que las operaciones para llevar a cabo o la operación asincrónica. Para esperar indefinidamente hasta que se produce la finalización, establezca _ulTimeout_ en 0xFFFFFFFF. 
    
 _lpulTableStatus_
  
> [entrada, salida] En la entrada, un puntero válido o un valor NULL. En la salida, si _lpulTableStatus_ es un puntero válido, apunta al estado más reciente de la tabla. Si _lpulTableStatus_ es NULL, no se devuelve ninguna información de estado. Si **WaitForCompletion** devuelve un valor HRESULT realizado correctamente, el contenido de _lpulTableStatus_ es indefinido. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de espera fue correcta.
    
MAPI_E_NO_SUPPORT 
  
> La tabla no es compatible con la espera para la finalización de las operaciones asincrónicas.
    
MAPI_E_TIMEOUT 
  
> Las operaciones o una operación asincrónica no se completó en el tiempo especificado.
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable::WaitForCompletion** suspende el procesamiento hasta que han completado las operaciones asincrónicas actualmente en curso para la tabla. **WaitForCompletion** puede permitir que las operaciones asincrónicas a totalmente completa o para que se ejecute durante un determinado número de milisegundos, como se indica en _ulTimeout_, antes de que se interrumpa. Para detectar las operaciones asincrónicas en curso, llame al método [IMAPITable::GetStatus](imapitable-getstatus.md) . 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

