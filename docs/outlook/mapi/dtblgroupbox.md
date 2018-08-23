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
ms.openlocfilehash: ef38893c9ad44556cc9220809b5e407f86fd2642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576319"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe un control de cuadro de grupo que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macro relacionado:  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Posición en la memoria de la cadena de caracteres que acompaña al cuadro de grupo. Si aparece, la etiqueta aparece en la parte superior, izquierda del cuadro.
    
 **ulFlags**
  
> Máscara de bits de indicadores que se utilizan para designar el formato de la etiqueta que señala el miembro **ulbLpszLabel** . Se puede establecer la marca siguiente: 
    
MAPI_UNICODE. 
  
> La etiqueta está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., la etiqueta está en formato ANSI.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLGROUPBOX** describe un control de cuadro de grupo que se usa para asociar visualmente otros controles en el cuadro de diálogo. La técnica con resaltado de coincidencias implica que rodea los otros controles por un cuadro. 
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).
  
## <a name="see-also"></a>Recursos adicionales



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

