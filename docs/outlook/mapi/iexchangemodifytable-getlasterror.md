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
ms.openlocfilehash: 8d5d4895e4440945896ee4f2212c5fca6da8610d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350865"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve información sobre el último error que se produjo en un objeto Table.
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a>Parameters

 _Valores_
  
> a Valor devuelto del método que produjo el error.
    
 _ulFlags_
  
> a No se usa, se establece en 0 (cero).
    
 _lppMAPIError_
  
> contempla Apunta a una estructura [MAPIERROR](mapierror.md) de MAPI que contiene información sobre el último error que se produjo en un objeto Table. 
    
## <a name="see-also"></a>Vea también



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

