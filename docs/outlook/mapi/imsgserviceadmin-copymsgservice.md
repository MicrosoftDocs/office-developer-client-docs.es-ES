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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309971"
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
  
> a Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único del servicio de mensajes que se va a copiar. 
    
 _lpszDisplayName_
  
> a Este parámetro ha quedado obsoleto. 
    
 _lpInterfaceToCopy_
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la sección de perfil del servicio de mensajes que se va a copiar. Pasar resultados NULL en la interfaz de sección de perfil estándar, [IProfSect](iprofsectimapiprop.md), que se usa.
    
 _lpInterfaceDst_
  
> a Puntero al IID que representa la interfaz que se va a usar para obtener acceso al objeto al que apunta el parámetro _lpObjectDst_ . Pasar resultados NULL en la interfaz de sesión, [IMAPISession](imapisessioniunknown.md), que se usa. El parámetro _lpInterfaceDst_ también se puede establecer en IID_IMsgServiceAdmin. 
    
 _lpObjectDst_
  
> a Un puntero a un puntero a un objeto de administración de sesión o de servicio de mensajes. El tipo de objeto debe coincidir con el identificador de interfaz pasado en _lpInterfaceDst_. Los punteros de objeto válidos son LPMAPISESSION y LPSERVICEADMIN.
    
 _ulUIParam_
  
> a Un controlador para la ventana primaria de los cuadros de diálogo o ventanas que este método muestra.
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla cómo se copia el servicio de mensajes. Se pueden establecer los siguientes indicadores:
    
SERVICE_UI_ALWAYS 
  
> Solicita que el servicio de mensajes muestre siempre una hoja de propiedades de configuración.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El servicio de mensajes se copió correctamente.
    
MAPI_E_NO_ACCESS 
  
> El servicio de mensajes ya está en el perfil y no permite varias instancias de sí mismo.
    
MAPI_E_NOT_FOUND 
  
> La **MAPIUID** a la que apunta _lpUID_ no hace referencia a un servicio de mensajes existente. 
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin:: CopyMsgService** copia un servicio de mensajes en un perfil, ya sea el perfil activo u otro perfil. El perfil que contiene el servicio de mensajes que se va a copiar y el destino no tienen que ser el mismo perfil, pero pueden ser. 
  
No se llama a la función de punto de entrada del servicio de mensajes para una operación de copia. El servicio de mensajes copiado tiene las mismas opciones de configuración que su original. Para cambiar esta configuración, un cliente debe llamar al método [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

