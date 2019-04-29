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
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434602"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe un botón de opción que formará parte de un grupo de botones de opción. El grupo de botones de opción se utilizará en un cuadro de diálogo que se genera a partir de una tabla de presentación.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Posición en la memoria de la etiqueta de la cadena de caracteres para el botón de radio.
    
 **ulFlags**
  
> Máscara de la máscara usada para designar el formato de la etiqueta a la que señala el miembro **ulbLpszLabel** . Se puede establecer la siguiente marca: 
    
MAPI_UNICODE 
  
> La etiqueta está en formato Unicode. Si no se establece la marca MAPI_UNICODE, la etiqueta está en formato ANSI.
    
 **ulcButtons**
  
> Número de botones del grupo de botones de opción. Las estructuras **DTBLRADIOBUTTON** para los demás botones del grupo deben estar incluidas en filas sucesivas de la tabla de presentación. Cada una de estas filas debe contener el mismo valor para el miembro **ulcButtons** . 
    
 **ulPropTag**
  
> Etiqueta de propiedad de una propiedad de tipo PT_LONG. La selección inicial en el grupo de botones de opción se basa en el valor inicial de esta propiedad. Cada botón del grupo debe tener **ulPropTag** establecido en la misma propiedad. 
    
 **lReturnValue**
  
> Número único que identifica el botón seleccionado.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLRADIOBUTTON** describe un botón de opción un control de botón que está asociado a un grupo de botones. Solo se puede comprobar un botón del grupo; la configuración de un botón hace que el resto de los botones del grupo queden inestablecidos. 
  
El recuento de botones es el número de botones de radio del grupo. Las estructuras de los otros botones de radio del grupo deben estar en filas posteriores de la tabla de presentación. Cada una de estas estructuras debe tener el mismo valor para el recuento de botones.
  
Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md). Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Ver también



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[Estructuras MAPI](mapi-structures.md)

