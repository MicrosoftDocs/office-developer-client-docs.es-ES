---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f0d2ad118346dd06788af972b64b10d6f6f6d0fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594295"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve información sobre el último error que se produjo en un objeto table.
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a>Parámetros

 _hResult_
  
> [entrada] El valor devuelto por el método fallidas.
    
 _ulFlags_
  
> [entrada] No se usa, se establece en 0 (cero).
    
 _lppMAPIError_
  
> [out] Apunta a una estructura MAPI [MAPIERROR](mapierror.md) que contiene información sobre el último error que se ha producido para un objeto table. 
    
## <a name="see-also"></a>Recursos adicionales



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

