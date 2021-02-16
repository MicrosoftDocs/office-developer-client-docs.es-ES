---
title: IMAPIContainerGetContentsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431109"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un puntero a la tabla de contenido del contenedor.
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se devuelve la tabla de contenido. Se pueden establecer las siguientes marcas:
    
MAPI_ASSOCIATED 
  
> Se debe devolver la tabla de contenido asociada del contenedor en lugar de la tabla de contenido estándar. Esta marca solo se usa con carpetas. Los mensajes que se incluyen en la tabla de contenido asociada se crearon con la marca MAPI_ASSOCIATED establecida en la llamada al método [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) Normalmente, los clientes usan la tabla de contenido asociada para recuperar formularios, vistas y otros mensajes ocultos. 
    
ACLTABLE_FREEBUSY
  
> Habilita el acceso a los derechos frightsFreeBusySimple y frightsFreeBusyDetailed en **PR_MEMBER_RIGHTS**.
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable** puede devolverse correctamente, posiblemente antes de que la tabla esté disponible para el autor de la llamada. Si la tabla no está disponible, realizar una llamada de tabla posterior puede generar un error. 
    
MAPI_UNICODE 
  
> Solicita que las columnas que contienen datos de cadena se devuelvan en formato Unicode. Si no MAPI_UNICODE marca, las cadenas deben devolverse en el formato ANSI. 
    
SHOW_SOFT_DELETES
  
> Muestra los elementos que están marcados actualmente como eliminados temporalmente, es decir, están en la fase de tiempo de retención de elementos eliminados.
    
 _lppTable_
  
> [salida] Puntero a un puntero a la tabla de contenido.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de contenido se recuperó correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.
    
MAPI_E_NO_SUPPORT 
  
> El contenedor no tiene contenido y no puede proporcionar una tabla de contenido.
    
## <a name="remarks"></a>Comentarios

El **método IMAPIContainer::GetContentsTable** devuelve un puntero a la tabla de contenido de un contenedor. Una tabla de contenido contiene información resumida acerca de los objetos del contenedor. 
  
Las tablas de contenido tienen conjuntos de columnas largos. Para obtener una lista completa de las columnas obligatorias y opcionales de las tablas de contenido, vea [Tablas de contenido.](contents-tables.md) 
  
Es posible que algunos contenedores no tengan contenido. Estos contenedores devuelven MAPI_E_NO_SUPPORT de sus implementaciones **de GetContentsTable**.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si admite una tabla de contenido para el contenedor, también debe hacer lo siguiente:
  
- Llamadas de soporte técnico al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para abrir **la PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).
    
- Devolver **PR_CONTAINER_CONTENTS** respuesta a una llamada al contenedor 
    
    [Métodos IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
    
La implementación de este método por parte de un proveedor de transporte remoto debe devolver un puntero a una interfaz [IMAPITable : IUnknown](imapitableiunknown.md) en el parámetro _ppTable_ pasado al **método GetContentsTable.** Si el proveedor de transporte tiene una tabla de contenido existente, es suficiente con devolver un puntero a ella. Si no es así, este método debe crear un nuevo objeto [IMAPITable : IUnknown,](imapitableiunknown.md) rellenar la tabla con encabezados de mensaje (si hay alguno disponible) y devolver un puntero a la nueva tabla. El [método ITableData::HrGetView](itabledata-hrgetview.md) es útil para generar un valor devuelto y almacenar el puntero de tabla en el _parámetro ppTable._ La tabla de contenido debe admitir al menos las siguientes columnas de propiedad: 
  
- **PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))
    
- **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
    
- **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))
    
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))
    
- **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))
    
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))
    
- **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
    
- **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
    
- **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
    
- **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))
    
- **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Las columnas de la tabla de contenido binario y de cadena se pueden truncar. Normalmente, los proveedores devuelven 255 caracteres. Como no puede saber de antemano si una tabla incluye columnas truncadas, suponga que una columna se trunca si la longitud de la columna es de 255 o 510 bytes. Siempre puede recuperar el valor completo de una columna truncada, si es necesario, directamente desde el objeto usando su identificador de entrada para abrirlo y, a continuación, llamando al método **IMAPIProp::GetProps.** 
  
Según la implementación del proveedor, las restricciones y las operaciones de ordenación pueden aplicarse a toda una cadena o a la versión truncada de esa cadena.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableDialog.cpp  <br/> |CContentsTableDlg::CContentsTableDlg  <br/> |La **clase CContentsTableDlg** usa **GetContentsTable** para obtener las entradas de una tabla de contenido.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propiedad canónica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

