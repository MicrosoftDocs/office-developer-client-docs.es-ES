---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 02663570e3173bbd696af732e71f060d9dee49bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286631"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica que se ha producido un cambio en el estado del visor de formularios. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Parameters

 _ulDir_
  
> a Máscara de máscara de marcadores que proporciona información sobre el cambio que se ha producido en el visor y la respuesta esperada en el formulario. Se pueden establecer los siguientes indicadores:
    
VCSTATUS_CATEGORY 
  
> Hay un mensaje siguiente o anterior en otra categoría. 
    
VCSTATUS_INTERACTIVE 
  
> El formulario debe mostrar una interfaz de usuario. Si no se establece esta marca, el formulario debe suprimir la visualización de una interfaz de usuario, incluso en respuesta a un verbo que normalmente hace que se muestre una interfaz de usuario. 
    
VCSTATUS_MODAL 
  
> El formulario es modal para el visor de formulario. 
    
VCSTATUS_NEXT 
  
> Hay un mensaje siguiente en el visor de formularios. 
    
VCSTATUS_PREV 
  
> Hay un mensaje anterior en el visor de formularios. 
    
VCSTATUS_READONLY 
  
> Las operaciones de eliminar, enviar y mover deben estar deshabilitadas. 
    
VCSTATUS_UNREAD 
  
> Hay un mensaje no leído siguiente o anterior en el visor de formularios.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se realizó correctamente.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormAdviseSink:: onchange** para notificar al formulario sobre un cambio en el estado de un visor. Normalmente, el único cambio consiste en establecer o borrar la marca VCSTATUS_NEXT o VCSTATUS_PREVIOUS en función de la presencia o ausencia de un mensaje siguiente o anterior en el visor. Por lo tanto, el objeto Form habilita o deshabilita cualquier acción siguiente o anterior que admita. 
  
La configuración de VCSTATUS_MODAL y VCSTATUS_INTERACTIVE no puede cambiar en un contexto de vista una vez que se ha creado.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La implementación específica de este método depende completamente de los detalles del formulario. La mayoría de los objetos Form utilizan este método para cambiar la interfaz de usuario (por ejemplo, para habilitar o deshabilitar los comandos de menú o los botones para que correspondan con el parámetro de indicadores de estado del visor).
  
## <a name="see-also"></a>Vea también



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

