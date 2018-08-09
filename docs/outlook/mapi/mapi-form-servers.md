---
title: Servidores de formulario MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 855292b8-028e-4c1e-87ed-3f20b9ba584a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: dad36bfc5fed296cff3baa4cc11bb1fdf359c45a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818123"
---
# <a name="mapi-form-servers"></a>Servidores de formulario MAPI

  
  
**Hace referencia a**: Outlook 
  
Desde la perspectiva del usuario, un formulario es normalmente una hoja de propiedades para un mensaje o un formulario de entrada de datos que permite a los usuarios introducir información estructurada. Sin embargo, puede ser cualquier interfaz de usuario que está asociado a una clase de mensaje. Desde el punto de vista del programador, una forma consta de:
  
- Un tipo de mensaje MAPI con su propia clase de mensaje y el identificador de OLE.
    
- El archivo ejecutable que implementa el servidor de formulario.
    
- Una colección de propiedades MAPI: personalizado o de lo contrario, que usa el servidor de formulario. Algunas o todas estas pueden estar disponible para clientes de mensajería para su uso.
    
- El archivo de configuración que describe la forma y se usa en el Administrador de formularios.
    
Debido a que los formularios son objetos [IMessage](imessageimapiprop.md) , presentan las propiedades y el comportamiento que es coherente con los objetos de mensaje MAPI. Sin embargo, debido a que los formularios pueden tener propiedades personalizadas, controles y una representación para mostrar que es específico de la aplicación, las interfaces MAPI que formularios de uso son lo suficientemente genéricas como para permitir a cualquier tipo de interfaz que es necesario. La definición de un formulario se almacena en una biblioteca de formularios, que se trata más adelante en esta sección. 
  
> [!NOTE]
> De forma más precisa, todos los mensajes son instancias de formularios MAPI. Sin embargo, generalmente resulta más sencillo pensar de formularios personalizados como casos especiales de mensajes, ya que los formularios para redactar y leer mensajes de correo electrónico típicos son los formularios usados con frecuencia. El hecho de que todos los mensajes son en realidad proporciona de formularios personalizado de formularios el mismo estado que cualquier otro mensaje en el sistema MAPI. 
  
Cada formulario tiene un conjunto de propiedades, algunas de las cuales están visibles en la interfaz de usuario del formulario. Normalmente, las propiedades coinciden con los campos en la interfaz de usuario del formulario. Por ejemplo, un formulario de pedido de compra puede tener los campos de elemento, descripción, precio, impuestos y Subtotal. Estos campos son versiones simplemente visual del formulario de propiedades de los mismos nombres. Los clientes de determinar qué propiedades son compatibles con una clase de mensaje en particular a través del método [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md) , que se implementa mediante el Administrador de formularios de MAPI. 
  
Como básica de los mensajes, los formularios MAPI pueden contener todas las propiedades de mensaje estándar, como el remitente, el destinatario, y cuándo se envió el mensaje. Formularios también pueden contener cualquier número de propiedades personalizadas que son específicos para el formulario. Por ejemplo un formulario de "Informe de errores" podría contener propiedades personalizadas para el tipo de error, la gravedad de errores y versión del producto.
  
Para crear un formulario debe implementar un servidor de formulario. El servidor de formulario es el archivo ejecutable que se carga cuando un cliente de mensajería debe mostrar un mensaje que es el tipo admitido por el servidor de formulario. El servidor de formulario a su vez crea objetos de formulario según sea necesario para mostrar mensajes específicos y controlar las interacciones de usuario con los mensajes.
  
Cada servidor de formulario tiene un archivo de configuración asociado con él. Este archivo contiene información que describe el servidor de formulario en beneficio de administrador de formularios. El Administrador de formulario usa esta información al instalar al servidor de formulario en una biblioteca de formularios.
  
Para obtener información detallada sobre la creación de las partes de un formulario, vea [Desarrollo de servidores de formulario MAPI](developing-mapi-form-servers.md).
  
Servidores de formulario se ajustan al modelo de objetos componentes (COM). Servidores de formulario se ejecutan como ejecutables independientes, no como servidores en proceso. Para obtener más información, vea la sección Servicios de objeto de ActiveX y COM en el SDK de Windows.
  
Un identificador único de clase (CLSID) identifica cada servidor del formulario. Siempre hay una asignación uno a uno entre un identificador de clase y su clase de mensaje. Esto no significa, sin embargo, que un servidor de formulario sólo puede trabajar con los mensajes de una clase de mensaje. Si no hay ningún servidor de formulario está disponible para un mensaje de una clase determinada de servicio, debe intentar el Administrador de formulario que se usa Buscar un servidor de formulario para una clase de mensaje más arriba en la jerarquía de clases de mensaje; el Administrador de formulario predeterminado que se proporciona con el SDK de Windows para ello. Como un servidor de formulario probablemente podrá representar sólo un subconjunto de las propiedades del mensaje (es decir, los que admite la superclase), pero es mejor que nada. ¿Qué sucede cuando se encuentra ningún servidor de formulario coincidente en absoluto es un detalle de implementación específico para el Administrador de formulario que se usa; el Administrador de formulario predeterminado no abrir los mensajes cuando esto sucede.
  
Para obtener más información, vea [Las clases de mensajes de MAPI](mapi-message-classes.md).
  
## <a name="see-also"></a>Vea también



[Formularios MAPI](mapi-forms.md)

