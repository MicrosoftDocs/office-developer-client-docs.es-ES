---
title: IMAPISessionSetDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f4ff2a3897306ebe4f77c08630782c5f2c7d5d3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335808"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece un almacén de mensajes como el almacén de mensajes predeterminado para la sesión.
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla la configuración del almacén de mensajes predeterminado. Estas marcas se excluyen mutuamente; solo se puede establecer uno de los siguientes indicadores:
    
MAPI_DEFAULT_STORE
  
> Establece el almacén de mensajes como el valor predeterminado de la sesión. Actualiza la fila de la tabla de estado del almacén de mensajes estableciendo la marca STATUS_DEFAULT_STORE en la columna **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
MAPI_PRIMARY_STORE
  
> Establece el almacén de mensajes como el almacén que se va a usar al iniciar sesión. Si el almacén de mensajes no es el almacén predeterminado, los clientes deben convertirlo en el predeterminado. Actualiza la fila de la tabla de estado del almacén de mensajes estableciendo la marca STATUS_PRIMARY_STORE en la columna **PR_RESOURCE_FLAGS** . 
    
MAPI_SECONDARY_STORE
  
> Establece el almacén de mensajes como el almacén que se va a usar en el inicio de sesión si el almacén de mensajes principal no está disponible. Si un cliente no puede abrir el almacén principal, debe abrir el almacén secundario y establecerlo como predeterminado. Actualiza la fila de la tabla de estado del almacén de mensajes estableciendo la marca STATUS_SECONDARY_STORE en la columna **PR_RESOURCE_FLAGS** . 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Establece la marca STATUS_SIMPLE_STORE en la propiedad **PR_RESOURCE_FLAGS** del almacén de mensajes en la fila de la tabla de estado, en la fila de la tabla del almacén de mensajes y en el perfil de sesión. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Establece la marca STATUS_SIMPLE_STORE en la propiedad **PR_RESOURCE_FLAGS** del almacén de mensajes en la fila de la tabla de estado y la fila de la tabla del almacén de mensajes. El perfil no se modifica. 
    
 _cbEntryID_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada del almacén de mensajes que está pensado como predeterminado. Si un cliente pasa NULL en _lpEntryID_, no hay ningún almacén de mensajes seleccionado como predeterminado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession:: SetDefaultStore** establece un almacén de mensajes como uno de los siguientes: 
  
- El almacén de mensajes predeterminado para la sesión.
    
- El almacén de mensajes principal para la sesión.
    
- El almacén de mensajes secundario para la sesión.
    
Para establecer un almacén de mensajes como predeterminado, el almacén de mensajes debe tener los siguientes marcadores establecidos en su propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)):
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede determinar el almacén de mensajes predeterminado para la sesión recuperando la tabla de estado y buscando la configuración de la marca STATUS_DEFAULT_STORE en la columna **PR_RESOURCE_FLAGS** . La fila que tiene esta configuración representa el almacén de mensajes designado como valor predeterminado de la sesión. 
  
Cuando se establece la marca MAPI_DEFAULT_STORE o MAPI_SIMPLE_STORE_PERMANENT, MAPI actualiza el perfil, la tabla del almacén de mensajes y la tabla de estado. 
  
Siempre que se realiza un cambio en la configuración predeterminada del almacén de mensajes, se generan las siguientes notificaciones:
  
- Se emite una notificación de evento **fnevTableModified** para cada fila afectada tanto en la tabla de estado como en el almacén de mensajes. 
    
- Se emite una notificación interna a la cola MAPI. Las operaciones que ya están en curso se completan sin cambios; las nuevas operaciones que implican el almacén de mensajes predeterminado, como la descarga de mensajes, se procesan para el nuevo almacén predeterminado.
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnSetDefaultStore  <br/> |MFCMAPI usa el método **IMAPISession:: SetDefaultStore** para establecer el almacén seleccionado como almacén predeterminado.  <br/> |
   
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagResourceFlags](pidtagresourceflags-canonical-property.md)
  
[Propiedad canónica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

