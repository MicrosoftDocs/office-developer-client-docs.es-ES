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
ms.openlocfilehash: d9e09de1064a0ae034bb3618f0e5b3719a82c163
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435904"
---
# <a name="ixplogonopenstatusentry"></a>IXPLogon::OpenStatusEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre el objeto de estado del proveedor de transporte.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in] Puntero a un identificador de interfaz (IID) para el objeto de inicio de sesión de transporte. Si se pasa NULL, se [devuelve la interfaz IMAPIStatus.](imapistatusimapiprop.md) El  _parámetro lpInterface_ también se puede establecer en un identificador de una interfaz para el objeto. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abre el objeto de estado. Se puede establecer la siguiente marca:
    
MAPI_MODIFY 
  
> Solicitudes de permiso de lectura y escritura. La interfaz predeterminada es de solo lectura. 
    
 _lpulObjType_
  
> [salida] Puntero al tipo del objeto abierto.
    
 _lppEntry_
  
> [salida] Puntero al puntero al objeto de estado abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPLogon::OpenStatusEntry** cuando una aplicación cliente llama a un método **OpenEntry** para el identificador de entrada en la fila de tabla de estado del proveedor de transporte. **OpenStatusEntry** abre un objeto con la interfaz **IMAPIStatus** asociada a este inicio de sesión del proveedor de transporte en particular. A continuación, este objeto se usa para permitir que las aplicaciones cliente llamen a métodos **IMAPIStatus** (por ejemplo, para volver a configurar la sesión de inicio de sesión mediante el método [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) o para validar el estado de la sesión de inicio de sesión mediante el método [IMAPIStatus::ValidateState).](imapistatus-validatestate.md) 
  
## <a name="see-also"></a>Vea también



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

