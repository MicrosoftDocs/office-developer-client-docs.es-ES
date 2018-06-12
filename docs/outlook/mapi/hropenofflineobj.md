---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: ac6584819b5dfa96a5f7816f1d77b89323e3eaf8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817086"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**Se aplica a**: Outlook 
  
Se abre un objeto sin conexión basada en un perfil determinado.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportada por:  <br/> |Msmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Se implementa mediante:  <br/> |Outlook  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a>Sintaxis

 _ulReserved_
  
> [entrada] Este parámetro no se usa. Debe ser 0.
    
 _pwszProfileNameIn_
  
> [entrada] El nombre del perfil que es el objeto sin conexión para. Se expresará en Unicode. 
    
 _pGUID_
  
> [entrada] Puntero a un GUID que se puede usar para identificar de forma única este objeto desde otros objetos sin conexión. Debe ser **GUID_GlobalState**.
    
 _Conserva_
  
> [entrada] Este parámetro no se usa. Debe ser **null**.
    
 _ppOfflineObj_
  
> [out] Un puntero al objeto solicitado sin conexión. El autor de la llamada puede usar este puntero para obtener acceso a la [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) interfaz para buscar las devoluciones de llamada que admite este objeto y para configurar las devoluciones de llamada para él. 
    
## <a name="return-values"></a>Valores devueltos

S_OK 
  
- La llamada a la función es correcta.
    
MAPI_E_NOT_FOUND
  
- Error en la llamada de función.
    
## <a name="remarks"></a>Notas

Se trata de la primera llamada realizada por un cliente cuando el cliente desea recibir una notificación de los cambios de estado de conexión para un perfil determinado. Tras llamar a **HrOpenOfflineObj**, el cliente obtiene un objeto sin conexión que admite **IMAPIOfflineMgr**. El cliente puede comprobar para los tipos de devoluciones de llamada admitidos por el objeto (mediante el uso de [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)) y, a continuación, configurar las devoluciones de llamada para él (mediante [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).
  
Cuando se usa [GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx) para buscar la dirección de esta función en msmapi32.dll, especifique **HrOpenOfflineObj@20** como el nombre del procedimiento. 
  
 **HrOpenOfflineObj** sólo funciona para los clientes que son proveedores MAPI, complementos COM y las extensiones de cliente de Exchange que se ejecuta dentro del proceso de Outlook. De lo contrario, **HrOpenOfflineObj** devuelve **MAPI_E_NOT_FOUND**. 
  
## <a name="see-also"></a>Ver también



[IMAPIOffline: IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md)


[Acerca de la API de estado sin conexión](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)

