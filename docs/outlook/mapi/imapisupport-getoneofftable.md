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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412761"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un puntero a la tabla de uso único mapi (una lista de plantillas que todos los proveedores de libretas de direcciones admiten para crear nuevos destinatarios).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla el tipo de las columnas de cadena. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las columnas de cadena están en formato Unicode. Si no MAPI_UNICODE marca, las columnas de cadena están en formato ANSI.
    
 _lppTable_
  
> [salida] Puntero a un puntero a la tabla de un solo acceso.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de un solo juego se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::GetOneOffTable** se implementa para objetos de compatibilidad del proveedor de libreta de direcciones. Los proveedores de libretas de direcciones **llaman a GetOneOffTable** para recuperar la lista completa de plantillas para crear nuevos destinatarios. Esta tabla incluye plantillas que abordan proveedores de libretas que están activos en la compatibilidad con sesiones, así como plantillas compatibles con MAPI. 
  
Los destinatarios recién creados se pueden usar para dirigir un mensaje o se pueden agregar a un contenedor de libreta de direcciones.
  
Para obtener una lista de las propiedades que forma la columna necesaria establecida en tablas de uso único, vea [Tablas de uso único.](one-off-tables.md)
  
Establecer el MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas de los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md) Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si está registrado para recibir notificaciones de cambios en esta tabla de uso único, también recibirá notificaciones de cambios en las tablas de uso único de otros proveedores. En función de estas notificaciones, puede admitir nuevos tipos de direcciones que se agregan durante la sesión actual.
  
## <a name="see-also"></a>Consulte también



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[Propiedad canónica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Tablas de un solo usuario](one-off-tables.md)

