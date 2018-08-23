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
ms.openlocfilehash: 4421fcde6ccd2f2ac6245927d9d5d63ddc5200af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573519"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recursos de accesos en un proveedor de la libreta de direcciones.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Expuestos por:  <br/> |Objetos de inicio de sesión de la libreta de direcciones  <br/> |
|Se implementa mediante:  <br/> |Proveedores de la libreta de direcciones  <br/> |
|Llamado por:  <br/> |MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IABLogon  <br/> |
|Tipo de puntero:  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de proveedor de la libreta de direcciones anterior.  <br/> |
|[Cierre de sesión](iablogon-logoff.md) <br/> |Inicia el proceso de cierre de sesión.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Se abre un contenedor, usuario o lista de distribución, de mensajería y devuelve un puntero a una implementación de interfaz para proporcionar más acceso.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.  <br/> |
|[Aviso](iablogon-advise.md) <br/> |Registra el autor de la llamada para recibir notificaciones de los eventos que afectan a un contenedor, usuario o lista de distribución de mensajería.  <br/> |
|[Desaconsejar](iablogon-unadvise.md) <br/> |Cancela las notificaciones que se han configurado previamente con una llamada al método **Advise** .  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Se abre el objeto de estado del proveedor.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Se abre una entrada del destinatario que tiene datos que residen en un proveedor de libreta de direcciones de host.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Devuelve un objeto table de plantillas de uso único para la creación de los destinatarios que se agregará a la lista de destinatarios de un mensaje saliente.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Prepara una lista de destinatarios para usarlo más adelante mediante el sistema de mensajería.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener información general acerca de los métodos de la interfaz **IABLogon** , vea [Implementación de inicio de sesión de proveedor de servicio](implementing-service-provider-logon.md).
  
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

