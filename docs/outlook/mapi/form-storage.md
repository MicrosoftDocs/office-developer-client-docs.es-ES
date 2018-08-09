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
ms.openlocfilehash: a99ef76e63e634c661bf82bdab10b86c843e0df0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816857"
---
# <a name="form-storage"></a>Almacenamiento de formularios

**Hace referencia a**: Outlook 
  
Aunque no es necesario conocer todos los detalles de cómo se almacenan físicamente los formularios, es útil comprender algunos de los conceptos principales. Por lo tanto, antes de describir los tres tipos de bibliotecas de formularios compatibles con el Administrador de forma predeterminada, este tema proporciona una visión general de cómo se almacenan los formularios.
  
Las definiciones de formularios pueden almacenarse físicamente dentro de las carpetas en uno o varios almacenes de mensaje MAPI. Cada carpeta MAPI puede considerarse como tener dos áreas para almacenar objetos de mensaje: el elemento estándar y el elemento asociado. El elemento estándar de la carpeta incluye los mensajes y carpetas que manipulan los usuarios.
  
El elemento asociado incluye objetos de mensaje oculto que están asociados con la carpeta, incluidas las definiciones de formularios, vistas, plantillas de reglas, plantillas de respuesta y así sucesivamente. En este artículo alternativo se llama en la tabla de contenido asociada a la carpeta y el conjunto de mensajes en la tabla de contenido asociada se conoce como la información asociada a la carpeta. Los mensajes ocultos son una parte integral de la carpeta y se copian junto con el contenido de la carpeta estándar cuando se copia la carpeta. Aunque se almacenan físicamente como mensajes, información de tabla de contenido asociada de una carpeta se comporta más como propiedades de los mensajes visibles, como. Cualquier objeto de carpeta que es compatible con una tabla de contenido asociada es capaz de almacenar formularios personalizados. El método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) puede devolver el contenido estándar o el contenido de la carpeta, según el valor del parámetro del método _ulflags_ asociado. 
  
Una biblioteca de formularios se compone de definiciones de formulario almacenadas en la tabla de contenido asociada de una carpeta. La definición del formulario incluye las propiedades del formulario, las acciones que admite el formulario e incluso el formulario server archivo ejecutable, que se almacena como datos adjuntos de mensajes de uno o más.
  
Además, los formularios pueden almacenarse en cualquier archivo o ubicación que admite el Administrador de formulario que se usa. El Administrador de formulario predeterminado almacena los servidores de formulario en las carpetas MAPI, pero el Administrador de un formulario personalizado podría implementar su propio almacenamiento de información para servidores de formulario.
  
Un formulario puede tener varias interfaces de usuario que se enlazan a su clase de mensaje. Por ejemplo, un formulario puede tener interfaces de usuario independientes de redacción y lectura. Se llama el formulario se encarga de invocar la interfaz de usuario adecuados para las solicitudes de usuario diferente, dependiendo de cuál de los verbos del formulario. Por ejemplo, si su servidor de formulario tiene Redactar independientes y la lectura de interfaces de usuario, la interfaz de usuario de redacción puede abrirse automáticamente cuando el usuario crea un nuevo mensaje de clase de mensaje del formulario y la interfaz de usuario de lectura se puede abrir automáticamente cuando la usuario abre un mensaje existente de clase de mensaje del formulario.
  
La mayor parte de la información almacenada dentro de una definición de formulario está disponible al invocar el método [IMAPIFormInfo::IMAPIProp](imapiforminfoimapiprop.md) en un objeto **IMAPIFormInfo** . La interfaz de **IMAPIFormInfo** simplifica el acceso a la información del formulario mediante una llamada a todos los métodos necesarios para recuperar la información del mensaje y carpeta MAPI. Un objeto **IMAPIFormInfo** puede obtenerse llamando al método [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) . 
  
Los tres tipos de bibliotecas de formularios se describen en los temas de [Las bibliotecas de formularios Local](local-form-libraries.md), [Bibliotecas de formularios de carpeta](folder-form-libraries.md) y [Bibliotecas de formularios personales](personal-form-libraries.md).
  
## <a name="see-also"></a>Vea también

- [Formularios MAPI](mapi-forms.md)

