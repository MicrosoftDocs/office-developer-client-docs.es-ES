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
ms.openlocfilehash: 244aaea4902d6be8eda4cdca176436af9b002ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438851"
---
# <a name="dtblddlbx"></a>DTBLDDLBX

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Miembros

 **ulFlags**
  
> Reservado, debe ser cero. 
    
 **ulPRDisplayProperty**
  
> Etiqueta de propiedad para una propiedad de tipo PT_TSTRING. Esta propiedad es una de las columnas de la tabla identificadas por el **miembro ulPRTableName.** Los valores de esta propiedad se muestran en la lista. 
    
 **ulPRSetProperty**
  
> Etiqueta de propiedad para una propiedad de cualquier tipo. Esta propiedad es una de las columnas de la tabla identificadas por el **miembro ulPRTableName.** Cuando el usuario de la lista selecciona un valor de propiedad para el miembro **ulPRDisplayProperty** de las filas de la tabla identificadas por el **miembro ulPRTableName,** se establece el miembro **ulPRSetProperty** correspondiente. 
    
 **ulPRTableName**
  
> Etiqueta de propiedad para una propiedad table de tipo PT_OBJECT que se puede abrir mediante una **llamada OpenProperty.** La tabla debe tener dos columnas: **ulPRDisplayProperty** y **ulPRSetProperty**. Las filas de la tabla deben corresponder a los elementos de la lista.
    
## <a name="remarks"></a>Comentarios

Una **estructura DTBLDDLBX** describe un control de lista desplegable que se muestra como un único elemento hasta que el usuario decide expandirlo. 
  
Las tres propiedades identificadas por las etiquetas de propiedad funcionan juntas para mostrar la información en la lista y establecer una propiedad relacionada. El **miembro ulPRTableName** es un objeto table al que se tiene acceso a través de una llamada a [IMAPIProp::OpenProperty](imapiprop-openproperty.md). La tabla tiene dos columnas: una columna para la propiedad identificada por el miembro **ulPRDisplayProperty** y la otra para la propiedad identificada por el **miembro ulPRSetProperty.** 
  
La **propiedad ulPRDisplayProperty** dirige la presentación de la lista. Cuando un usuario selecciona uno de los valores de la pantalla, MAPI llama a [IMAPIProp::SetProps](imapiprop-setprops.md) para establecer la propiedad correspondiente tal como la identificó el **miembro ulPRSetProperty.** Esto significa que la propiedad en la misma fila que la propiedad para mostrar seleccionada. El **miembro ulPRSetProperty** no se puede **establecer en PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
  
Un valor inicial se muestra en la lista si MAPI ha recuperado la propiedad representada por el miembro **ulPRSetProperty** a través de una llamada a [IMAPIProp::GetProps](imapiprop-getprops.md) y se encuentra una fila en la tabla con el valor del **miembro ulPRSetProperty.** El valor mostrado inicial es el contenido de la columna **ulPRDisplayProperty** de esa fila que coincide con la propiedad del **miembro ulPRDisplayProperty** de la estructura. El valor devuelto por **GetProps** para la propiedad identificada por el **miembro ulPRDisplayProperty** se convierte en el valor inicial que se muestra cuando se muestra la lista por primera vez. 
  
Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md) Para obtener información sobre cómo implementar una tabla para mostrar, vea [Implementing a Display Table](display-table-implementation.md). Para obtener información acerca de los tipos de propiedad, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[Estructuras MAPI](mapi-structures.md)
  
[Implementación de tabla para mostrar](display-table-implementation.md)
  
[Tablas para mostrar](display-tables.md)
  
[Información general del tipo de propiedad MAPI](mapi-property-type-overview.md)

