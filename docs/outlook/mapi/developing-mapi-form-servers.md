---
title: Desarrollo de los servidores de formulario MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 83d652f313e139b1c6bb628d1119edda03a70e23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816674"
---
# <a name="developing-mapi-form-servers"></a>Desarrollo de los servidores de formulario MAPI

  
  
**Se aplica a**: Outlook 
  
En esta sección se describe el proceso de creación de servidor de formulario ejecutable y los archivos de configuración de formulario para la creación de formularios personalizados de MAPI. Antes de leer esta sección, debe familiarizarse con la información de [Formularios de MAPI](mapi-forms.md).
  
Desarrollo de un servidor de formulario incluye los siguientes pasos:
  
1. Decidir qué información va a contener el formulario y elegir un conjunto de propiedades para contener esa información. Para obtener más información, vea [elegir establecer propiedad de un formulario](choosing-a-form-s-property-set.md).
    
2. Diseño de una interfaz de usuario con la que los usuarios pueden interactuar con las propiedades del formulario.
    
3. Elección de una clase de mensaje y generar un identificador único de clase (CLSID). Para obtener información general de las clases de mensajes, vea [Las clases de mensajes de MAPI](mapi-message-classes.md). Para obtener más información acerca de las clases de mensajes y formularios, vea [Elegir una clase de mensaje](choosing-a-message-class.md).
    
4. Implementación de las interfaces de formulario MAPI necesarias, así como cualquier interfaces opcionales que necesita su servidor de formulario en particular. Para obtener más información, vea [Escribir código de servidor de formulario](writing-form-server-code.md). 
    
5. Escritura de código de la interfaz de usuario para controlar la interacción del usuario con el objeto de formulario y las propiedades utiliza el formulario.
    
6. Creación de un archivo de configuración de formulario para el formulario. Para obtener más información, vea el [Archivo de formato de formulario de los archivos de configuración](file-format-of-form-configuration-files.md).
    
7. Instalando el formulario en los equipos de los usuarios. Para obtener más información, vea [instalar un formulario en una biblioteca](installing-a-form-into-a-library.md).
    
Es muy probable que llevará a cabo los pasos del 1 al 5 simultáneamente en lugar de realizarlas en secuencia. El proceso de desarrollo de un servidor de formulario, al igual que muchos proyectos de programación, no es uno de que exista una secuencia especialmente bien definida. Por ejemplo, la creación de un archivo de configuración de formulario se muestra como el segundo a último paso anterior, pero probablemente va a crear el archivo de configuración del formulario de forma incremental y se convertirán en más completa como agregar características a su servidor de formulario.
  
## <a name="see-also"></a>Ver también



[Conceptos MAPI](mapi-concepts.md)

