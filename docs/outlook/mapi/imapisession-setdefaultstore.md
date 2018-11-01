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
ms.openlocfilehash: c7eda7089515942cb38a941bab863b3adf971bdc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587848"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Establece un almacén de mensajes como el almacén de mensajes predeterminado para la sesión.
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la configuración del almacén de mensajes predeterminado. Estas marcas son mutuamente excluyentes; se puede establecer solo uno de los siguientes indicadores:
    
MAPI_DEFAULT_STORE
  
> Establece el almacén de mensajes como el valor predeterminado de la sesión. Actualiza la fila de tabla de estado del almacén de mensajes estableciendo el indicador STATUS_DEFAULT_STORE en la columna **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
MAPI_PRIMARY_STORE
  
> Establece el almacén de mensajes como el almacén que se usará en el inicio de sesión. Si el almacén de mensajes no es el almacén de forma predeterminada, los clientes hacen que el valor predeterminado. Actualiza la fila de tabla de estado del almacén de mensajes estableciendo el indicador STATUS_PRIMARY_STORE en la columna **PR_RESOURCE_FLAGS** . 
    
MAPI_SECONDARY_STORE
  
> Establece el almacén de mensajes como el almacén que se usará en el inicio de sesión si el almacén de mensajes principal no está disponible. Si un cliente no puede abrir el almacén principal, debe abrir el almacén de secundario y establecer como predeterminado. Actualiza la fila de tabla de estado del almacén de mensajes estableciendo el indicador STATUS_SECONDARY_STORE en la columna **PR_RESOURCE_FLAGS** . 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Establece la marca STATUS_SIMPLE_STORE en propiedad **PR_RESOURCE_FLAGS** del almacén de mensajes en su fila de tabla de estado, fila de la tabla de almacenamiento de mensajes y en el perfil de sesión. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Establece la marca STATUS_SIMPLE_STORE en propiedad **PR_RESOURCE_FLAGS** del almacén de mensajes en su fila de la tabla de estado y la fila de tabla del almacén de mensajes. No se modificó el perfil. 
    
 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada del almacén de mensajes que se ha diseñado como el valor predeterminado. Si un cliente pasa NULL en _lpEntryID_, no se selecciona ningún almacén de mensajes como el valor predeterminado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession::SetDefaultStore** establece un almacén de mensajes como una de las siguientes opciones: 
  
- El almacén de mensajes predeterminado para la sesión.
    
- El almacén de mensajes principal para la sesión.
    
- El almacén de mensajes secundario para la sesión.
    
Para establecer un almacén de mensajes como el valor predeterminado, el almacén de mensajes debe tener las siguientes marcas establecer en su propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)):
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede determinar el almacén de mensajes predeterminado para la sesión al recuperar la tabla de estado y busca el valor de la marca STATUS_DEFAULT_STORE en la columna **PR_RESOURCE_FLAGS** . La fila que tiene esta opción representa el almacén de mensajes que se designa como el valor predeterminado de la sesión. 
  
Cuando se establece la MAPI_DEFAULT_STORE o la marca MAPI_SIMPLE_STORE_PERMANENT, MAPI actualiza el perfil, tabla de almacén de mensajes y tabla de estado. 
  
Cada vez que se realiza un cambio a la configuración predeterminada de almacén de mensajes, se generan las notificaciones siguientes:
  
- Se emite una notificación de evento **fnevTableModified** para cada fila afectada en ambas en la tabla de almacenamiento y el estado de mensaje. 
    
- Se emite una notificación interna a la cola MAPI. Operaciones en curso se completan sin cambio; nuevas operaciones relacionadas con el almacén de mensajes de forma predeterminada, como una descarga el mensaje, se procesan para el nuevo almacén predeterminado.
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSetDefaultStore  <br/> |MFCMAPI usa el método **IMAPISession::SetDefaultStore** para establecer el almacén seleccionado como el almacén predeterminado.  <br/> |
   
## <a name="see-also"></a>Vea también



[Propiedad canónico PidTagResourceFlags](pidtagresourceflags-canonical-property.md)
  
[Propiedad canónico PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

