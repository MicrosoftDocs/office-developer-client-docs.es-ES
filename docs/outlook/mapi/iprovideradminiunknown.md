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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 41195a49d1bf3566c81fe6e97697012209cbc5ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817907"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin: IUnknown

  
  
**Se aplica a**: Outlook 
  
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
   
## <a name="remarks"></a>Notas

Los clientes pueden obtener un puntero a una interfaz **IProviderAdmin** llamando al método [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) ; proveedores de servicios se pasan un puntero **IProviderAdmin** cuando se llama a la función de punto de entrada del servicio de sus mensajes. 
  
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

