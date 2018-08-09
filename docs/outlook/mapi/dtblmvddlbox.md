---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ede0a448a32565446e614fc2d14f2a72a9549dad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816744"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**Hace referencia a**: Outlook 
  
Describe una lista desplegable que se usará en un cuadro de diálogo que se genera a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a>Members

 **ulFlags**
  
> Reservado; debe ser cero.
    
 **ulMVPropTag**
  
> Etiqueta de propiedad de una propiedad con varios valores de tipo PT_MV_TSTRING. Se muestran los distintos valores de esta propiedad como distintas entradas en la lista desplegable.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLMVDDLBOX** describe una lista desplegable multivalor una lista de solo lectura de elementos. Mediante el uso de una lista desplegable con múltiples valores, los valores se muestran cuando un usuario hace clic en una barra de desplazamiento. 
  
Los datos que se muestran proceden de la propiedad identificada en el miembro **ulMVPropTag** . No hay ningún requisito para leer desde la interfaz de propiedad que está asociada a la tabla para mostrar. Además, debido a que los usuarios no son puedan realizar selecciones de estos tipos de cuadros de lista, datos no se escriben en la interfaz (propiedad). 
  
Propiedades de cadena multivalor sólo son compatibles con la lista desplegable multivalor; otros tipos de propiedad de varios valores no son compatibles. 
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

