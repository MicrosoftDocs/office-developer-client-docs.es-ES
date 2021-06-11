---
title: Desarrollo de servidores de formulario MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420769"
---
# <a name="developing-mapi-form-servers"></a>Desarrollo de servidores de formulario MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En esta sección se describe el proceso de creación de archivos ejecutables y de configuración de formularios del servidor de formularios para crear formularios MAPI personalizados. Antes de leer esta sección, debe familiarizarse con la información de [formularios MAPI.](mapi-forms.md)
  
El desarrollo de un servidor de formularios incluye los siguientes pasos:
  
1. Decidir qué información contendrá el formulario y elegir un conjunto de propiedades para contener esa información. Para obtener más información, vea [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).
    
2. Diseño de una interfaz de usuario con la que los usuarios puedan interactuar con las propiedades del formulario.
    
3. Elegir una clase de mensaje y generar un identificador de clase único (CLSID). Para obtener información general sobre las clases de mensaje, vea [Mapi Message Classes](mapi-message-classes.md). Para obtener más información acerca de los formularios y clases de mensaje, vea [Elegir una clase de mensaje](choosing-a-message-class.md).
    
4. Implementar las interfaces de formulario MAPI necesarias, así como las interfaces opcionales que necesita el servidor de formulario en particular. Para obtener más información, vea [Writing Form Server Code](writing-form-server-code.md). 
    
5. Escribir código de interfaz de usuario para controlar la interacción del usuario con el objeto de formulario y las propiedades que usa el formulario.
    
6. Crear un archivo de configuración de formulario para el formulario. Para obtener más información, vea [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).
    
7. Instalar el formulario en los equipos de los usuarios. Para obtener más información, vea [Installing a Form into a Library](installing-a-form-into-a-library.md).
    
Lo más probable es que realice los pasos del 1 al 5 simultáneamente en lugar de completarlos en secuencia. El proceso de desarrollo de un servidor de formularios, como muchos proyectos de programación, no es uno en el que haya una secuencia especialmente bien definida. Por ejemplo, la creación de un archivo de configuración de formulario se muestra como el segundo al último paso anterior, pero probablemente creará el archivo de configuración de formulario de forma incremental y se hará más completo a medida que agregue características al servidor de formularios.
  
## <a name="see-also"></a>Vea también



[Conceptos de MAPI](mapi-concepts.md)

