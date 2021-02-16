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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431900"
---
# <a name="imapiformadvisesinkonchange"></a>IMAPIFormAdviseSink::OnChange

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica que se ha producido un cambio en el estado del visor de formularios. 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a>Parámetros

 _ulDir_
  
> [entrada] Máscara de bits de marcas que proporciona información sobre el cambio que se ha producido en el visor y la respuesta esperada en el formulario. Se pueden establecer las siguientes marcas:
    
VCSTATUS_CATEGORY 
  
> Hay un mensaje siguiente o anterior en otra categoría. 
    
VCSTATUS_INTERACTIVE 
  
> El formulario debe mostrar una interfaz de usuario. Si no se establece esta marca, el formulario debería suprimir la visualización de una interfaz de usuario, incluso en respuesta a un verbo que normalmente hace que se muestre una interfaz de usuario. 
    
VCSTATUS_MODAL 
  
> El formulario debe ser modal para el visor del formulario. 
    
VCSTATUS_NEXT 
  
> Hay un siguiente mensaje en el visor de formularios. 
    
VCSTATUS_PREV 
  
> Hay un mensaje anterior en el visor de formularios. 
    
VCSTATUS_READONLY 
  
> Las operaciones de eliminación, envío y movimiento deben deshabilitarse. 
    
VCSTATUS_UNREAD 
  
> Hay un mensaje no leído siguiente o anterior en el visor de formularios.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se ha realizado correctamente.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormAdviseSink::OnChange** para notificar al formulario sobre un cambio en el estado de un visor. Normalmente, el único cambio es establecer o borrar la marca VCSTATUS_NEXT o VCSTATUS_PREVIOUS en función de la presencia o ausencia de un mensaje siguiente o anterior en el visor. En consecuencia, el objeto de formulario habilita o deshabilita las acciones siguientes o anteriores que admita. 
  
La configuración de VCSTATUS_MODAL y VCSTATUS_INTERACTIVE no pueden cambiar en un contexto de vista después de su creación.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La implementación específica de este método depende completamente de los detalles del formulario. La mayoría de los objetos de formulario usan este método para cambiar su interfaz de usuario (por ejemplo, para habilitar o deshabilitar comandos de menú o botones para que coincidan con el parámetro de indicadores de estado del visor).
  
## <a name="see-also"></a>Consulte también



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)

