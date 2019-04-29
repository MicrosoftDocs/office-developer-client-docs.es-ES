---
title: Capacidades no admitidas por los administradores de formularios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e31eacaae54968fbdbd9fe0345130a8d09c3509f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419383"
---
# <a name="capabilities-not-supported-by-form-managers"></a>Capacidades no admitidas por los administradores de formularios

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las siguientes características no son compatibles con el administrador de formularios predeterminado por motivos de rendimiento, pero pueden ser compatibles con los administradores de formularios personalizados.
  
- Una jerarquía que permite agrupar o clasificar formularios en una biblioteca de formularios. Una biblioteca de formularios es una base de datos de archivos sin formato de los formularios.
    
- Control de acceso para categorías de formularios, correspondientes a las clases de mensaje o las superclases.
    
- Compatibilidad con versiones de varios idiomas del mismo formulario en una única biblioteca de formularios.
    
Estos son problemas de implementación. No hay nada que impida que un administrador de formularios personalizado implemente estas características.
  
La arquitectura de formularios MAPI no es compatible con varios administradores de formularios que se ejecutan simultáneamente. Aunque MAPI admite varios proveedores de almacenamiento de mensajes simultáneos, proveedores de transporte y proveedores de libretas de direcciones, solo se admite un único administrador de formularios.
  
Como solo se puede ejecutar un administrador de formularios a la vez, si implementa un administrador de formularios personalizado tendrá que volver a implementar cualquier funcionalidad del administrador de formularios predeterminado que necesite. Como el administrador de formularios personalizado reemplazará por completo el administrador de formularios predeterminado, las capacidades del administrador de formularios predeterminado no estarán disponibles a menos que se dupliquen en el administrador de formularios personalizado.
  
## <a name="see-also"></a>Ver también



[Formularios MAPI](mapi-forms.md)

