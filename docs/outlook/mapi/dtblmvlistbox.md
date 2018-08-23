---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f7c1241f2ad31dee8277f3b3b77ac02137067a12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576312"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una lista de varios valores que se mostrará en un cuadro de diálogo que se genera a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>Members

 **ulFlags**
  
> Reservado; debe ser cero.
    
 **ulMVPropTag**
  
> Etiqueta de propiedad de una propiedad con varios valores de tipo PT_MV_TSTRING.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLMVLISTBOX** describe una lista de varios valores estándar que tiene una lista de solo lectura de elementos. Mediante el uso de una lista de varios valores estándar, los valores se muestran inmediatamente. 
  
Los datos que se muestran proceden de la propiedad identificada en el miembro **ulMVPropTag** . No hay ningún requisito para leer desde la interfaz de propiedad que está asociada a la tabla para mostrar. Además, debido a que los usuarios no son puedan realizar selecciones de estos tipos de listas, datos no se escriben en la interfaz (propiedad). 
  
Propiedades de cadena multivalor sólo son compatibles con la lista de varios valores; otros tipos de propiedad de varios valores no son compatibles. 
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).
  
## <a name="see-also"></a>Recursos adicionales



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

