---
title: Funcionalidades no admitidas por los administradores de formularios
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
# <a name="capabilities-not-supported-by-form-managers"></a>Funcionalidades no admitidas por los administradores de formularios

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El administrador de formularios predeterminado no admite las siguientes características por motivos de rendimiento, pero pueden ser compatibles con los administradores de formularios personalizados.
  
- Jerarquía que permite agrupar o clasificar formularios en una biblioteca de formularios. Una biblioteca de formularios es una base de datos de formularios de archivos planos.
    
- Control de acceso para categorías de formularios, correspondientes a clases de mensajes o superclases.
    
- Compatibilidad con varias versiones de idioma del mismo formulario en una sola biblioteca de formularios.
    
Estos son problemas de implementación. No hay nada que impida que un administrador de formularios personalizado implemente estas características.
  
La arquitectura de formulario MAPI no admite la ejecución simultánea de varios administradores de formularios. Aunque MAPI admite varios proveedores de almacén de mensajes simultáneos, proveedores de transporte y proveedores de libretas de direcciones, solo se admite un administrador de formularios único.
  
Como solo se puede ejecutar un administrador de formularios a la vez, si implementa un administrador de formularios personalizado, tendrá que volver a implementar cualquier funcionalidad del administrador de formularios predeterminado que necesite. Dado que el administrador de formularios personalizado reemplazará por completo al administrador de formularios predeterminado, las capacidades del administrador de formularios predeterminado no estarán disponibles a menos que se dupliquen en el administrador de formularios personalizado.
  
## <a name="see-also"></a>Consulte también



[Formularios MAPI](mapi-forms.md)

