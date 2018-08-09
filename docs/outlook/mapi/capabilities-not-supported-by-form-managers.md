---
title: Funciones no compatibles con los administradores de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 86c91353b620482ca0862aa998aae1b3329cfc94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816502"
---
# <a name="capabilities-not-supported-by-form-managers"></a>Funciones no compatibles con los administradores de formulario

  
  
**Hace referencia a**: Outlook 
  
Las siguientes características no son compatibles con el Administrador de formulario predeterminado por motivos de rendimiento, pero pueden ser compatibles con los administradores de formulario personalizado.
  
- Una jerarquía que permite formularios se agrupan o clasifican a lo largo de una biblioteca de formularios. Una biblioteca de formularios es una base de datos de archivos planos de formularios.
    
- Control de acceso para las categorías de formularios, correspondiente a las clases de mensajes o superclase.
    
- Compatibilidad con varias versiones de idioma del mismo formulario en una biblioteca de formularios único.
    
Estos son los problemas de implementación. No hay nada para evitar que el Administrador de un formulario personalizado de la implementación de estas características.
  
La arquitectura de formulario MAPI no admite la ejecución simultánea de varios directores de formulario. Aunque MAPI admite varios proveedores de almacén de mensajes de usuarios simultáneos, los proveedores de transporte y los proveedores de la libreta de direcciones, se admite solo un administrador de formulario simple.
  
Debido a que el formulario sólo un administrador puede estar en ejecución a la vez, si implementa el Administrador de un formulario personalizado debe volver a implementar cualquier funcionalidad desde el Administrador de formulario predeterminado que necesita. Debido a que el Administrador de su formulario personalizado reemplazará por completo el Administrador de forma predeterminada, las funciones del Administrador de formulario predeterminado de no estará disponibles a menos que se duplican en el Administrador de su formulario personalizado.
  
## <a name="see-also"></a>Vea también



[Formularios MAPI](mapi-forms.md)

