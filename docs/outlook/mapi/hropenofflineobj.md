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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347750"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre un objeto sin conexión basado en un perfil determinado.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|ExPortado por:  <br/> |MSMAPI32. dll  <br/> |
|Llamado por:  <br/> |Client  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a>Parameters

 _ulReserved_
  
> a Este parámetro no se usa. Debe ser 0.
    
 _pwszProfileNameIn_
  
> a Nombre del perfil para el que se encuentra el objeto sin conexión. Debe expresarse en Unicode. 
    
 _pGUID_
  
> a Puntero a un GUID que se puede usar para identificar de forma única este objeto de otros objetos sin conexión. Debe ser **GUID_GlobalState**.
    
 _Preserva_
  
> a Este parámetro no se usa. Debe ser **null**.
    
 _ppOfflineObj_
  
> contempla Un puntero al objeto solicitado sin conexión. El autor de la llamada puede usar este puntero para obtener acceso a la interfaz [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) para buscar las devoluciones de llamada que admite este objeto y configurar las devoluciones de llamada para él. 
    
## <a name="return-values"></a>Valores devueltos

S_OK 
  
- La llamada a la función es correcta.
    
MAPI_E_NOT_FOUND
  
- Error en la llamada a la función.
    
## <a name="remarks"></a>Comentarios

Esta es la primera llamada que un cliente realiza cuando el cliente desea recibir una notificación de los cambios en el estado de conexión de un perfil determinado. Al llamar a **HrOpenOfflineObj**, el cliente obtiene un objeto sin conexión que admite **IMAPIOfflineMgr**. El cliente puede comprobar los tipos de devoluciones de llamada admitidas por el objeto (mediante [IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)) y, a continuación, configurar las devoluciones de llamada para él (mediante [IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)).
  
Al utilizar [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) para buscar la dirección de esta función en MSMAPI32. dll, especifique **HrOpenOfflineObj @ 20** como nombre del procedimiento. 
  
 **HrOpenOfflineObj** solo funciona para clientes que son proveedores MAPI, Complementos com y extensiones de cliente de Exchange que se ejecutan dentro del proceso de Outlook. De lo contrario, **HrOpenOfflineObj** devuelve **MAPI_E_NOT_FOUND**. 
  
## <a name="see-also"></a>Vea también



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Información sobre la API de estado sin conexión](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)

