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
ms.openlocfilehash: 871dafd7bf8959cf814d65991fe08fdb2b283c08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817213"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**Hace referencia a**: Outlook 
  
Devuelve un puntero a la tabla de contenido del contenedor.
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se devuelve en la tabla de contenido. Se pueden establecer los siguientes indicadores:
    
MAPI_ASSOCIATED 
  
> Tabla de contenido asociado del contenedor se debe devolver en lugar de la tabla de contenido estándar. Este indicador se utiliza sólo con las carpetas. Los mensajes que se incluyen en la tabla de contenido asociado se crearon con el indicador MAPI_ASSOCIATED establecido en la llamada al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . Normalmente, los clientes utilizan en la tabla de contenido asociada para recuperar formularios, vistas y otros mensajes ocultos. 
    
ACLTABLE_FREEBUSY
  
> Permite el acceso a los derechos de frightsFreeBusySimple y frightsFreeBusyDetailed en **PR_MEMBER_RIGHTS**.
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable** puede devolver correctamente, posiblemente antes de que la tabla está disponible para el autor de la llamada. Si no está disponible en la tabla, realizar una llamada de tabla subsiguiente puede producir un error. 
    
MAPI_UNICODE. 
  
> Solicitudes que se devuelven las columnas que contienen datos de cadena en el formato Unicode. Si no está establecido el indicador MAPI_UNICODE., se deben devolver las cadenas en el formato ANSI. 
    
SHOW_SOFT_DELETES
  
> Muestra los elementos que actualmente están marcados como suaves eliminan, es decir, se encuentran en la retención de elementos eliminados fase de tiempo.
    
 _lppTable_
  
> [out] Un puntero a un puntero a la tabla de contenido.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> En la tabla de contenido se recuperó correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.
    
MAPI_E_NO_SUPPORT 
  
> El contenedor tiene contenido y no puede proporcionar una tabla de contenido.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIContainer::GetContentsTable** devuelve un puntero a la tabla de contenido de un contenedor. Una tabla de contenido contiene información de resumen acerca de los objetos en el contenedor. 
  
Las tablas de contenido tienen conjuntos de columnas prolongada. Para obtener una lista completa de las columnas obligatorias y opcionales en las tablas de contenido, vea [Las tablas de contenido](contents-tables.md). 
  
Es posible que algunos contenedores tener ningún contenido. Estos contenedores devuelven MAPI_E_NO_SUPPORT de sus implementaciones de **GetContentsTable**.
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Si decide admitir una tabla de contenido de su contenedor, también debe hacer lo siguiente:
  
- Admite las llamadas al método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la propiedad **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).
    
- Devolver **PR_CONTAINER_CONTENTS** en respuesta a una llamada en el contenedor 
    
    Métodos [IMAPIProp::GetProps](imapiprop-getprops.md) y [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
    
Implementación del proveedor de transporte remoto de este método debe devolver un puntero a un [IMAPITable: IUnknown](imapitableiunknown.md) interfaz en el parámetro _ppTable_ que se pasan al método **GetContentsTable** . Si su proveedor de transporte tiene una tabla de contenido existente, es suficiente devolver un puntero a ella. Si no, este método debe crear un nuevo [IMAPITable: IUnknown](imapitableiunknown.md) de objetos, rellenar la tabla con encabezados de mensaje (si hay alguno disponible) y devolver un puntero a la nueva tabla. El método [ITableData::HrGetView](itabledata-hrgetview.md) es útil para generar un valor devuelto y almacenar el puntero de la tabla en el parámetro _ppTable_ . En la tabla de contenido debe admitir al menos las siguientes columnas de propiedad: 
  
- **Entrada del objeto** ([PidTagEntryID](pidtagentryid-canonical-property.md))
    
- **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
    
- **PR_SENT_REPRESENTING_NAME de MAPI** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))
    
- **PR_DISPLAY_TO de MAPI** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))
    
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

Las columnas de tabla de contenido de cadena y binaria se pueden truncar. Normalmente, los proveedores devuelven 255 caracteres. Debido a que no se conoce de antemano si una tabla incluye columnas truncadas, supongamos que una columna se trunca si la longitud de la columna es de 255 o 510 bytes. Siempre puede recuperar el valor completo de una columna truncada, si es necesario, directamente desde el objeto mediante su identificador de entrada para abrirlo y, a continuación, llamar al método **IMAPIProp::GetProps** . 
  
Dependiendo del proveedor en la implementación, las restricciones y las operaciones de ordenación pueden aplicar a todos de una cadena o a la versión truncada de dicha cadena.
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableDialog.cpp  <br/> |CContentsTableDlg::CContentsTableDlg  <br/> |La clase **CContentsTableDlg** utiliza **GetContentsTable** para obtener las entradas en una tabla de contenido.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propiedad canónica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

