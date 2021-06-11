---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422330"
---
# <a name="imsgstore--imapiprop"></a>IMsgStore : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la información del almacén de mensajes y a los mensajes y carpetas.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |Objeto de almacén de mensajes  <br/> |
|Implementado por:  <br/> |Proveedores de almacén de mensajes  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente, la cola MAPI y MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMsgStore  <br/> |
|Tipo de puntero:  <br/> |LPMDB  <br/> |
|Modelo de transacciones:  <br/> |No transacted  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[Aconsejar](imsgstore-advise.md) <br/> |Se registra para recibir una notificación de eventos especificados que afectan al almacén de mensajes.  <br/> |
|[Unadvise](imsgstore-unadvise.md) <br/> |Cancela el envío de notificaciones configuradas anteriormente con una llamada al **método IMsgStore::Advise.**  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |Compara dos identificadores de entrada para determinar si hacen referencia a la misma entrada en un almacén de mensajes.  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |Abre una carpeta o mensaje y devuelve un puntero de interfaz para obtener más acceso.  <br/> |
|[SetReceiveFolder](imsgstore-setreceivefolder.md) <br/> |Establece una carpeta como destino para los mensajes entrantes de una clase de mensaje determinada.  <br/> |
|[GetReceiveFolder](imsgstore-getreceivefolder.md) <br/> |Obtiene la carpeta que se estableció como destino para los mensajes entrantes de una clase de mensaje especificada o como la carpeta de recepción predeterminada para el almacén de mensajes.  <br/> |
|[GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) <br/> |Proporciona acceso a la tabla de carpetas de recepción, una tabla con información sobre todas las carpetas de recepción del almacén de mensajes.  <br/> |
|[StoreLogoff](imsgstore-storelogoff.md) <br/> |Habilita el cierre de sesión orden del almacén de mensajes.  <br/> |
|[AbortSubmit](imsgstore-abortsubmit.md) <br/> |Intenta quitar un mensaje de la cola saliente.  <br/> |
|[GetOutgoingQueue](imsgstore-getoutgoingqueue.md) <br/> |Proporciona acceso a la tabla de cola saliente, una tabla que tiene información sobre todos los mensajes de la cola saliente del almacén de mensajes.  <br/> |
|[SetLockState](imsgstore-setlockstate.md) <br/> |Bloquea o desbloquea un mensaje.  <br/> |
|[FinishedMsg](imsgstore-finishedmsg.md) <br/> |Permite al proveedor del almacén de mensajes realizar el procesamiento en un mensaje enviado.  <br/> |
|[NotifyNewMail](imsgstore-notifynewmail.md) <br/> |Informa el almac�n de mensajes que ha llegado un mensaje nuevo.  <br/> |
   
|**Propiedades requeridas**|**Nivel de acceso**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
Las propiedades siguientes son para los almacenes de mensajes de mensajes interpersonales (IPM):
  
- **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
    
- **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
    
- **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
    
- **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)

