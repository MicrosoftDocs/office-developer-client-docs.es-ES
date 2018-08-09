---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 28f6471f74fb0fcc4f7e2f4114f0790e1564e17e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816741"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**Hace referencia a**: Outlook 
  
Describe una etiqueta que se usará en un cuadro de diálogo que se genera a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macro relacionado  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Members

 **ulbLpszLabelName**
  
> Posición en la memoria de la etiqueta de cadena de caracteres.
    
 **ulFlags**
  
> Máscara de bits de indicadores que se utilizan para designar el formato de la etiqueta que señala el miembro **ulbLpszLabelName** . Se puede establecer la marca siguiente: 
    
MAPI_UNICODE. 
  
> La etiqueta está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., la etiqueta está en formato ANSI.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLLABEL** describe un texto de control de etiqueta que se muestra con otro tipo de control que se va a agregar significado a ese control. Por ejemplo, la mayoría de los controles de edición se coloca junto a las etiquetas para informar al usuario del tipo de información que debe escribirse. Algunos controles, como cuadros de grupo y los botones de radio, mantenga sus propias etiquetas. 
  
La etiqueta puede incluir un acelerador de Windows, identificado como el carácter que sigue la y comercial (&amp;). Al presionar la tecla de aceleración coloca el foco en el primer nonlabel, control de nonbutton seguir esta etiqueta en la tabla para mostrar.
  
No hay ninguna compatibilidad para las etiquetas de varias líneas. Mostrar varias líneas requiere varias etiquetas.
  
No es posible utilizar una etiqueta como un control de edición de sólo lectura. La diferencia es que un control de edición se puede seleccionar y copiar mientras que una etiqueta no se puede. 
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

