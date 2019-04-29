---
title: IUnknown IMAPISupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport
api_type:
- COM
ms.assetid: 92bfe604-18dd-46a1-9ae8-0b04167606bd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6da488408d3be9464d6ae1e016d5095707d451e4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415442"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona implementaciones para tareas que normalmente realizan los proveedores de servicios y las funciones de punto de entrada del servicio de mensajes. Los proveedores de servicios reciben un puntero a su objeto de soporte cuando MAPI llama al método de inicio de sesión del objeto de proveedor. Los servicios de mensajes reciben su puntero de objeto de soporte en la llamada a su función de punto de entrada.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi. h  <br/> |
|Expuesto por:  <br/> |Objetos de compatibilidad  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPISup  <br/> |
|Tipo de puntero:  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Volvió](imapisupport-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior del objeto support.  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Recupera las direcciones de las funciones de asignación y desasignación de memoria MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md)).  <br/> |
|[Suscrito](imapisupport-subscribe.md) <br/> |Registra un receptor de notificaciones para recibir notificaciones a través de MAPI.  <br/> |
|[Unsubscribe](imapisupport-unsubscribe.md) <br/> |Cancela la responsabilidad para enviar notificaciones previamente establecidas con una llamada al método **subscribe** .  <br/> |
|[Notify](imapisupport-notify.md) <br/> |Envía una notificación de un evento especificado a un origen de notificaciones que se registró originalmente para la notificación mediante el método **subscribe** .  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Modifica la tabla de estado agregando una nueva fila o modificando una fila existente.  <br/> |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Registra la función de preprocesador del proveedor de transporte (una función que se ajusta al prototipo [PreprocessMessage](preprocessmessage.md) ).  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |Crea una nueva estructura [MAPIUID](mapiuid.md) para usarla como identificador único.  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Marca un objeto como inutilizable.  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Proporciona el control de la CPU a la cola MAPI para que pueda llevar a cabo las tareas que estime necesarias.  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Notifica a la cola MAPI un cambio de estado o una solicitud de servicio.  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Crea un identificador de entrada para una dirección de uso único.  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Registra una estructura **MAPIUID** que representa exclusivamente al proveedor de servicios.  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |Abre una entrada de destinatario en un proveedor de libreta de direcciones externa.  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |Abre un objeto y devuelve un puntero de interfaz para obtener más acceso.  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Devuelve un puntero a la tabla única de MAPI (una lista de plantillas que todos los proveedores de la libreta de direcciones admiten para crear nuevos destinatarios).  <br/> |
|[Dirección](imapisupport-address.md) <br/> |Muestra el cuadro de diálogo Dirección común.  <br/> |
|[Detalles](imapisupport-details.md) <br/> |Muestra un cuadro de diálogo que muestra los detalles de una entrada de la libreta de direcciones en particular.  <br/> |
|[NewEntry](imapisupport-newentry.md) <br/> |Agrega un nuevo destinatario directamente a un contenedor de libreta de direcciones o a la lista de destinatarios de un mensaje saliente.  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Muestra una hoja de propiedades de configuración.  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Copia o mueve mensajes de una carpeta a otra.  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Copia o mueve una carpeta de su carpeta principal actual a otra carpeta principal.  <br/> |
|[EnCopyto](imapisupport-docopyto.md) <br/> |Copia o mueve todas las propiedades de un objeto, excepto para las propiedades excluidas específicamente, a otro objeto.  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Copia o mueve una o varias propiedades de un objeto a otro objeto.  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Recupera un objeto Progress que muestra un indicador de progreso.  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Genera un informe de lectura o no leído para un mensaje.  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Prepara un mensaje para enviarlo a la cola MAPI.  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Completa la lista de destinatarios de un mensaje y expande listas de distribución particulares.  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |Procesa un mensaje enviado.  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Proporciona acceso a la libreta de direcciones.  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Realiza el procesamiento de postprocesamiento en un mensaje.  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Solicita la liberación ordenada de un almacén de mensajes.  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Genera informes de entrega y de no entrega.  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |Convierte el identificador de entrada interno de un almacén de mensajes en un identificador de entrada en el formato MAPI estándar.  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Realiza cambios permanentes en una sección de perfil del almacén de mensajes.  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Implementa un objeto de almacenamiento para obtener acceso a una secuencia.  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Crea un objeto de compatibilidad del servicio de mensajes.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las libretas de direcciones, los almacenes de mensajes, los proveedores de transporte y los servicios de mensajes tienen sus propios objetos de compatibilidad. Los proveedores de servicios y los servicios de mensajes llaman a los métodos en sus objetos de soporte como parte de sus implementaciones de otros métodos de interfaz. Cada objeto de compatibilidad diferente tiene implementaciones completas de los métodos que se aplican a su autor de la llamada; los métodos que no son aplicables devuelven MAPI_E_NO_SUPPORT. Los objetos de compatibilidad del proveedor de libreta de direcciones tienen implementaciones para los métodos siguientes:
  
||||
|:-----|:-----|:-----|
|**Dirección** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**Detalles** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**Volvió** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Notify** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Suscrito** <br/> |**Unsubscribe** <br/> |**WrapStoreEntryID** <br/> |
   
Los objetos de compatibilidad del proveedor de almacenamiento de mensajes tienen implementaciones para los métodos siguientes:
  
||||
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**EnCopyto** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**Volvió** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Notify** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**OpenProfileSection** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Suscrito** <br/> |**Unsubscribe** <br/> |
|**WrapStoreEntryID** <br/> |
   
Los objetos de soporte del proveedor de transporte tienen implementaciones para los métodos siguientes:
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**Volvió** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Notify** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Suscrito** <br/> |**Unsubscribe** <br/> |
   
Los objetos de compatibilidad del servicio de mensajes tienen implementaciones para los métodos siguientes:
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**Volvió** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

