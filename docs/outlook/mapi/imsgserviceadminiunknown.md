---
title: IUnknown IMsgServiceAdmin
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: aba61d4acf7c1f9a5d91fa15f1ca6b16f173bcb2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309712"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza cambios en un servicio de mensajes en un perfil.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MapiX. h  <br/> |
|Expuesto por:  <br/> |Objetos de administración del servicio de mensajes  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMsgServiceAdmin  <br/> |
|Tipo de puntero:  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Volvió](imsgserviceadmin-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el último error generado por un objeto de administración del servicio de mensajes.  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |Proporciona acceso a la tabla servicio de mensajes, una lista de los servicios de mensajes del perfil.  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |Agrega un servicio de mensajes al perfil actual.  <br/> <br/>**Nota**: este método está en desuso. Use [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) en su lugar.           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |Elimina un servicio de mensajes de un perfil.  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |Copia un servicio de mensajes en un perfil.  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |En desuso. Asigna un nombre nuevo a un servicio de mensajes.  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |Reconfigura un servicio de mensajes.  <br/> |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso.  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |Establece el orden en que se llama a los proveedores de transporte para entregar un mensaje.  <br/> |
|[AdminProviders](imsgserviceadmin-adminproviders.md) <br/> |Devuelve un puntero que proporciona acceso a un objeto de administración del proveedor.  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |Designa un servicio de mensajes para que sea el proveedor de la identidad principal del perfil.  <br/> |
|[GetProviderTable](imsgserviceadmin-getprovidertable.md) <br/> |Proporciona acceso a la tabla de proveedores, una lista de los proveedores de servicios del perfil.  <br/> |
   
## <a name="remarks"></a>Comentarios

Una implementación puede obtener un puntero a una interfaz **IMsgServiceAdmin** de dos maneras: llamando al método [IMAPISession:: AdminServices](imapisession-adminservices.md) o llamando al método [IProfAdmin:: AdminServices](iprofadmin-adminservices.md) . Para los clientes principalmente relacionados con la configuración del perfil, **IProfAdmin:: AdminServices** es la forma preferida de obtener la interfaz de **IMsgServiceAdmin** , porque no inician sesión en los proveedores en la sesión MAPI. Si un cliente necesita poder realizar cambios en el perfil activo, se debe llamar a **IMAPISession:: AdminServices** para obtener el puntero **IMsgServiceAdmin** . Tenga en cuenta que, si bien MAPI no permite la eliminación de un perfil que está en uso, no hay ninguna protección para evitar que un cliente quite todos los servicios de mensajes del perfil. 
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

