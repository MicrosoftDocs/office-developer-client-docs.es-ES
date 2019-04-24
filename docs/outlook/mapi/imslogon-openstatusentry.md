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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348702"
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
  
> a Un puntero al identificador de interfaz (IID) del objeto status que se va a abrir. Si se pasa NULL, se indica la interfaz estándar para el objeto que se devuelve (en este caso, la interfaz [IMAPIStatus](imapistatusimapiprop.md) ). El parámetro _lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el objeto. 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se abre el objeto status. Se puede establecer la siguiente marca:
    
MAPI_MODIFY 
  
> Solicita el permiso de lectura y escritura. De forma predeterminada, los objetos se crean con permiso de solo lectura y las aplicaciones cliente no deben funcionar por el supuesto de que se ha concedido el permiso de lectura y escritura. 
    
 _lpulObjType_
  
> contempla Un puntero al tipo del objeto abierto.
    
 _lppEntry_
  
> contempla Un puntero al puntero al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores de almacenamiento de mensajes implementan el método **IMSLogon:: OpenStatusEntry** para abrir un objeto de estado. A continuación, este objeto de estado se usa para permitir a los clientes llamar a métodos [IMAPIStatus](imapistatusimapiprop.md) . Por ejemplo, los clientes pueden usar el método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) para reconfigurar la sesión de inicio del almacén de mensajes o el método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) para validar el estado de la sesión de inicio del almacén de mensajes. 
  
## <a name="see-also"></a>Vea también



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

