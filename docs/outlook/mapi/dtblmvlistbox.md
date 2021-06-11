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
  
Describe una lista de varios valores que se mostrará en un cuadro de diálogo creado a partir de una tabla para mostrar.
  
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

## <a name="members"></a>Miembros

 **ulFlags**
  
> Reservado; debe ser cero.
    
 **ulMVPropTag**
  
> Etiqueta de propiedad para una propiedad multivalor de tipo PT_MV_TSTRING.
    
## <a name="remarks"></a>Comentarios

Una **estructura DTBLMVLISTBOX** describe una lista estándar de varios valores que tiene una lista de elementos de solo lectura. Al usar una lista multivalor estándar, los valores se muestran inmediatamente. 
  
Los datos que se muestran proceden de la propiedad identificada en el **miembro ulMVPropTag.** No hay ningún requisito para leer desde la interfaz de propiedades asociada a la tabla para mostrar. Además, como los usuarios no pueden realizar selecciones de estos tipos de listas, los datos no se escriben en la interfaz de propiedades. 
  
Solo se admiten propiedades de cadena de varios valores para la lista de varios valores; no se admiten otros tipos de propiedades multivalor. 
  
Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md) Para obtener información sobre cómo implementar una tabla para mostrar, vea [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

