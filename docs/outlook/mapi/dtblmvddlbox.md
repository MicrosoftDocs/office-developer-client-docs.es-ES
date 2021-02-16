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
ms.openlocfilehash: 33b4fd87f33c26db15e1a6a28f077c393168db91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420748"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una lista desplegable que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.
  
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

## <a name="members"></a>Miembros

 **ulFlags**
  
> Reservado; debe ser cero.
    
 **ulMVPropTag**
  
> Etiqueta de propiedad para una propiedad multivalor de tipo PT_MV_TSTRING. Los diferentes valores de esta propiedad se muestran como entradas distintas en la lista desplegable.
    
## <a name="remarks"></a>Comentarios

Una **estructura DTBLMVDDLBOX** describe una lista desplegable de varios valores, una lista de elementos de solo lectura. Al usar una lista desplegable de varios valores, los valores se muestran cuando un usuario hace clic en una barra de desplazamiento. 
  
Los datos que se muestran proceden de la propiedad identificada en el **miembro ulMVPropTag.** No es necesario leer desde la interfaz de propiedades asociada a la tabla para mostrar. Además, como los usuarios no pueden realizar selecciones de estos tipos de cuadros de lista, los datos no se escriben en la interfaz de propiedades. 
  
Solo se admiten propiedades de cadena de varios valores para la lista desplegable de varios valores; no se admiten otros tipos de propiedades multivalor. 
  
Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md) Para obtener información acerca de cómo implementar una tabla para mostrar, vea [Implementar una tabla para mostrar.](display-table-implementation.md)
  
## <a name="see-also"></a>Consulte también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

