---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7cb77308ebc7229adcab290fc8e1f9e11ce45065
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587022"
---
# <a name="ixplogonopenstatusentry"></a>IXPLogon::OpenStatusEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se abre el objeto de estado del proveedor de transporte.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>Parámetros

 _lpInterface_
  
> [entrada] Un puntero a un identificador de interfaz (IID) para el objeto de inicio de sesión de transporte. Pasando NULL, devuelve la interfaz [IMAPIStatus](imapistatusimapiprop.md) . El parámetro _lpInterface_ también se puede establecer en un identificador para una interfaz para el objeto. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto de estado. Se puede establecer la marca siguiente:
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. La interfaz predeterminada es de sólo lectura. 
    
 _lpulObjType_
  
> [out] Un puntero al tipo del objeto abierto.
    
 _lppEntry_
  
> [out] Un puntero al puntero para el objeto de estado abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método de **IXPLogon::OpenStatusEntry** cuando una aplicación cliente llama a un método **OpenEntry** para el identificador de entrada de fila de tabla de estado del proveedor de transporte. **OpenStatusEntry** abre un objeto con la interfaz de **IMAPIStatus** asociada a este inicio de sesión del proveedor de transporte determinado. A continuación, se utiliza este objeto para habilitar las aplicaciones de cliente llamar a métodos **IMAPIStatus** (por ejemplo, para volver a configurar el inicio de sesión mediante el método [SettingsDialog](imapistatus-settingsdialog.md) , o para validar el estado de la sesión de inicio de sesión mediante el uso de la [ IMAPIStatus::ValidateState](imapistatus-validatestate.md) (método)). 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

