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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394121"
---
# <a name="component-object-model-and-mapi"></a>MAPI y modelo de objetos componentes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
La documentación del SDK de Windows incluye una explicación completa de las reglas para la implementación de objetos que se ajustan al modelo de objetos componentes (COM). Estas reglas de direcciones cómo hacer lo siguiente:
  
- Interfaces de diseño y objetos.
    
- Implementar la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) . 
    
- Administrar la memoria.
    
- Controlar el recuento de referencia.
    
- Implementar objetos de subprocesamiento controlado.
    
Si bien todos los objetos MAPI se consideran basada en COM porque implementan las interfaces que heredan de [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI se desvía en algunas situaciones de las reglas de COM estándar. Este desviación permite a los programadores más flexibilidad en sus implementaciones. Por ejemplo, una interfaz de MAPI, al igual que cualquier interfaz COM, describe un contrato entre implementador y autor de la llamada. Una vez que la interfaz se ha creado y publicada, su definición no se puede y no cambia. MAPI no se desvían de esta descripción, pero algo modera la descripción. Los implementadores pueden optar por no implementar métodos concretos, devolver uno de los siguientes valores de error al autor de la llamada: 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Las otras desviaciones de las reglas de COM estándar se describen en la siguiente tabla.
  
|**Regla de programación de COM**|**Variante de MAPI**|
|:-----|:-----|
|Todos los parámetros de cadena de los métodos de interfaz deben ser Unicode.  <br/> |Interfaces MAPI se definen para permitir que los parámetros de cadena Unicode o ANSI. Muchos de los métodos que tienen un parámetro de cadena también tienen un parámetro **ulFlags** ; el ancho de un parámetro de cadena se indica mediante el valor de la marca MAPI_UNICODE en **ulFlags**. Algunas interfaces MAPI no admite Unicode y devolver MAPI_E_BAD_CHARWIDTH cuando se establece el indicador MAPI_UNICODE..  <br/> |
|Todos los métodos de interfaz deben tener un tipo de valor devuelto de HRESULT.  <br/> |MAPI tiene al menos un método que devuelve un valor HRESULT que no sean: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).  <br/> |
|Los autores de llamadas y los implementadores deben asignar y liberar memoria para los parámetros de la interfaz mediante la asignadores de tarea COM estándares.  <br/> |Todos los métodos MAPI utilizan la asignadores vinculados [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md) para administrar la memoria para los parámetros de la interfaz. Todas las implementaciones de MAPI de interfaces definidas por OLE, como [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use la asignadores de tarea COM estándares.  <br/> |
|Cerrar todos los parámetros de puntero explícitamente se deben establecer en NULL cuando se produce un error en un método.  <br/> |Interfaces MAPI requieren que los parámetros de puntero estar establecido en NULL o no se modifican cuando un método de salida se produce un error. Todas las implementaciones de MAPI de interfaces definidas por OLE establecer explícitamente los parámetros en NULL en caso de error de salida.  <br/> |
|Implementar objetos agregables siempre que sea posible.  <br/> |Interfaces MAPI no están agregables.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Objeto MAPI e Introducción a la interfaz](mapi-object-and-interface-overview.md)

