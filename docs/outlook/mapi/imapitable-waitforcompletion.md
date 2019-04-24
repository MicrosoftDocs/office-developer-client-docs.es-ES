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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328815"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Suspende el procesamiento hasta que se completen una o más operaciones asincrónicas en curso en la tabla.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> Reserve debe ser cero.
    
 _ulTimeout_
  
> a Número máximo de milisegundos que se debe esperar para que finalice la operación asincrónica o las operaciones. Para esperar indefinidamente hasta que se complete la finalización, establezca _ulTimeout_ en 0xFFFFFFFF. 
    
 _lpulTableStatus_
  
> [in, out] En la entrada, ya sea un puntero válido o NULL. En la salida, si _lpulTableStatus_ es un puntero válido, apunta al estado más reciente de la tabla. Si _lpulTableStatus_ es null, no se devuelve información de estado. Si **WaitForCompletion** devuelve un valor HRESULT incorrecto, no se define el contenido de _lpulTableStatus_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de espera se realizó correctamente.
    
MAPI_E_NO_SUPPORT 
  
> La tabla no admite la espera de la finalización de las operaciones asincrónicas.
    
MAPI_E_TIMEOUT 
  
> La operación asincrónica o las operaciones no se completaron en el tiempo especificado.
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: WaitForCompletion** suspende el procesamiento hasta que se hayan completado todas las operaciones asincrónicas actualmente en modo de la tabla. **WaitForCompletion** puede permitir que las operaciones asincrónicas se completen o se ejecuten durante un número determinado de milisegundos, como se indica en _ulTimeout_, antes de que se interrumpa. Para detectar las operaciones asincrónicas en curso, llame al método [IMAPITable:: getStatus](imapitable-getstatus.md) . 
  
## <a name="see-also"></a>Vea también



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

