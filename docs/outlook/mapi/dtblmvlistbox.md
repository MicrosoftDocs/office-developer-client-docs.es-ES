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
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439705"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una lista con varios valores que se mostrará en un cuadro de diálogo que se genera a partir de una tabla de presentación.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>Miembros

 **ulFlags**
  
> Reserve debe ser cero.
    
 **ulMVPropTag**
  
> Etiqueta de propiedad de una propiedad de varios valores de tipo PT_MV_TSTRING.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLMVLISTBOX** describe una lista estándar con varios valores que tiene una lista de solo lectura de elementos. Mediante el uso de una lista estándar de varios valores, los valores se muestran inmediatamente. 
  
Los datos que se muestran provienen de la propiedad identificada en el miembro **ulMVPropTag** . No es necesario leer de la interfaz de propiedades asociada a la tabla de visualización. Además, dado que los usuarios no pueden realizar selecciones de estos tipos de listas, los datos no se escriben en la interfaz de propiedades. 
  
Solo se admiten propiedades de cadena de varios valores para la lista de varios valores; no se admiten otros tipos de propiedades con varios valores. 
  
Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md). Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Ver también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

