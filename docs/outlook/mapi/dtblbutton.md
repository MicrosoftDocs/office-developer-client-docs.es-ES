---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e0797364eb4ec24793f64bad2f4d838507c236e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571069"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene información sobre un control de botón para un cuadro de diálogo creado a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macro relacionado:  <br/> |[SizedDtblButton](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Posición en la memoria de la cadena de caracteres que se muestra en el botón.
    
 **ulFlags**
  
> Máscara de bits de indicadores que se utilizan para designar el formato de la etiqueta que señala el miembro **ulbLpszLabel** . Se puede establecer la marca siguiente: 
    
MAPI_UNICODE. 
  
> La etiqueta está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., la etiqueta está en formato ANSI.
    
 **ulPRControl**
  
> Etiqueta de propiedad de una propiedad de tipo pt Object que implementa la interfaz [IMAPIControl](imapicontroliunknown.md) . Cuando se hace clic en el botón, MAPI llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para la implementación de [IMAPIProp](imapipropiunknown.md) de la tabla para mostrar recuperar esta propiedad. 
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLBUTTON** describe un botón de un control que, al hacer clic, permite que un usuario comenzar una operación. Normalmente, al hacer clic en un botón hace que un cuadro de diálogo modal que se mostrará o una tarea de programación va a invocar. Proveedores de servicios pueden implementar algo a través de un control de botón. Si se supone que el botón para realizar una tarea en función de los valores de otros controles, dichos controles deben ha establecido el indicador DT_SET_IMMEDIATE. 
  
El miembro **ulbLpszLabel** es la posición en la memoria de la cadena de caracteres que se muestra en el botón. Proveedores de servicios pueden agregar un carácter de y comercial (&amp;) para indicar un acelerador de Windows en la etiqueta del botón. Al presionar una tecla de aceleración tiene el mismo efecto que hacer clic en el botón. 
  
El miembro **ulPRControl** describe una propiedad de objeto que, cuando se abre con el método **IMAPIProp::OpenProperty** , devuelve un puntero a un objeto de control. Implementación de un objeto de control que admite la interfaz **IMAPIControl** es una forma de extender el conjunto de características MAPI y definir la operación o una tarea que se produce cuando se hace clic en el botón. **IMAPIControl** proporciona dos métodos para manipular los botones: [GetState](imapicontrol-getstate.md) para deshabilitar o habilitar los botones y [Activar](imapicontrol-activate.md) para controlar los clics de botón. 
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).
  
## <a name="see-also"></a>Recursos adicionales



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

