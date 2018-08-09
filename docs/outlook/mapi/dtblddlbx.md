---
title: DTBLDDLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2db95697cd98e66da9fb3d0cd0180b238c0a8dff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816725"
---
# <a name="dtblddlbx"></a>DTBLDDLBX

  
  
**Hace referencia a**: Outlook 
  
Describe un control de lista desplegable que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a>Members

 **ulFlags**
  
> Reservado, debe ser cero. 
    
 **ulPRDisplayProperty**
  
> Etiqueta de propiedad de una propiedad de tipo PT_TSTRING. Esta propiedad es una de las columnas en la tabla identificada por el miembro **ulPRTableName** . Los valores de esta propiedad se muestran en la lista. 
    
 **ulPRSetProperty**
  
> Etiqueta de propiedad de una propiedad de cualquier tipo. Esta propiedad es una de las columnas en la tabla identificada por el miembro **ulPRTableName** . Cuando el usuario de la lista, selecciona un valor de propiedad para el miembro **ulPRDisplayProperty** de las filas de la tabla identificada por el miembro **ulPRTableName** , se establece el miembro **ulPRSetProperty** correspondiente. 
    
 **ulPRTableName**
  
> Etiqueta de la propiedad para una propiedad de tabla de tipo pt Object que se pueden abrir mediante el uso de un **OpenProperty** llamar. La tabla debe tener dos columnas: **ulPRDisplayProperty** y **ulPRSetProperty**. Las filas de la tabla deben corresponden a elementos de la lista.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLDDLBX** describe un control de lista desplegable que se muestra como un solo elemento hasta que el usuario elige para expandirla. 
  
Las tres propiedades identificadas por las etiquetas de propiedad funcionan conjuntamente para mostrar la información en la lista y establecer una propiedad relacionada. El miembro **ulPRTableName** es un objeto table que se tiene acceso a través de una llamada a [IMAPIProp::OpenProperty](imapiprop-openproperty.md). La tabla tiene dos columnas: una columna para la propiedad identificada por el miembro **ulPRDisplayProperty** y otro para la propiedad identificada por el miembro **ulPRSetProperty** . 
  
La propiedad **ulPRDisplayProperty** unidades de la visualización de la lista. Cuando un usuario selecciona uno de los valores de la presentación, MAPI llama a [IMAPIProp::SetProps](imapiprop-setprops.md) para establecer la propiedad correspondiente que se identifican por el miembro **ulPRSetProperty** . Esto significa la propiedad en la misma fila que la propiedad para mostrar seleccionado. No se puede establecer el miembro **ulPRSetProperty** para **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
  
Un valor inicial se muestra en la lista si se ha recuperado la propiedad representada por el miembro **ulPRSetProperty** a través de una llamada a [IMAPIProp::GetProps](imapiprop-getprops.md) y se encuentra una fila en la tabla con el valor para el miembro **ulPRSetProperty** MAPI. El valor inicial mostrado es el contenido de la columna **ulPRDisplayProperty** de esa fila que coincida con la propiedad en el miembro **ulPRDisplayProperty** de la estructura. El valor devuelto por **GetProps** para la propiedad identificada por el miembro **ulPRDisplayProperty** se convierte en el valor inicial que se muestra cuando se muestra en primer lugar la lista. 
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md). Para obtener información acerca de los tipos de propiedad, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[Estructuras MAPI](mapi-structures.md)
  
[Implementación de la tabla para mostrar](display-table-implementation.md)
  
[Tablas para mostrar](display-tables.md)
  
[Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md)

