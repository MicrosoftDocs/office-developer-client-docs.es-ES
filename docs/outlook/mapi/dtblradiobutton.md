---
title: DTBLRADIOBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dee12ba9da83d2167afe13d00270a900bf0d73d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816743"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**Hace referencia a**: Outlook 
  
Describe un botón de opción que formará parte de un grupo de botones de radio. Se usará el grupo de botones de radio en un cuadro de diálogo que se genera a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLRADIOBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulcButtons;
  ULONG ulPropTag;
  long lReturnValue;
} DTBLRADIOBUTTON, FAR *LPDTBLRADIOBUTTON;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Posición en la memoria de la etiqueta de cadena de caracteres para el botón de opción.
    
 **ulFlags**
  
> Máscara de bits de indicadores que se utilizan para designar el formato de la etiqueta que señala el miembro **ulbLpszLabel** . Se puede establecer la marca siguiente: 
    
MAPI_UNICODE. 
  
> La etiqueta está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., la etiqueta está en formato ANSI.
    
 **ulcButtons**
  
> Recuento de botones en el grupo de botones de radio. Las estructuras **DTBLRADIOBUTTON** para los otros botones en el grupo deben estar incluidas en las filas sucesivas de la tabla para mostrar. Cada una de estas filas debe contener el mismo valor para el miembro **ulcButtons** . 
    
 **ulPropTag**
  
> Etiqueta de propiedad de una propiedad de tipo PT_LONG. La selección inicial en el grupo de botones de radio se basa en el valor inicial de esta propiedad. Cada botón en el grupo debe tener **ulPropTag** establecida en la misma propiedad. 
    
 **lReturnValue**
  
> Número único que identifica el botón seleccionado.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLRADIOBUTTON** describe un botón de opción de un control de botón que está asociado a un grupo de botones. Sólo un botón en el grupo se puede proteger; establecer un botón hace que el resto de los botones en el grupo al que se va a anular. 
  
El recuento de botón es el número de botones de opción en el grupo. Las estructuras de los otros botones de opción en el grupo deben ser en filas posteriores en la tabla para mostrar. Cada una de estas estructuras debe tener el mismo valor para su número de botones.
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).
  
## <a name="see-also"></a>Vea también



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[Estructuras MAPI](mapi-structures.md)

