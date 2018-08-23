---
title: IProviderAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 559680b9ca4ea5be85718d8f9692df93f77b0edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585755"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Funciona con proveedores de servicios en un servicio de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Objetos de administración del proveedor  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IProviderAdmin  <br/> |
|Tipo de puntero:  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](iprovideradmin-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjeron en el objeto de administración del proveedor.  <br/> |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |Proporciona acceso a la tabla de proveedor del servicio de mensajes, una lista de los proveedores de servicios en el servicio de mensajes.  <br/> |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |Agrega un proveedor de servicios para el servicio de mensajes.  <br/> |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |Elimina un proveedor de servicios desde el servicio de mensajes.  <br/> |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |Abre una sección de perfil desde el perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para aún más el acceso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los clientes pueden obtener un puntero a una interfaz **IProviderAdmin** llamando al método [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) ; proveedores de servicios se pasan un puntero **IProviderAdmin** cuando se llama a la función de punto de entrada del servicio de sus mensajes. 
  
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

