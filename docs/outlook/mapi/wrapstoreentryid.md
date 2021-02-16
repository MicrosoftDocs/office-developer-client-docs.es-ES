---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409212"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte el identificador de entrada interna de un almacén de mensajes en un identificador de entrada más utilizable por el sistema de mensajería. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
WrapStoreEntryID(
  ULONG ulFlags,
  LPSTR szDLLName,
  ULONG cbOrigEntry,
  LPENTRYID lpOrigEntry,
  ULONG * lpcbWrappedEntry,
  LPENTRYID * lppWrappedEntry
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas están en formato Unicode. Si no MAPI_UNICODE marca, las cadenas están en formato ANSI. 
    
 _szDLLName_
  
> [entrada] Nombre de la DLL del proveedor del almacén de mensajes. 
    
 _cbOrigEntry_
  
> [entrada] Tamaño, en bytes, del identificador de entrada original para el almacén de mensajes. 
    
 _lpOrigEntry_
  
> [entrada] Puntero a una [estructura ENTRYID](entryid.md) que contiene el identificador de entrada original. 
    
 _lpcbWrappedEntry_
  
> [salida] Puntero al tamaño, en bytes, del nuevo identificador de entrada. 
    
 _lppWrappedEntry_
  
> [salida] Puntero a un puntero a una **estructura ENTRYID** que contiene el nuevo identificador de entrada. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Un objeto de almacén de mensajes conserva un identificador de entrada interno que solo es significativo para los proveedores de servicios que se encuentra en ese almacén de mensajes. Para otros componentes de mensajería, MAPI proporciona una versión ajustada del identificador de entrada interno que hace que sea reconocible como que pertenece al almacén de mensajes. Los proveedores de servicios coresident siempre deben tener el identificador de entrada del almacén de mensajes original sin envolver; las aplicaciones cliente siempre deben tener la versión ajustada, que se puede usar en cualquier parte del dominio de mensajería y en otros dominios. 
  
Un proveedor de servicios puede encapsular un identificador de entrada de almacén de mensajes mediante la función **WrapStoreEntryID** o el método [IMAPISupport::WrapStoreEntryID,](imapisupport-wrapstoreentryid.md) que llama a la **función WrapStoreEntryID.** El proveedor debe encapsular el identificador de entrada al exponer la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) del almacén de mensajes o escribirla en una sección de perfil, y al exponer la propiedad **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)). MAPI encapsula un identificador de entrada del almacén de mensajes al responder a una [llamada IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md) 
  
Cuando una aplicación cliente pasa un identificador de entrada de almacén de mensajes ajustado a MAPI, por ejemplo en una llamada [IMAPISession::OpenEntry,](imapisession-openentry.md) MAPI desenvuelve el identificador de entrada antes de usarlo para llamar a un método de proveedor como [IMSProvider::Logon](imsprovider-logon.md) o [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md). 
  

