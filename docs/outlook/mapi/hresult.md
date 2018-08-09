---
title: HRESULT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5bacf3c73ba7f9a7720586c77ee520d289c40e11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817036"
---
# <a name="hresult"></a>HRESULT

  
  
**Hace referencia a**: Outlook 
  
Un valor de 32 bits que se usa para describir un error o advertencia.
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>Comentarios

El tipo de datos **HRESULT** es el mismo que el tipo de datos [SCODE](scode.md) . 
  
Devuelve un valor **HRESULT** consta de los siguientes campos: 
  
- Un código de 1 bit que indica la gravedad, donde cero representa éxito y 1 representa el error.
    
- Un valor de 4 bits reservado.
    
- Un código de 11 bits que indica la responsabilidad del error o advertencia, también conocido como un código de servicio.
    
- Un código que describe el error o advertencia de 16 bits.
    
La mayoría de los métodos de interfaz MAPI y funciones devuelven valores **HRESULT** para proporcionar formación causa detallada. Los valores **HRESULT** también se usan ampliamente en los métodos de interfaz OLE. OLE proporciona varias macros para convertir entre valores **HRESULT** y **SCODE** valores, escriba otros datos comunes para el tratamiento de errores. 
  
> [!NOTE]
> En MAPI de 64 bits, **HRESULT** sigue siendo un valor de 32 bits. 
  
Para obtener información sobre el uso OLE de los valores **HRESULT** , vea la *referencia del programador de OLE* . Para obtener más información sobre el uso de estos valores en MAPI, vea [Tratamiento de errores](error-handling-in-mapi.md) y cualquiera de los métodos de interfaz siguientes: 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>Vea también



[SCODE](scode.md)


[Tipos de datos MAPI](mapi-data-types.md)

