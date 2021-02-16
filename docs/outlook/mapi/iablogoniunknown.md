---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fc8615fcd984623ae9c17c45fb7b51a4498a723b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431081"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Accede a los recursos de un proveedor de libreta de direcciones.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Expuesto por:  <br/> |Objetos de inicio de sesión de la libreta de direcciones  <br/> |
|Implementado por:  <br/> |Proveedores de libretas de direcciones  <br/> |
|Llamado por:  <br/> |MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IABLogon  <br/> |
|Tipo de puntero:  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior del proveedor de libreta de direcciones.  <br/> |
|[Cierre de sesión](iablogon-logoff.md) <br/> |Inicia el proceso de cierre de sesión.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Abre un contenedor, un usuario de mensajería o una lista de distribución y devuelve un puntero a una implementación de interfaz para proporcionar acceso adicional.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.  <br/> |
|[Aconsejar](iablogon-advise.md) <br/> |Registra al autor de la llamada para recibir una notificación de eventos especificados que afectan a un contenedor, un usuario de mensajería o una lista de distribución.  <br/> |
|[Unadvise](iablogon-unadvise.md) <br/> |Cancela las notificaciones configuradas anteriormente con una llamada al **método Advise.**  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Abre el objeto de estado del proveedor.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Abre una entrada de destinatario que tiene datos que residen en un proveedor de libreta de direcciones host.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Devuelve una tabla de plantillas de uso único para crear destinatarios que se agregarán a la lista de destinatarios de un mensaje saliente.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Prepara una lista de destinatarios para su uso posterior por parte del sistema de mensajería.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener información general acerca de los métodos de **la interfaz IABLogon,** vea Implementar el inicio de sesión [del proveedor de servicios.](implementing-service-provider-logon.md)
  
## <a name="see-also"></a>Consulte también



[Interfaces MAPI](mapi-interfaces.md)

