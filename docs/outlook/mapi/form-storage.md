---
title: Almacenamiento de formularios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ddf9158-3c10-408a-aeaf-5a382c4339e7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 793a34b093ba69f73be7e186bec0a769584bbac4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328087"
---
# <a name="form-storage"></a>Almacenamiento de formularios

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Aunque no es necesario conocer todos los detalles sobre cómo se almacenan físicamente los formularios, es útil comprender algunos de los conceptos principales. Por lo tanto, antes de describir los tres tipos de bibliotecas de formularios compatibles con el administrador de formularios predeterminado, en este tema se proporciona información general sobre cómo se almacenan los formularios.
  
Las definiciones de formulario se pueden almacenar físicamente en carpetas en uno o más almacenes de mensajes MAPI. Se puede considerar que cada carpeta MAPI tiene dos áreas para almacenar objetos de mensaje: la parte estándar y la parte asociada. La parte estándar de la carpeta incluye los mensajes y las carpetas que los usuarios manipulan.
  
La parte asociada incluye los objetos de mensajes ocultos que están asociados a la carpeta, incluidas las definiciones de formulario, las vistas, las plantillas de regla, las plantillas de respuesta, etc. Este elemento alternativo se denomina tabla de contenido asociado a la carpeta y el conjunto de mensajes de la tabla de contenido asociada se conoce como la información asociada a la carpeta. Los mensajes ocultos son una parte integral de la carpeta y se copian junto con el contenido de la carpeta estándar cuando se copia la carpeta. Aunque se almacenan físicamente como mensajes, la información de la tabla de contenido asociada a una carpeta se comporta más que las propiedades que como los mensajes visibles. Cualquier objeto Folder que admita una tabla de contenido asociada puede almacenar formularios personalizados. El método [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) puede devolver el contenido estándar o el contenido asociado de la carpeta, según el valor del parámetro _ulflags_ del método. 
  
Una biblioteca de formularios consta de definiciones de formulario almacenadas en la tabla de contenido asociada de una carpeta. La definición del formulario incluye las propiedades del formulario, las acciones que admite y, incluso, el archivo ejecutable del servidor de formularios, que se almacena como uno o varios datos adjuntos del mensaje.
  
Además, los formularios se pueden almacenar en cualquier archivo o ubicación que el administrador de formularios use admita. El administrador de formularios predeterminado almacena los servidores de formularios en las carpetas MAPI, pero un administrador de formularios personalizado puede implementar su propio almacenamiento para los servidores de formularios.
  
Un formulario puede tener varias interfaces de usuario enlazadas a su clase de mensaje. Por ejemplo, un formulario puede tener interfaces de usuario de redacción y lectura separadas. El formulario se encarga de invocar la interfaz de usuario adecuada para diferentes solicitudes de usuario, en función de cuál de los verbos del formulario se llama. Por ejemplo, si el servidor de formularios tiene interfaces de usuario de redacción y lectura separadas, la interfaz de usuario de redacción se puede abrir automáticamente cuando el usuario crea un nuevo mensaje de la clase de mensaje del formulario y la interfaz de usuario de lectura se puede abrir automáticamente cuando el el usuario abre un mensaje existente de la clase de mensaje del formulario.
  
La mayor parte de la información almacenada en una definición de formulario está disponible al invocar el método [IMAPIFormInfo:: IMAPIProp](imapiforminfoimapiprop.md) en un objeto **IMAPIFormInfo** . La interfaz **IMAPIFormInfo** simplifica el acceso a la información de los formularios al llamar a todos los métodos de carpeta y mensajes MAPI necesarios para recuperar la información. Se puede obtener un objeto **IMAPIFormInfo** llamando al método [IMAPIFormContainer:: ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) . 
  
Los tres tipos de bibliotecas de formularios se describen en los temas bibliotecas de formularios [locales](local-form-libraries.md), bibliotecas de [formularios de carpetas](folder-form-libraries.md) y bibliotecas de [formularios personales](personal-form-libraries.md).
  
## <a name="see-also"></a>Vea también

- [Formularios MAPI](mapi-forms.md)

