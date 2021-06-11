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
ms.openlocfilehash: 6da488408d3be9464d6ae1e016d5095707d451e4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415442"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona implementaciones para las tareas que normalmente realizan los proveedores de servicios y las funciones de punto de entrada del servicio de mensajes. Los proveedores de servicios reciben un puntero a su objeto de soporte técnico cuando MAPI llama al método de inicio de sesión del objeto de proveedor. Los servicios de mensajes reciben su puntero de objeto de soporte técnico en la llamada a su función de punto de entrada.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Expuesto por:  <br/> |Objetos de compatibilidad  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPISup  <br/> |
|Tipo de puntero:  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[GetLastError](imapisupport-getlasterror.md) <br/> |Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error del objeto de soporte técnico anterior.  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Recupera las direcciones de las funciones de asignación y asignación de memoria MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md)).  <br/> |
|[Subscribe](imapisupport-subscribe.md) <br/> |Registra un receptor de avisos para recibir notificaciones a través de MAPI.  <br/> |
|[Unsubscribe](imapisupport-unsubscribe.md) <br/> |Cancela la responsabilidad de enviar notificaciones establecidas anteriormente con una llamada al **método Subscribe.**  <br/> |
|[Notificar](imapisupport-notify.md) <br/> |Envía una notificación de un evento especificado a un origen de aviso que se registró originalmente para la notificación a través del **método Subscribe.**  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Modifica la tabla de estado agregando una nueva fila o modificando una fila existente.  <br/> |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Registra la función de preprocesador de un proveedor de transporte (una función que se ajusta al [prototipo PreprocessMessage).](preprocessmessage.md)  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |Crea una nueva [estructura MAPIUID](mapiuid.md) que se usará como identificador único.  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Marca un objeto como inutilizable.  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Proporciona el control de la CPU a la cola MAPI para que pueda realizar las tareas que considere necesarias.  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Notifica a la cola MAPI de un cambio de estado o una solicitud de servicio.  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Crea un identificador de entrada para una dirección de uso único.  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Registra una estructura **MAPIUID** que representa de forma única al proveedor de servicios.  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |Abre una entrada de destinatario en un proveedor de libreta de direcciones externo.  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |Abre un objeto y devuelve un puntero de interfaz para obtener más acceso.  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Devuelve un puntero a la tabla única MAPI (una lista de plantillas que todos los proveedores de libretas de direcciones admiten para crear nuevos destinatarios).  <br/> |
|[Address](imapisupport-address.md) <br/> |Muestra el cuadro de diálogo dirección común.  <br/> |
|[Detalles](imapisupport-details.md) <br/> |Muestra un cuadro de diálogo que muestra detalles sobre una entrada de libreta de direcciones determinada.  <br/> |
|[NewEntry](imapisupport-newentry.md) <br/> |Agrega un nuevo destinatario directamente a un contenedor de libreta de direcciones o a la lista de destinatarios de un mensaje saliente.  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Muestra una hoja de propiedades de configuración.  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Copia o mueve mensajes de una carpeta a otra carpeta.  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Copia o mueve una carpeta de su carpeta principal actual a otra carpeta primaria.  <br/> |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |Copia o mueve todas las propiedades de un objeto, excepto las propiedades excluidas específicamente, a otro objeto.  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Copia o mueve una o más propiedades de un objeto a otro objeto.  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Recupera un objeto de progreso que muestra un indicador de progreso.  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Genera un informe leído o no leído para un mensaje.  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Prepara un mensaje para el envío a la cola MAPI.  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Completa la lista de destinatarios de un mensaje, expandiendo listas de distribución determinadas.  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |Procesa un mensaje enviado.  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Proporciona acceso a la libreta de direcciones.  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Realiza el postprocesamiento en un mensaje.  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Solicita la liberación de un almacén de mensajes de forma ordenar.  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Genera informes de entrega y no entrega.  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |Convierte el identificador de entrada interna de un almacén de mensajes en un identificador de entrada en el formato estándar MAPI.  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Hace que los cambios en una sección de perfil de almacén de mensajes se realicen de forma permanente.  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Implementa un objeto de almacenamiento para obtener acceso a una secuencia.  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Crea un objeto de soporte técnico de servicio de mensajes.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las libretas de direcciones, los almacenes de mensajes, los proveedores de transporte y los servicios de mensajes tienen sus propios objetos de soporte técnico. Los proveedores de servicios y los servicios de mensajes llaman a los métodos de sus objetos de soporte técnico como parte de sus implementaciones de otros métodos de interfaz. Cada objeto de soporte técnico tiene implementaciones completas de los métodos que se aplican a su autor de la llamada; los métodos que no son aplicables devuelven MAPI_E_NO_SUPPORT. Los objetos de soporte del proveedor de libreta de direcciones tienen implementaciones para los siguientes métodos:
  
||||
|:-----|:-----|:-----|
|**Address** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**Detalles** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**GetLastError** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Notificar** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Subscribe** <br/> |**Unsubscribe** <br/> |**WrapStoreEntryID** <br/> |
   
Los objetos de soporte del proveedor del almacén de mensajes tienen implementaciones para los siguientes métodos:
  
||||
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**DoCopyTo** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Notificar** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**OpenProfileSection** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Subscribe** <br/> |**Unsubscribe** <br/> |
|**WrapStoreEntryID** <br/> |
   
Los objetos de soporte del proveedor de transporte tienen implementaciones para los siguientes métodos:
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**GetLastError** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Notificar** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Subscribe** <br/> |**Unsubscribe** <br/> |
   
Los objetos de soporte técnico del servicio de mensajes tienen implementaciones para los siguientes métodos:
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

