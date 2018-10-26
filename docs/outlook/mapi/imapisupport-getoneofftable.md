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
ms.openlocfilehash: d54487928abcc889441ec9bf89ab6a10e5290062
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570838"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Devuelve un puntero a la tabla de uso único de MAPI (una lista de plantillas que todos los libreta de direcciones de proveedores de soporte técnico para la creación de nuevos destinatarios).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de las columnas de cadena. Se puede establecer la marca siguiente:
    
MAPI_UNICODE 
  
> Las columnas de cadena se encuentran en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las columnas de cadena están en formato ANSI.
    
 _lppTable_
  
> [out] Un puntero a un puntero a la tabla de uso único.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> En la tabla de uso único se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::GetOneOffTable** se implementa para objetos de compatibilidad con de proveedor de la libreta de direcciones. Los proveedores de la libreta de direcciones, llame a **GetOneOffTable** para recuperar la lista completa de las plantillas para la creación de nuevos destinatarios. Esta tabla incluye plantillas que admiten los proveedores de la libreta de direcciones que están activos en la sesión, así como plantillas que es compatible con MAPI. 
  
Los destinatarios recién creados se pueden usar para enviar un mensaje o pueden agregarse a un contenedor de la libreta de direcciones.
  
Para obtener una lista de las propiedades que componen la columna requiere establecer en las tablas de uso único, vea [Las tablas de uso único](one-off-tables.md).
  
Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas desde los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) . Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si se ha registrado para recibir notificaciones de los cambios realizados en esta tabla de uso único, también recibirá notificaciones de los cambios realizados en las tablas de uso único de otros proveedores. En función de estas notificaciones, puede admitir nuevos tipos de dirección que se agregan durante la sesión actual.
  
## <a name="see-also"></a>Vea también



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[Propiedad canónico PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Tablas de uso único](one-off-tables.md)

