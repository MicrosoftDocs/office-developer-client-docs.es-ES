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
ms.openlocfilehash: 0de5bf5d5bb4d8c5606e97bdbc6e70493609a05f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816742"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Hace referencia a**: Outlook 
  
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
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

