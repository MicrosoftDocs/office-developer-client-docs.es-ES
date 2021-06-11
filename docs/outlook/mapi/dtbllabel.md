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
  
Describe una etiqueta que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
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
  
> Posición en la memoria de la etiqueta de cadena de caracteres.
    
 **ulFlags**
  
> Máscara de bits de las marcas usadas para designar el formato de la etiqueta a la que apunta el **miembro ulbLpszLabelName.** Se puede establecer la siguiente marca: 
    
MAPI_UNICODE 
  
> La etiqueta está en formato Unicode. Si la MAPI_UNICODE no está establecida, la etiqueta está en formato ANSI.
    
## <a name="remarks"></a>Comentarios

Una **estructura DTBLLABEL** describe un texto de control de etiqueta que se muestra con otro tipo de control para agregar significado a ese control. Por ejemplo, la mayoría de los controles de edición se sitúan junto a las etiquetas para informar al usuario del tipo de información que se va a especificar. Algunos controles, como cuadros de grupo y botones de radio, tienen sus propias etiquetas. 
  
La etiqueta puede incluir un acelerador Windows, identificado como el carácter que sigue a la ampersand ( &amp; ). Al presionar la tecla de aceleración, se coloca el foco en el primer control sin etiqueta y sin botón que sigue a esta etiqueta en la tabla para mostrar.
  
No hay compatibilidad con etiquetas de varias líneas. Mostrar varias líneas requiere varias etiquetas.
  
No es posible usar una etiqueta como control de edición de solo lectura. La diferencia es que un control de edición se puede seleccionar y copiar mientras que una etiqueta no puede. 
  
Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md) Para obtener información sobre cómo implementar una tabla para mostrar, vea [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

