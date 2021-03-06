---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f50c0eb9e3af68e206eaa5bcc51cefa923c30f72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413181"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre un objeto status.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) para que se abra el objeto de estado. Si se pasa NULL, se devuelve la interfaz estándar del objeto (en este caso, la [interfaz IMAPIStatus).](imapistatusimapiprop.md) El  _parámetro lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el objeto. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abre el objeto de estado. Se puede establecer la siguiente marca:
    
MAPI_MODIFY 
  
> Solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se crean con permiso de solo lectura y las aplicaciones cliente no deben funcionar con la suposición de que se ha concedido permiso de lectura y escritura. 
    
 _lpulObjType_
  
> [salida] Puntero al tipo del objeto abierto.
    
 _lppEntry_
  
> [salida] Puntero al puntero al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores de almacén de mensajes implementan el método **IMSLogon::OpenStatusEntry** para abrir un objeto status. A continuación, este objeto status se usa para permitir que los clientes llamen a [métodos IMAPIStatus.](imapistatusimapiprop.md) Por ejemplo, los clientes pueden usar el método [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) para volver a configurar la sesión de inicio de sesión del almacén de mensajes o el método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) para validar el estado de la sesión de inicio de sesión del almacén de mensajes. 
  
## <a name="see-also"></a>Vea también



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

