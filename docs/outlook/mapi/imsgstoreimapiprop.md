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
ms.openlocfilehash: 426333e6e2624adcd7cb6bc6dc4982b3d1ef1999
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817782"
---
# <a name="imsgstore--imapiprop"></a>IMsgStore : IMAPIProp

  
  
**Hace referencia a**: Outlook 
  
Proporciona acceso al almacén de información del mensaje y a los mensajes y carpetas.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Objeto de almacén de mensajes  <br/> |
|Se implementa mediante:  <br/> |Proveedores de almacén de mensajes  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente, la cola MAPI y MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMsgStore  <br/> |
|Tipo de puntero:  <br/> |LPMDB  <br/> |
|Modelo de transacciones:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Aviso](imsgstore-advise.md) <br/> |Se registra para recibir notificaciones de los eventos que afectan el almacén de mensajes.  <br/> |
|[Desaconsejar](imsgstore-unadvise.md) <br/> |Cancela el envío de notificaciones configuradas previamente con una llamada al método **IMsgStore::Advise** .  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |Compara dos identificadores de entrada para determinar si hacen referencia a la misma entrada en un almacén de mensajes.  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |Se abre una carpeta o un mensaje y devuelve un puntero de interfaz para aún más el acceso.  <br/> |
|[SetReceiveFolder](imsgstore-setreceivefolder.md) <br/> |Establece una carpeta como destino de los mensajes entrantes de una clase de mensaje en particular.  <br/> |
|[GetReceiveFolder](imsgstore-getreceivefolder.md) <br/> |Obtiene la carpeta que se estableció como el destino para los mensajes entrantes de una clase de mensaje especificado o como el valor predeterminado de recepción carpeta para el almacén de mensajes.  <br/> |
|[GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) <br/> |Proporciona acceso a la tabla de la carpeta de recepción, una tabla con información acerca de todas las carpetas de recepción para el almacén de mensajes.  <br/> |
|[StoreLogoff](imsgstore-storelogoff.md) <br/> |Permite el cierre de sesión ordenada del almacén de mensajes.  <br/> |
|[AbortSubmit](imsgstore-abortsubmit.md) <br/> |Intenta quitar un mensaje de la cola de salida.  <br/> |
|[GetOutgoingQueue](imsgstore-getoutgoingqueue.md) <br/> |Proporciona acceso a la tabla de cola saliente, una tabla que contiene información acerca de todos los mensajes en cola de salida del almacén de mensajes.  <br/> |
|[SetLockState](imsgstore-setlockstate.md) <br/> |Bloquea o desbloquea un mensaje.  <br/> |
|[FinishedMsg](imsgstore-finishedmsg.md) <br/> |Permite que el proveedor de almacén de mensajes realizar el procesamiento en un mensaje enviado.  <br/> |
|[NotifyNewMail](imsgstore-notifynewmail.md) <br/> |Informa el almac�n de mensajes que ha llegado un mensaje nuevo.  <br/> |
   
|**Propiedades requeridas**|**Nivel de acceso**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Es de lectura y escritura.  <br/> |
|**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
Las siguientes propiedades son para los almacenes de mensajes mensajes interpersonales (IPM):
  
- **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
    
- **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
    
- **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
    
- **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)

