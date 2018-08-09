---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d9a15abc05bf0f0a6fef35dd489f12925b88014a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817745"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**Hace referencia a**: Outlook 
  
Copia un servicio de mensajes en un perfil. 
  
```cpp
HRESULT CopyMsgService(
  LPMAPIUID lpUID,
  LPSTR lpszDisplayName,
  LPCIID lpInterfaceToCopy,
  LPCIID lpInterfaceDst,
  LPVOID lpObjectDst,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpUID_
  
> [entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único del servicio de mensajes para copiar. 
    
 _lpszDisplayName_
  
> [entrada] Este parámetro ha quedado obsoleto. 
    
 _lpInterfaceToCopy_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil de servicio de mensajes para copiar. Si se pasa NULL da como resultado la interfaz de sección del perfil estándar, [IProfSect](iprofsectimapiprop.md), que se usa.
    
 _lpInterfaceDst_
  
> [entrada] Un puntero a la IID que representa la interfaz que se usará para tener acceso al objeto al que apunta el parámetro _lpObjectDst_ . Si se pasa NULL da como resultado la interfaz de sesión [IMAPISession](imapisessioniunknown.md), que se utiliza. También se puede establecer el parámetro _lpInterfaceDst_ en IID_IMsgServiceAdmin. 
    
 _lpObjectDst_
  
> [entrada] Un puntero a un puntero a un objeto de administración de servicio de sesión o un mensaje. El tipo de objeto debe coincidir con el identificador de interfaz que se pasó _lpInterfaceDst_. Punteros a objetos válidos son LPMAPISESSION y LPSERVICEADMIN.
    
 _ulUIParam_
  
> [entrada] Un identificador de la ventana principal de windows o cuadros de diálogo que muestra este método.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se copia el servicio de mensajes. Se pueden establecer los siguientes indicadores:
    
SERVICE_UI_ALWAYS 
  
> Solicitudes que el servicio de mensajes siempre mostrar una hoja de propiedades de configuración.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El servicio de mensajes se ha copiado correctamente.
    
MAPI_E_NO_ACCESS 
  
> El servicio de mensajes ya está en el perfil y no admite varias instancias de sí mismo.
    
MAPI_E_NOT_FOUND 
  
> El **MAPIUID** que señala _lpUID_ no hace referencia a un servicio de mensaje existente. 
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin::CopyMsgService** copia un servicio de mensajes en un perfil, el perfil activo u otro perfil. El perfil que contiene el servicio de mensajes que se va a copiar y el destino no tienen que ser el mismo perfil, pero pueden ser. 
  
Función de punto de entrada del servicio de mensajes no se llama para una operación de copia. El servicio de mensajes copiados tiene la misma configuración que su original. Para cambiar esta configuración, un cliente debe llamar al método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

