---
title: Desarrollar servidores de formulario MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338531"
---
# <a name="developing-mapi-form-servers"></a>Desarrollar servidores de formulario MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En esta sección se describe el proceso de creación de archivos de configuración de formulario y ejecutables del servidor de formularios para crear formularios MAPI personalizados. Antes de leer esta sección, debe familiarizarse con la información de los [formularios MAPI](mapi-forms.md).
  
El desarrollo de un servidor de formularios incluye los siguientes pasos:
  
1. Decidir qué información contendrá el formulario y cómo elegir un conjunto de propiedades que contengan esta información. Para obtener más información, vea [elegir el conjunto de propiedades de un formulario](choosing-a-form-s-property-set.md).
    
2. Diseño de una interfaz de usuario con la que los usuarios pueden interactuar con las propiedades del formulario.
    
3. Elegir una clase de mensaje y generar un identificador de clase único (CLSID). Para obtener información general sobre las clases de mensajes, consulte [MAPI Message classes](mapi-message-classes.md). Para obtener más información acerca de las clases de mensajes y formularios, consulte [elección de una clase de mensaje](choosing-a-message-class.md).
    
4. Implementar las interfaces de formulario de MAPI necesarias, así como todas las interfaces opcionales que su servidor de formularios concreto necesite. Para obtener más información, consulte [Writing Form Server Code](writing-form-server-code.md). 
    
5. Escribir código de interfaz de usuario para controlar la interacción del usuario con el objeto Form y las propiedades que usa el formulario.
    
6. Crear un archivo de configuración de formulario para el formulario. Para obtener más información, vea el [formato de archivo de los archivos de configuración de formulario](file-format-of-form-configuration-files.md).
    
7. Instalar el formulario en los equipos de los usuarios. Para obtener más información, vea [instalar un formulario en una biblioteca](installing-a-form-into-a-library.md).
    
Probablemente realizará los pasos del 1 al 5 simultáneamente, en lugar de completarlos en secuencia. El proceso de desarrollo de un servidor de formularios, como muchos proyectos de programación, no es uno en el que hay una secuencia especialmente bien definida. Por ejemplo, la creación de un archivo de configuración de formulario se muestra como el último paso anterior, pero probablemente creará el archivo de configuración de formulario de forma incremental y se volverá más completo a medida que agregue características al servidor de formularios.
  
## <a name="see-also"></a>Vea también



[Conceptos de MAPI](mapi-concepts.md)

