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
ms.openlocfilehash: 72b4ab1fec10b2e91c7609af6644a54d29ed5e02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432124"
---
# <a name="imsgserviceadmincopymsgservice"></a>IMsgServiceAdmin::CopyMsgService

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _lpUID_
  
> [in] Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único del servicio de mensajes que se debe copiar. 
    
 _lpszDisplayName_
  
> [in] Este parámetro ha quedado en desuso. 
    
 _lpInterfaceToCopy_
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil del servicio de mensajes que se va a copiar. Si se pasa NULL, se usa la interfaz de sección de perfil [estándar, IProfSect.](iprofsectimapiprop.md)
    
 _lpInterfaceDst_
  
> [in] Puntero al IID que representa la interfaz que se usará para tener acceso al objeto al que apunta el _parámetro lpObjectDst._ Si se pasa NULL, se usa la interfaz de [sesión, IMAPISession.](imapisessioniunknown.md) El  _parámetro lpInterfaceDst_ también se puede establecer en IID_IMsgServiceAdmin. 
    
 _lpObjectDst_
  
> [in] Puntero a un puntero a un objeto de administración de servicio de mensajes o de sesión. El tipo de objeto debe corresponder al identificador de interfaz pasado  _en lpInterfaceDst_. Los punteros de objeto válidos son LPMAPISESSION y LPSERVICEADMIN.
    
 _ulUIParam_
  
> [in] Un identificador de la ventana principal de cualquier cuadro de diálogo o ventana que muestre este método.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se copia el servicio de mensajes. Se pueden establecer las siguientes marcas:
    
SERVICE_UI_ALWAYS 
  
> Solicita que el servicio de mensajes muestre siempre una hoja de propiedades de configuración.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El servicio de mensajes se copió correctamente.
    
MAPI_E_NO_ACCESS 
  
> El servicio de mensajes ya está en el perfil y no permite varias instancias de sí mismo.
    
MAPI_E_NOT_FOUND 
  
> El **MAPIUID al** que  _apunta lpUID_ no hace referencia a un servicio de mensajes existente. 
    
## <a name="remarks"></a>Comentarios

El **método IMsgServiceAdmin::CopyMsgService** copia un servicio de mensajes en un perfil, ya sea el perfil activo u otro perfil. El perfil que contiene el servicio de mensajes que se va a copiar y el destino no tiene que ser el mismo perfil, pero pueden serlo. 
  
No se llama a la función de punto de entrada del servicio de mensajes para una operación de copia. El servicio de mensajes copiado tiene las mismas opciones de configuración que su original. Para cambiar esta configuración, un cliente debe llamar al [método IMsgServiceAdmin::ConfigureMsgService.](imsgserviceadmin-configuremsgservice.md) 
  
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

