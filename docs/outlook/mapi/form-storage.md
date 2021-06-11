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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414896"
---
# <a name="form-storage"></a>Almacenamiento de formularios

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Aunque no es necesario conocer todos los detalles de cómo se almacenan físicamente los formularios, resulta útil comprender algunos de los conceptos principales. Por lo tanto, antes de describir los tres tipos de bibliotecas de formularios admitidas por el administrador de formularios predeterminado, en este tema se ofrece información general sobre cómo se almacenan los formularios.
  
Las definiciones de formulario se pueden almacenar físicamente en carpetas en uno o más almacenes de mensajes MAPI. Cada carpeta MAPI se puede pensar que tiene dos áreas para almacenar objetos de mensaje: la parte estándar y la parte asociada. La parte estándar de la carpeta incluye los mensajes y carpetas que los usuarios manipulan.
  
La parte asociada incluye objetos de mensaje ocultos asociados a la carpeta, incluidas definiciones de formulario, vistas, plantillas de regla, plantillas de respuesta, entre otros. Esta parte alternativa se denomina tabla de contenido asociada a la carpeta y el conjunto de mensajes de la tabla de contenido asociada se conoce como la información asociada a la carpeta. Los mensajes ocultos son una parte integral de la carpeta y se copian junto con el contenido de la carpeta estándar cuando se copia la carpeta. Aunque físicamente se almacena como mensajes, la información de la tabla de contenido asociada de una carpeta se comporta más como propiedades que como mensajes que se pueden ver. Cualquier objeto de carpeta que admita una tabla de contenido asociada es capaz de almacenar formularios personalizados. El [método IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) puede devolver el contenido estándar o el contenido asociado de la carpeta, según el valor del parámetro  _ulflags del_ método. 
  
Una biblioteca de formularios consta de definiciones de formulario almacenadas en la tabla de contenido asociada de una carpeta. La definición del formulario incluye las propiedades del formulario, las acciones que admite el formulario e incluso el archivo ejecutable del servidor de formulario, que se almacena como uno o varios datos adjuntos de mensajes.
  
Además, los formularios se pueden almacenar en cualquier archivo o ubicación que admita el administrador de formularios que se está utilizando. El administrador de formularios predeterminado almacena servidores de formulario en carpetas MAPI, pero un administrador de formularios personalizado podría implementar su propio almacenamiento para servidores de formulario.
  
Un formulario puede tener varias interfaces de usuario enlazadas a su clase de mensaje. Por ejemplo, un formulario puede tener interfaces de usuario de redacción y lectura independientes. El formulario se encarga de invocar la interfaz de usuario adecuada para distintas solicitudes de usuario, según cuál de los verbos del formulario se llame. Por ejemplo, si el servidor de formularios tiene interfaces de usuario de redacción y lectura independientes, la interfaz de usuario Redacción se puede abrir automáticamente cuando el usuario crea un nuevo mensaje de la clase de mensaje del formulario y la interfaz de usuario Leer se puede abrir automáticamente cuando el usuario abre un mensaje existente de la clase de mensaje del formulario.
  
La mayor parte de la información almacenada en una definición de formulario está disponible invocando el método [IMAPIFormInfo::IMAPIProp](imapiforminfoimapiprop.md) en un **objeto IMAPIFormInfo.** La **interfaz IMAPIFormInfo** simplifica el acceso a la información del formulario llamando a todos los métodos de mensaje y carpeta MAPI necesarios para recuperar la información. Se puede obtener un objeto **IMAPIFormInfo** llamando al método [IMAPIFormContainer::ResolveMessageClass.](imapiformcontainer-resolvemessageclass.md) 
  
Los tres tipos de bibliotecas de formularios se describen en los temas Bibliotecas de [formularios locales,](local-form-libraries.md)Bibliotecas de formularios de [carpetas](folder-form-libraries.md) y [Bibliotecas de formularios personales.](personal-form-libraries.md)
  
## <a name="see-also"></a>Vea también

- [Formularios MAPI](mapi-forms.md)

