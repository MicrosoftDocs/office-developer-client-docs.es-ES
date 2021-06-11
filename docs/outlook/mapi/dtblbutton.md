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
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412789"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene información sobre un control de botón para un cuadro de diálogo creado a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macro relacionada:  <br/> |[SizedDtblButton](sizeddtblbutton.md) <br/> |
   
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
  
> Máscara de bits de las marcas usadas para designar el formato de la etiqueta señalada por el **miembro ulbLpszLabel.** Se puede establecer la siguiente marca: 
    
MAPI_UNICODE 
  
> La etiqueta está en formato Unicode. Si la MAPI_UNICODE no está establecida, la etiqueta está en formato ANSI.
    
 **ulPRControl**
  
> Etiqueta de propiedad para una propiedad de tipo PT_OBJECT que implementa la [interfaz IMAPIControl.](imapicontroliunknown.md) Cuando se hace clic en el botón, MAPI llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para que la implementación [IMAPIProp](imapipropiunknown.md) de la tabla para mostrar recupere esta propiedad. 
    
## <a name="remarks"></a>Comentarios

Una **estructura DTBLBUTTON** describe un botón un control que, al hacer clic, permite al usuario iniciar una operación. Normalmente, al hacer clic en un botón, se muestra un cuadro de diálogo modal o se invoca una tarea mediante programación. Los proveedores de servicios pueden implementar cualquier cosa a través de un control de botón. Si se supone que el botón debe realizar una tarea en función de los valores de otros controles, estos controles deben haber establecido la marca DT_SET_IMMEDIATE. 
  
El **miembro ulbLpszLabel** es la posición en la memoria de la cadena de caracteres que se muestra en el botón. Los proveedores de servicios pueden agregar un carácter de yerba ( ) para indicar &amp; un Windows acelerador en la etiqueta del botón. Presionar una tecla de aceleración tiene el mismo efecto que hacer clic en el botón. 
  
El **miembro ulPRControl** describe una propiedad de objeto que, cuando se abre con el método **IMAPIProp::OpenProperty,** devuelve un puntero a un objeto de control. La implementación de un objeto de control compatible con la interfaz **IMAPIControl** es una forma de ampliar el conjunto de características MAPI y definir la operación o tarea que se produce cuando se hace clic en el botón. **IMAPIControl proporciona** dos métodos para manipular botones: [GetState](imapicontrol-getstate.md) para deshabilitar o habilitar botones y [Activar](imapicontrol-activate.md) para controlar los clics de botón. 
  
Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md) Para obtener información sobre cómo implementar una tabla para mostrar, vea [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

