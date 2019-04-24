---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c0beec8a0b234794d3f623c4ceac773db698dd79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316579"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un puntero a la tabla única de MAPI (una lista de plantillas que todos los proveedores de la libreta de direcciones admiten para crear nuevos destinatarios).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que controla el tipo de las columnas de cadena. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las columnas de cadena están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las columnas de la cadena tienen formato ANSI.
    
 _lppTable_
  
> contempla Un puntero a un puntero a la tabla de un solo uso.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de uso único se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: GetOneOffTable** se implementa para los objetos de compatibilidad del proveedor de la libreta de direcciones. Los proveedores de la libreta de direcciones llaman a **GetOneOffTable** para recuperar la lista completa de plantillas para crear nuevos destinatarios. En esta tabla se incluyen plantillas que admiten proveedores de libretas de direcciones activos en la compatibilidad con sesiones, así como plantillas admitidas por MAPI. 
  
Los destinatarios recién creados pueden usarse para dirigir un mensaje o pueden agregarse a un contenedor de libretas de direcciones.
  
Para obtener una lista de las propiedades que conforman el conjunto de columnas necesario en las tablas de uso único, consulte [tablas de uso único](one-off-tables.md).
  
La configuración de la marca MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas que se devuelven desde los métodos [IMAPITable:: QueryColumns](imapitable-querycolumns.md) y [IMAPITable:: QueryRows](imapitable-queryrows.md) . Esta marca también controla los tipos de propiedades en el criterio de ordenación devueltos por el método [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si está registrado para recibir notificaciones de cambios en esta tabla única, también recibirá notificaciones de los cambios realizados en las tablas de un solo uso de los proveedores. En función de estas notificaciones, puede admitir nuevos tipos de direcciones que se agregan durante la sesión actual.
  
## <a name="see-also"></a>Vea también



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[Propiedad canónica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Tablas de un solo uso](one-off-tables.md)

