---
title: IUnknown IProviderAdmin
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
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315529"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Trabaja con proveedores de servicios en un servicio de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Expuesto por:  <br/> |Objetos de administración del proveedor  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IProviderAdmin  <br/> |
|Tipo de puntero:  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Volvió](iprovideradmin-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjo en el objeto de administración del proveedor.  <br/> |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |Proporciona acceso a la tabla de proveedores del servicio de mensajes, una lista de los proveedores de servicios del servicio de mensajes.  <br/> |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |Agrega un proveedor de servicios al servicio de mensajes.  <br/> |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |Elimina un proveedor de servicios del servicio de mensajes.  <br/> |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |Abre una sección de perfil desde el perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los clientes pueden obtener un puntero a una interfaz **IProviderAdmin** llamando al método [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md) ; a los proveedores de servicios se les pasa un puntero **IProviderAdmin** cuando se llama a la función de punto de entrada del servicio de mensajes. 
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

