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
ms.openlocfilehash: 396320c6b39553da09aa1f45d0c755f40a939382
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428224"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el identificador de entrada del objeto que proporciona la identidad principal de la sesión.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parámetros

 _lpcbEntryID_
  
> [salida] Puntero al recuento de bytes en el identificador de entrada al que apunta el _parámetro lppEntryID._ 
    
 _lppEntryID_
  
> [salida] Puntero a un puntero al identificador de entrada del objeto que proporciona la identidad principal.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La identidad principal se devolvió correctamente.
    
MAPI_W_NO_SERVICE 
  
> La llamada se ha hecho correctamente, pero no hay ninguna identidad principal para la sesión. Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta. Para probar esta advertencia, use la **macro HR_FAILED** datos. Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentarios

El **método IMAPISession::QueryIdentity** recupera la identidad principal de la sesión actual y devuelve el valor a través del parámetro _lppEntryID._ La identidad principal es un objeto, normalmente un usuario de mensajería, que representa al usuario de una sesión.  _lppEntryID_ devuelve la identidad principal de un [objeto IMailUser,](imailuserimapiprop.md) que también se almacena como la [propiedad PidTagEntryID.](pidtagentryid-canonical-property.md) Puede usar el valor devuelto en  _lppEntryID para_ abrir un objeto **IMailUser** mediante [IMAPISession::OpenEntry](imapisession-openentry.md).
  
Aunque muchos proveedores de servicios en varios servicios de mensajes pueden proporcionar la identidad principal de una sesión, MAPI designa un único proveedor de servicios. El proveedor de servicios que proporciona la identidad principal establece los siguientes elementos:
  
- Marca STATUS_PRIMARY_IDENTITY en la **propiedad PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- Propiedad **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).
    
- Propiedad **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).
    
- Propiedad **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).
    
Si el proveedor de servicios que proporciona la identidad principal pertenece a un servicio de mensajes, los demás proveedores de servicios del servicio de mensajes también establecen las PR_IDENTITY servicio. Estas propiedades se publican en la tabla de estado de la sesión. 
  
Si es posible, **QueryIdentity** devuelve el valor de la **propiedad PR_IDENTITY_ENTRYID** de la fila de estado etiquetada con STATUS_PRIMARY_IDENTITY. Si falta **PR_IDENTITY_ENTRYID** propiedad de la fila de identidad principal, **QueryIdentity** devuelve un identificador de entrada de uso único creado con otra información de esa fila. 
  
Si falta STATUS_PRIMARY_IDENTITY marca en todas las columnas **PR_RESOURCE_FLAG** de la tabla de estado, **QueryIdentity** devuelve el primer identificador de entrada que encuentra. Cuando no hay ningún identificador de entrada adecuado para devolver, **QueryIdentity** se ejecuta correctamente con la advertencia MAPI_W_NO_SERVICE y apunta  _lppEntryID_ a un identificador de entrada codificado de forma hard. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede llamar al método [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para asignar a un servicio de mensajes la tarea de suministrar la identidad principal de la sesión. 
  
Otra forma de recuperar la identidad principal es mediante la búsqueda en la tabla de estado de la fila con las **columnas PR_RESOURCE_FLAGS** establecidas en STATUS_PRIMARY_IDENTITY. Para obtener más información acerca de esta forma alternativa de recuperar información de identidad, vea [Tabla de estado y Objetos de estado](status-table-and-status-objects.md).
  
Cuando haya terminado de usar el identificador de entrada para la identidad principal devuelta por **QueryIdentity**, libera su memoria llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
Para obtener más información acerca de la identidad en general, vea [Identidad principal mapi](mapi-primary-identity.md). 
  
Para obtener más información acerca de cómo recuperar la identidad de la sesión MAPI, vea [Recuperar la identidad principal y del proveedor.](retrieving-primary-and-provider-identity.md) 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnQueryIdentity  <br/> |MFCMAPI usa el **método IMAPISession::QueryIdentity** para abrir la entrada de la libreta de direcciones para la identidad principal de la sesión.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Identidad principal mapi](mapi-primary-identity.md)
  
[Recuperación de identidad principal y de proveedor](retrieving-primary-and-provider-identity.md)
  
[Uso de macros para el control de errores](using-macros-for-error-handling.md)
  
[Tabla de estado y objetos de estado](status-table-and-status-objects.md)

