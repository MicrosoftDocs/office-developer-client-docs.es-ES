---
title: MAPI y modelo de objetos componentes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334471"
---
# <a name="component-object-model-and-mapi"></a>MAPI y modelo de objetos componentes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La documentación de Windows SDK incluye una explicación completa de las reglas para implementar objetos que se ajustan al Modelo de objetos componentes (COM). Estas reglas abordan cómo hacer lo siguiente:
  
- Diseñar interfaces y objetos.
    
- Implemente [la interfaz IUnknown.](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) 
    
- Administrar la memoria.
    
- Controlar el recuento de referencias.
    
- Implementar objetos de subprocesos de departamentos.
    
Aunque todos los objetos MAPI se consideran basados en COM porque implementan interfaces que heredan de [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI se desvía en algunas situaciones de las reglas COM estándar. Esta desviación permite a los desarrolladores más flexibilidad en sus implementaciones. Por ejemplo, una interfaz MAPI, como cualquier interfaz COM, describe un contrato entre el implementador y el llamador. Una vez creada y publicada la interfaz, su definición no puede cambiar ni cambia. MAPI no se desvía de esta descripción, pero se desvía un poco la descripción. Los implementadores pueden optar por no implementar métodos concretos, devolviendo uno de los siguientes valores de error al autor de la llamada: 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Las demás desviaciones de las reglas COM estándar se describen en la tabla siguiente.
  
|**Regla de programación COM**|**Variación MAPI**|
|:-----|:-----|
|Todos los parámetros de cadena de los métodos de interfaz deben ser Unicode.  <br/> |Las interfaces MAPI se definen para permitir parámetros de cadena Unicode o ANSI. Muchos métodos que tienen un parámetro de cadena también tienen un **parámetro ulFlags;** el ancho de un parámetro de cadena se indica mediante el valor de la marca MAPI_UNICODE en **ulFlags**. Algunas interfaces MAPI no admiten Unicode y devuelven MAPI_E_BAD_CHARWIDTH cuando se establece MAPI_UNICODE marca.  <br/> |
|Todos los métodos de interfaz deben tener un tipo devuelto de HRESULT.  <br/> |MAPI tiene al menos un método que devuelve un valor que no es HRESULT: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).  <br/> |
|Los autores de llamadas y los implementadores deben asignar y liberar memoria para los parámetros de interfaz mediante el uso de los asignadores de tareas COM estándar.  <br/> |Todos los métodos MAPI usan los asignadores [vinculados MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md) para administrar la memoria de los parámetros de interfaz. Todas las implementaciones MAPI de interfaces definidas por OLE, como [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), usan los asignadores de tareas COM estándar.  <br/> |
|Todos los parámetros de puntero de salida deben establecerse explícitamente en NULL cuando se produce un error en un método.  <br/> |Las interfaces MAPI requieren que los parámetros de puntero de salida se establezcan en NULL o no se cambien cuando se produce un error en un método. Todas las implementaciones MAPI de interfaces definidas por OLE establecen explícitamente parámetros en NULL en caso de error.  <br/> |
|Implemente objetos agregables siempre que sea posible.  <br/> |Las interfaces MAPI no se pueden agregar.  <br/> |
   
## <a name="see-also"></a>Consulte también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Información general sobre el objeto MAPI y la interfaz](mapi-object-and-interface-overview.md)

