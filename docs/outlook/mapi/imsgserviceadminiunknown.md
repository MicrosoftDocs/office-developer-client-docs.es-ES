---
title: IMsgServiceAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin
api_type:
- COM
ms.assetid: 5905b9e9-c462-451d-a49f-1f3a8aa506a6
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 21889bf626d7f9128d1e01b3e6a15b5fa0d2e696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817774"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin: IUnknown

  
  
**Se aplica a**: Outlook 
  
Realiza cambios en un servicio de mensajes en un perfil.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MapiX.h  <br/> |
|Expuestos por:  <br/> |Objetos de administración del servicio de mensajes  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMsgServiceAdmin  <br/> |
|Tipo de puntero:  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](imsgserviceadmin-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el último error generado por un objeto de administración del servicio de mensajes.  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |Proporciona acceso a la tabla de servicio de mensajes, una lista de los servicios de mensaje en el perfil.  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |Agrega un servicio de mensajes para el perfil actual.  <br/> <br/>**Nota**: este método está en desuso. Utilice [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) en su lugar.           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |Elimina un servicio de mensajes de un perfil.  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |Copia un servicio de mensajes en un perfil.  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |En desuso. Asigna un nombre nuevo a un servicio de mensajes.  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |Vuelve a configurar un servicio de mensajes.  <br/> |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para aún más el acceso.  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |Establece el orden en que transporte se denominan proveedores para entregar un mensaje.  <br/> |
|[AdminProviders](imsgserviceadmin-adminproviders.md) <br/> |Devuelve un puntero que proporciona acceso a un objeto de administración del proveedor.  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |Designa un servicio de mensajes para ser el proveedor de la identidad principal para el perfil.  <br/> |
|[GetProviderTable](imsgserviceadmin-getprovidertable.md) <br/> |Proporciona acceso a la tabla de proveedor, una lista de los proveedores de servicios en el perfil.  <br/> |
   
## <a name="remarks"></a>Notas

Una implementación puede obtener un puntero a una interfaz **IMsgServiceAdmin** de dos maneras: llamando al método [IMAPISession::AdminServices](imapisession-adminservices.md) o llamando al método [IProfAdmin::AdminServices](iprofadmin-adminservices.md) . Para los clientes que se trate principalmente con la configuración de perfiles, **IProfAdmin::AdminServices** es la mejor forma de obtener la interfaz **IMsgServiceAdmin** , debido a que no se registran en los proveedores de la sesión MAPI. Si un cliente requiere la capacidad de realizar cambios en el perfil activo, se debe llamar **IMAPISession::AdminServices** para obtener el puntero **IMsgServiceAdmin** . Tenga en cuenta que aunque MAPI no permite un perfil que está en uso que se va a eliminar, no hay ningún medidas de seguridad para evitar que a un cliente de quitar todos los servicios de mensaje en el perfil de. 
  
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

