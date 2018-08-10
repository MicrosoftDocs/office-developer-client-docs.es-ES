---
title: IMAPISessionQueryIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c8f05707d63f922c9ce22e6e520c6c57e686f884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817459"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**Hace referencia a**: Outlook 
  
Devuelve el identificador de entrada del objeto que proporciona la identidad principal para la sesión.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parámetros

 _lpcbEntryID_
  
> [out] Un puntero para el número de bytes en el identificador de entrada indicado por el parámetro _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Un puntero a un puntero al identificador de entrada del objeto que proporciona la identidad principal.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La identidad principal se devolvió correctamente.
    
MAPI_W_NO_SERVICE 
  
> La llamada se ha realizado correctamente, pero no hay ninguna identidad principal para la sesión. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession::QueryIdentity** recupera la identidad principal para la sesión actual y devuelve el valor a través del parámetro _lppEntryID_ . La identidad principal es un objeto, normalmente un usuario de mensajería, que representa al usuario de una sesión.  _lppEntryID_ devuelve la identidad principal para un objeto [IMailUser](imailuserimapiprop.md) , que también se almacena como la propiedad [PidTagEntryID](pidtagentryid-canonical-property.md) . Puede usar el valor devuelto en _lppEntryID_ para abrir un objeto de **IMailUser** con [IMAPISession::OpenEntry](imapisession-openentry.md).
  
Si bien muchos proveedores de servicios en varios servicios de mensaje pueden proporcionar la identidad principal para una sesión, MAPI designa un proveedor de servicio único. El proveedor de servicios que proporciona la identidad principal establece los siguientes elementos:
  
- El indicador STATUS_PRIMARY_IDENTITY en la propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- La propiedad **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).
    
- La propiedad **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).
    
- La propiedad **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).
    
Si el proveedor de servicios que proporciona la identidad principal pertenece a un servicio de mensajes, los otros proveedores de servicios en el servicio de mensajes también establecen las propiedades PR_IDENTITY. Estas propiedades se publican en la tabla de estado de la sesión. 
  
Si es posible, **QueryIdentity** devuelve el valor de la propiedad **PR_IDENTITY_ENTRYID** de la fila de estado cuente con STATUS_PRIMARY_IDENTITY. Si falta la propiedad **PR_IDENTITY_ENTRYID** de la fila de identidad principal, **QueryIdentity** devuelve un identificador de entrada único creado con otra información de esa fila. 
  
Si falta la marca STATUS_PRIMARY_IDENTITY de todas las columnas en la tabla de estado **PR_RESOURCE_FLAG** , **QueryIdentity** devuelve el primer identificador de entrada que se encuentre. Cuando no hay ningún identificador de entrada apropiada para devolver, **QueryIdentity** se realiza correctamente con la advertencia MAPI_W_NO_SERVICE y señala _lppEntryID_ a un identificador de entrada codificado de forma rígida. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Se puede llamar al método [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para asignar la tarea de proporcionar la identidad principal de la sesión de un servicio de mensajes. 
  
Otra forma de recuperar la identidad principal es mediante la búsqueda en la tabla de estado de la fila con las columnas **PR_RESOURCE_FLAGS** establecida en STATUS_PRIMARY_IDENTITY. Para obtener más información acerca de esta forma alternativa de recuperación de información de identidad, vea la [tabla de estado y objetos de estado](status-table-and-status-objects.md).
  
Cuando haya terminado con el identificador de entrada para la identidad principal devuelta por **QueryIdentity**, liberar su memoria mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para obtener más información acerca de la identidad en general, vea [Identidad principal de MAPI](mapi-primary-identity.md). 
  
Para obtener más información acerca de cómo recuperar la identidad de la sesión MAPI, vea [recuperación principales y proveedor de identidad](retrieving-primary-and-provider-identity.md). 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnQueryIdentity  <br/> |MFCMAPI utiliza el método **IMAPISession::QueryIdentity** para abrir la entrada de la libreta de direcciones para la identidad principal de la sesión.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Identidad principal de MAPI](mapi-primary-identity.md)
  
[Recuperar identidades de proveedor y principales](retrieving-primary-and-provider-identity.md)
  
[Uso de macros para el control de errores](using-macros-for-error-handling.md)
  
[Tabla de estado y objetos de estado](status-table-and-status-objects.md)

