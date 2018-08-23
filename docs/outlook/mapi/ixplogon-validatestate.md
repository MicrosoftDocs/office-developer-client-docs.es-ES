---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4fd0dd02c5cf6f6a49b782d06c02e373dcfc3327
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577488"
---
# <a name="ixplogonvalidatestate"></a>IXPLogon::ValidateState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Comprobaciones de estado externo del proveedor de transporte. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se realiza la comprobación de estado y los resultados de la comprobación de estado. Se pueden establecer los siguientes indicadores:
    
ABORT_XP_HEADER_OPERATION 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. El proveedor de transporte tiene la opción para continuar trabajando en la operación, o se puede anular la operación y devolver MAPI_E_USER_CANCELED. 
    
CONFIG_CHANGED 
  
> Valida el estado de los proveedores de transporte actualmente cargados por lo que provoca que la cola MAPI llamar a su método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . Esta marca también proporciona una oportunidad para corregir errores críticos del proveedor de transporte sin necesidad de aplicaciones de cliente para cerrar sesión y, a continuación, vuelva a iniciar sesión de la cola de MAPI. 
    
FORCE_XP_CONNECT 
  
> El usuario ha seleccionado una operación de conexión. Cuando este indicador se utiliza con el indicador REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, se produce la acción de conexión sin almacenamiento en caché.
    
FORCE_XP_DISCONNECT 
  
> El usuario ha seleccionado una operación de desconexión. Cuando se utiliza esta marca con REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, se produce la acción de desconexión sin almacenamiento en caché.
    
PROCESS_XP_HEADER_CACHE 
  
> Se deben procesar las entradas de la tabla de la memoria caché de encabezado, que deben descargarse todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DOWNLOAD y se deben eliminar todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DELETE. Los mensajes que tienen MSGSTATUS_REMOTE_DOWNLOAD y MSGSTATUS_REMOTE_DELETE establecer se va a mover.
    
REFRESH_XP_HEADER_CACHE 
  
> Una nueva lista de encabezados de mensaje que debe descargarse y se debe borrar el estado del mensaje todos los indicadores de marcadores.
    
SUPPRESS_UI 
  
> Impide que el proveedor de transporte mostrar la interfaz de usuario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
MAPI_E_BUSY 
  
> Otra operación está en curso; se debe permitir para llevar a cabo o se debe detener antes de intenta esta operación.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de transporte remoto implicado no es compatible con una interfaz de usuario y la propia aplicación cliente debe mostrar el cuadro de diálogo.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama el método **IXPLogon::ValidateState** para admitir las llamadas al método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) para el objeto de estado. El proveedor de transporte debe responder a la llamada **IXPLogon::ValidateState** exactamente como si hubiera abierto un objeto de estado para la sesión actual de inicio de sesión y, a continuación, llame **IMAPIStatus::ValidateState** en ese objeto la cola MAPI. 
  
Para admitir su implementación de **IMAPIStatus::ValidateState**, la cola MAPI llama a **IXPLogon::ValidateState** en todos los objetos de inicio de sesión para todos los proveedores de transporte de activo que se ejecutan en una sesión de perfil. 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

