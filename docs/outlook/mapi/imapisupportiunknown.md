---
title: IMAPISupport IUnknown
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
ms.openlocfilehash: 4843a52d7441de1e1ab545e80346db8dd308c4bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590207"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona implementaciones para las tareas que normalmente se llevan a cabo por los proveedores de servicios y funciones de punto de entrada de servicio de mensajes. Proveedores de servicios de reciben un puntero a su objeto de soporte técnico cuando MAPI llama el método de inicio de sesión del objeto de su proveedor. Servicios de mensajes reciben su puntero de objeto de soporte técnico en la llamada a su función de punto de entrada.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Expuestos por:  <br/> |Compatibilidad con objetos  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPISup  <br/> |
|Tipo de puntero:  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](imapisupport-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de objeto de soporte técnico anterior.  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Recupera las direcciones de la memoria de asignación y cancelación de asignación de funciones de MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md)).  <br/> |
|[Subscribe](imapisupport-subscribe.md) <br/> |Registra un receptor de notificaciones para recibir notificaciones a través de MAPI.  <br/> |
|[Unsubscribe](imapisupport-unsubscribe.md) <br/> |Cancela la responsabilidad de envío de notificaciones que se estableció previamente con una llamada al método **Subscribe** .  <br/> |
|[Notify](imapisupport-notify.md) <br/> |Envía una notificación de un evento especificado a un origen de advise que registró originalmente para la notificación a través del método **Subscribe** .  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Modifica la tabla de estado al agregar una fila nueva o modificar una fila existente.  <br/> |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para aún más el acceso  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Registra la función de preprocesador del proveedor de transporte (una función que se ajusta al prototipo [PreprocessMessage](preprocessmessage.md) ).  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |Crea una nueva estructura [MAPIUID](mapiuid.md) que se utilizará como un identificador único.  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Marca un objeto como no utilizable.  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Proporciona control de la CPU a la cola de MAPI para que pueda realizar las tareas que considere necesarias.  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Notifica a la cola MAPI de un cambio de estado o una solicitud de servicio.  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Crea un identificador de entrada para una dirección de uso único.  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Registra una estructura **MAPIUID** que representa el proveedor de servicios de forma exclusiva.  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |Se abre una entrada del destinatario en un proveedor de libreta de direcciones externa.  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |Se abre un objeto y devuelve un puntero de interfaz para aún más el acceso.  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Devuelve un puntero a la tabla de uso único de MAPI (una lista de plantillas que todos los libreta de direcciones de proveedores de soporte técnico para la creación de nuevos destinatarios).  <br/> |
|[Dirección](imapisupport-address.md) <br/> |Muestra el cuadro de diálogo dirección común.  <br/> |
|[Detalles](imapisupport-details.md) <br/> |Muestra un cuadro de diálogo que muestra detalles acerca de una entrada de la libreta de direcciones determinada.  <br/> |
|[NewEntry](imapisupport-newentry.md) <br/> |Agrega a un nuevo destinatario directamente a un contenedor de la libreta de direcciones o a la lista de destinatarios de un mensaje saliente.  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Muestra una hoja de propiedades de configuración.  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Copia o mueve los mensajes de una carpeta a otra carpeta.  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Copia o mueve una carpeta de su carpeta primaria actual a otra carpeta primaria.  <br/> |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |Copia o mueve todas las propiedades de un objeto, excepto propiedades excluidas específicamente, a otro objeto.  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Copia o mueve una o más propiedades de un objeto a otro objeto.  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Recupera un objeto de progreso que muestra un indicador de progreso.  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Genera una lectura o del informe nonread para un mensaje.  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Prepara un mensaje para el envío a la cola de MAPI.  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Finaliza la lista de destinatarios de un mensaje, expansión de las listas de distribución en particular.  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |Procesa un mensaje enviado.  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Proporciona acceso a la libreta de direcciones.  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Realiza procesamiento posterior en un mensaje.  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Solicita la versión ordenada de un almacén de mensajes.  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Genera informes de entrega y no entrega.  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |Convierte el identificador de entrada interno de un almacén de mensajes en un identificador de entrada con el formato estándar de MAPI.  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Hace que los cambios realizados en un mensaje de almacenar permanente de sección de perfil.  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Implementa un objeto de almacenamiento para obtener acceso a una secuencia.  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Crea un objeto de soporte técnico del servicio de mensajes.  <br/> |
   
## <a name="remarks"></a>Comentarios

Libretas de direcciones, almacenes de mensajes, los proveedores de transporte y servicios que cada uno tienen sus propios objetos de ayuda para el mensaje. Proveedores de servicios y los servicios de message llamar a los métodos en sus objetos de soporte técnico como parte de sus implementaciones de otros métodos de interfaz. Cada objeto de compatibilidad con diferentes tiene implementaciones completas de los métodos que se aplican a su autor de la llamada; los métodos que no son aplicables devolución MAPI_E_NO_SUPPORT. Objetos de soporte técnico de proveedor de la libreta de dirección tienen implementaciones para los métodos siguientes:
  
||||
|:-----|:-----|:-----|
|**Dirección** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**Detalles** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**GetLastError** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Notify** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Subscribe** <br/> |**Unsubscribe** <br/> |**WrapStoreEntryID** <br/> |
   
Objetos de soporte técnico de proveedor de almacén de mensajes tienen implementaciones para los métodos siguientes:
  
||||
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**DoCopyTo** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Notify** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**OpenProfileSection** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Subscribe** <br/> |**Unsubscribe** <br/> |
|**WrapStoreEntryID** <br/> |
   
Objetos de Ayuda del proveedor de transporte tienen implementaciones para los métodos siguientes:
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**GetLastError** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Notify** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Subscribe** <br/> |**Unsubscribe** <br/> |
   
Objetos de Ayuda del servicio de mensaje tienen implementaciones para los métodos siguientes:
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

