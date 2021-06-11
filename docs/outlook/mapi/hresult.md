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
ms.openlocfilehash: 64fcbebbd71bc3f478f36c711e49db9a3518ef9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435022"
---
# <a name="hresult"></a>HRESULT

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valor de 32 bits que se usa para describir un error o advertencia.
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>Comentarios

El **tipo de datos HRESULT** es el mismo que el tipo de datos [SCODE.](scode.md) 
  
Un **valor HRESULT** consta de los campos siguientes: 
  
- Un código de 1 bit que indica la gravedad, donde cero representa el éxito y 1 representa el error.
    
- Un valor reservado de 4 bits.
    
- Un código de 11 bits que indica la responsabilidad del error o advertencia, también conocido como código de instalación.
    
- Un código de 16 bits que describe el error o advertencia.
    
La mayoría de los métodos y funciones de interfaz MAPI **devuelven valores HRESULT** para proporcionar una formación detallada de la causa. **Los valores HRESULT** también se usan ampliamente en los métodos de interfaz OLE. OLE proporciona varias macros para convertir entre **valores HRESULT** y **valores SCODE,** otro tipo de datos común para el control de errores. 
  
> [!NOTE]
> En MAPI de 64 bits, **HRESULT** sigue siendo un valor de 32 bits. 
  
Para obtener información sobre el uso OLE de **valores HRESULT,** vea  *referencia del programador OLE*  . Para obtener más información sobre el uso de estos valores en MAPI, vea Control de [errores](error-handling-in-mapi.md) y cualquiera de los siguientes métodos de interfaz: 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>Vea también



[SCODE](scode.md)


[Tipos de datos MAPI](mapi-data-types.md)

