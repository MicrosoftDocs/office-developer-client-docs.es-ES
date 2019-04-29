---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 324cfe9d7c412b3bb0e3150b8eec51aaeb6a0e93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438396"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe un control de cuadro de grupo que se utilizará en un cuadro de diálogo generado a partir de una tabla de presentación.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Macro relacionada:  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Posición en la memoria de la cadena de caracteres que acompaña al cuadro de grupo. Si se muestra, la etiqueta aparece en la parte superior izquierda del cuadro.
    
 **ulFlags**
  
> Máscara de la máscara usada para designar el formato de la etiqueta a la que señala el miembro **ulbLpszLabel** . Se puede establecer la siguiente marca: 
    
MAPI_UNICODE 
  
> La etiqueta está en formato Unicode. Si no se establece la marca MAPI_UNICODE, la etiqueta está en formato ANSI.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLGROUPBOX** describe un control de cuadro de grupo que se usa para asociar visualmente otros controles en el cuadro de diálogo. La técnica de resaltado implica rodear los demás controles por un cuadro. 
  
Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md). Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Ver también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

