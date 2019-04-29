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
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410689"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una etiqueta que se utilizará en un cuadro de diálogo que se genera a partir de una tabla de presentación.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Macro relacionada  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Members

 **ulbLpszLabelName**
  
> Posición en la memoria de la etiqueta de la cadena de caracteres.
    
 **ulFlags**
  
> Máscara de la máscara usada para designar el formato de la etiqueta a la que señala el miembro **ulbLpszLabelName** . Se puede establecer la siguiente marca: 
    
MAPI_UNICODE 
  
> La etiqueta está en formato Unicode. Si no se establece la marca MAPI_UNICODE, la etiqueta está en formato ANSI.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLLABEL** describe un texto de control de etiqueta que se muestra con otro tipo de control para agregar significado a ese control. Por ejemplo, la mayoría de los controles de edición se colocan junto a las etiquetas para informar al usuario del tipo de información que se va a especificar. Algunos controles, como cuadros de grupo y botones de opción, contienen sus propias etiquetas. 
  
La etiqueta puede incluir un acelerador de Windows, identificado como el carácter que sigue&amp;a la y comercial (). Si se presiona la tecla de método abreviado, el foco se sitúa en el primer control que no sea una etiqueta y que no esté situado a continuación de esta etiqueta de la tabla de presentación.
  
No se admiten etiquetas de varias líneas. Mostrar varias líneas requiere varias etiquetas.
  
No se puede usar una etiqueta como control de edición de sólo lectura. La diferencia es que un control de edición se puede seleccionar y copiar mientras que una etiqueta no puede. 
  
Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md). Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Ver también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

