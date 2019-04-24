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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349290"
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

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se devuelve la tabla de contenido. Se pueden establecer los siguientes indicadores:
    
MAPI_ASSOCIATED 
  
> La tabla de contenido asociada al contenedor debe devolverse en lugar de la tabla de contenido estándar. Esta marca solo se usa con carpetas. Los mensajes que se incluyen en la tabla de contenido asociada se crearon con la marca MAPI_ASSOCIATED establecida en la llamada al método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) . Los clientes suelen usar la tabla de contenido asociada para recuperar formularios, vistas y otros mensajes ocultos. 
    
ACLTABLE_FREEBUSY
  
> Habilita el acceso a los derechos frightsFreeBusySimple y frightsFreeBusyDetailed en **PR_MEMBER_RIGHTS**.
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable** puede volver correctamente, posiblemente antes de que el autor de la llamada haya disponible la tabla. Si la tabla no está disponible, realizar una llamada subsiguiente a la tabla puede generar un error. 
    
MAPI_UNICODE 
  
> Solicita que las columnas que contienen datos de cadena se devuelvan en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas deben devolverse en formato ANSI. 
    
SHOW_SOFT_DELETES
  
> Muestra los elementos que están marcados actualmente como eliminados temporalmente, es decir, se encuentran en la fase de retención de elementos eliminados.
    
 _lppTable_
  
> contempla Un puntero a un puntero a la tabla de contenido.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de contenido se ha recuperado correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.
    
MAPI_E_NO_SUPPORT 
  
> El contenedor no tiene contenido y no puede proporcionar una tabla de contenido.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIContainer:: GetContentsTable** devuelve un puntero a la tabla de contenido de un contenedor. Una tabla de contenido contiene información de resumen sobre los objetos del contenedor. 
  
Las tablas de contenido tienen conjuntos de columnas extensos. Para obtener una lista completa de las columnas obligatorias y opcionales en las tablas de contenido, vea [tablas de contenido](contents-tables.md). 
  
Es posible que algunos contenedores no tengan contenido. Estos contenedores devuelven MAPI_E_NO_SUPPORT de sus implementaciones de **GetContentsTable**.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si admite una tabla de contenido para el contenedor, también debe hacer lo siguiente:
  
- Admitir llamadas al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la propiedad **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).
    
- Devuelve **PR_CONTAINER_CONTENTS** en respuesta a una llamada a la del contenedor. 
    
    [IMAPIProp:: GetProps](imapiprop-getprops.md) y [IMAPIProp:: GetPropList](imapiprop-getproplist.md) métodos. 
    
La implementación de este método por un proveedor de transporte remoto debe devolver un puntero a una interfaz [IMAPITable: IUnknown](imapitableiunknown.md) en el parámetro _ppTable_ que se pasa al método **GetContentsTable** . Si el proveedor de transporte tiene una tabla Contents existente, es suficiente devolver un puntero a ella. Si no es así, este método debe crear un nuevo objeto [IMAPITable: IUnknown](imapitableiunknown.md) , rellenar la tabla con encabezados de mensaje (si hay alguno disponible) y devolver un puntero a la nueva tabla. El método [ITableData:: HrGetView](itabledata-hrgetview.md) es útil para generar un valor devuelto y almacenar el puntero de tabla en el parámetro _ppTable_ . La tabla de contenido debe admitir al menos las siguientes columnas de propiedades: 
  
- **** Es ([PidTagEntryID](pidtagentryid-canonical-property.md))
    
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

Las columnas de la tabla de contenido binario y de cadena pueden truncarse. Normalmente, los proveedores devuelven 255 caracteres. Como no se puede saber de antemano si una tabla incluye columnas truncadas, se supone que una columna está truncada si la longitud de la columna es de 255 o de 510 bytes. Siempre puede recuperar el valor completo de una columna truncada, si es necesario, directamente desde el objeto mediante su identificador de entrada para abrirla y, a continuación, llamar al método **IMAPIProp:: GetProps** . 
  
Según la implementación del proveedor, las restricciones y las operaciones de ordenación pueden aplicarse a toda una cadena o a la versión truncada de dicha cadena.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableDialog. cpp  <br/> |CContentsTableDlg:: CContentsTableDlg  <br/> |La clase **CContentsTableDlg** usa **GetContentsTable** para obtener las entradas de una tabla de contenido.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propiedad canónica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

