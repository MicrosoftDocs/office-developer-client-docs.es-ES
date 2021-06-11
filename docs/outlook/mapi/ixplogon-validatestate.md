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
ms.openlocfilehash: a3469e6baacb52938b870ca87d824bf640a8a88f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439488"
---
# <a name="ixplogonvalidatestate"></a>IXPLogon::ValidateState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Comprueba el estado externo del proveedor de transporte. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se realiza la comprobación de estado y los resultados de la comprobación de estado. Se pueden establecer las siguientes marcas:
    
ABORT_XP_HEADER_OPERATION 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo. El proveedor de transporte tiene la opción de continuar trabajando en la operación o puede anular la operación y devolver MAPI_E_USER_CANCELED. 
    
CONFIG_CHANGED 
  
> Valida el estado de los proveedores de transporte cargados actualmente haciendo que la cola MAPI llame a su [método IXPLogon::AddressTypes.](ixplogon-addresstypes.md) Esta marca también proporciona a la cola MAPI la oportunidad de corregir errores críticos del proveedor de transporte sin forzar a las aplicaciones cliente a cerrar sesión y, a continuación, volver a iniciar sesión. 
    
FORCE_XP_CONNECT 
  
> El usuario seleccionó una operación de conexión. Cuando esta marca se usa con la marca REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, la acción de conexión se produce sin almacenamiento en caché.
    
FORCE_XP_DISCONNECT 
  
> El usuario seleccionó una operación de desconexión. Cuando esta marca se usa con REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, la acción de desconexión se produce sin almacenamiento en caché.
    
PROCESS_XP_HEADER_CACHE 
  
> Se deben procesar las entradas de la tabla de caché de encabezado, descargar todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DOWNLOAD y eliminar todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DELETE. Los mensajes que tienen MSGSTATUS_REMOTE_DOWNLOAD y MSGSTATUS_REMOTE_DELETE deben moverse.
    
REFRESH_XP_HEADER_CACHE 
  
> Se debe descargar una nueva lista de encabezados de mensaje y se deben borrar todas las marcas de marcado de estado del mensaje.
    
SUPPRESS_UI 
  
> Impide que el proveedor de transporte muestre una interfaz de usuario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso; debe poder completarse o debe detenerse antes de intentar esta operación.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de transporte remoto implicado no admite una interfaz de usuario y la propia aplicación cliente debe mostrar el cuadro de diálogo.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPLogon::ValidateState** para admitir llamadas al método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) para el objeto status. El proveedor de transporte debe responder a la llamada **IXPLogon::ValidateState** exactamente como si la cola MAPI hubiera abierto un objeto de estado para la sesión de inicio de sesión actual y, a continuación, llamara **IMAPIStatus::ValidateState** en ese objeto. 
  
Para admitir su implementación de **IMAPIStatus::ValidateState**, la cola MAPI llama a **IXPLogon::ValidateState** en todos los objetos de inicio de sesión para todos los proveedores de transporte activo que se ejecutan en una sesión de perfil. 
  
## <a name="see-also"></a>Vea también



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

