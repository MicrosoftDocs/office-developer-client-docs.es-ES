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
ms.openlocfilehash: a48d8248878c64de827bb09030073e6becba3024
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571202"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre un objeto de estado.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a>Parámetros

 _lpInterface_
  
> [entrada] Un puntero para el identificador de interfaz (IID) para el objeto de estado abrir. Paso de NULL indica que se devuelve la interfaz estándar para el objeto (en este caso, la interfaz [IMAPIStatus](imapistatusimapiprop.md) ). El parámetro _lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el objeto. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto de estado. Se puede establecer la marca siguiente:
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se crean con permiso de sólo lectura, y las aplicaciones cliente no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. 
    
 _lpulObjType_
  
> [out] Un puntero al tipo del objeto abierto.
    
 _lppEntry_
  
> [out] Un puntero al puntero para el objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores de almacén de mensajes implementan el método **IMSLogon::OpenStatusEntry** para abrir un objeto de estado. A continuación, se utiliza este objeto de estado para que los clientes puedan llamar a los métodos [IMAPIStatus](imapistatusimapiprop.md) . Por ejemplo, los clientes pueden utilizar el método [SettingsDialog](imapistatus-settingsdialog.md) para volver a configurar la sesión de inicio de sesión del almacén de mensaje o el método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) para validar el estado de la sesión de inicio de sesión del almacén de mensajes. 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

