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
ms.openlocfilehash: 3c95f6a1d4d50dd6552c6e786d17c40da14f3f3c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419110"
---
# <a name="mapi-form-servers"></a>Servidores de formulario MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Desde la perspectiva del usuario, un formulario suele ser una hoja de propiedades de un mensaje o un formulario de entrada de datos que permite a los usuarios escribir información estructurada. Sin embargo, puede ser cualquier interfaz de usuario asociada a una clase de mensaje. Desde el punto de vista de un programador, un formulario consta de:
  
- Tipo de mensaje MAPI con su propia clase de mensaje e identificador OLE.
    
- Archivo ejecutable que implementa el servidor de formularios.
    
- Colección de propiedades MAPI (personalizadas o de otro tipo) que usa el servidor de formularios. Algunos o todos estos pueden estar disponibles para los clientes de mensajería para su uso.
    
- El archivo de configuración que describe el formulario y que usa el administrador de formularios.
    
Dado que los formularios [son objetos IMessage,](imessageimapiprop.md) presentan propiedades y comportamiento coherentes con los objetos de mensaje MAPI. Sin embargo, como los formularios pueden tener propiedades personalizadas, controles y una representación para mostrar específica de la aplicación, las interfaces MAPI que usan los formularios son lo suficientemente genéricas como para permitir cualquier tipo de interfaz necesaria. La definición real de un formulario se almacena en una biblioteca de formularios, que se describe más adelante en esta sección. 
  
> [!NOTE]
> De forma más precisa, todos los mensajes son instancias de formularios MAPI. Sin embargo, suele ser más fácil pensar en formularios personalizados como casos especiales de mensajes, ya que los formularios para redactar y leer mensajes de correo electrónico típicos son los formularios más usados. El hecho de que todos los mensajes sean simplemente formularios proporciona a los formularios personalizados el mismo estado que cualquier otro mensaje en el sistema MAPI. 
  
Cada formulario tiene un conjunto de propiedades, algunas de las cuales son visibles en la interfaz de usuario del formulario. Normalmente, las propiedades coinciden con los campos de la interfaz de usuario del formulario. Por ejemplo, un formulario de pedido de compra puede tener los campos Item, Description, Price, Tax y Subtotal. Estos campos son simplemente representaciones visuales de propiedades de formulario de los mismos nombres. Los clientes comprueban qué propiedades son compatibles con una clase de mensaje determinada a través del método [IMAPIFormInfo::CalcFormPropSet,](imapiforminfo-calcformpropset.md) que implementa el administrador de formularios MAPI. 
  
Al igual que los mensajes básicos, los formularios MAPI pueden contener todas las propiedades de mensaje estándar, como el remitente, el destinatario previsto y cuándo se envió el mensaje. Los formularios también pueden contener cualquier número de propiedades personalizadas que sean específicas del formulario. Por ejemplo, un formulario "Informe de errores" puede contener propiedades personalizadas para tipo de error, gravedad de error y versión del producto.
  
Para crear un formulario, debe implementar un servidor de formularios. El servidor de formulario es el archivo ejecutable que se carga cuando un cliente de mensajería necesita mostrar un mensaje que sea el tipo admitido por el servidor de formularios. A su vez, el servidor de formularios crea objetos de formulario según sea necesario para mostrar mensajes específicos y controlar las interacciones del usuario con esos mensajes.
  
Cada servidor de formulario tiene asociado un archivo de configuración. Este archivo contiene información que describe el servidor de formularios en beneficio del administrador de formularios. El administrador de formularios usa esta información al instalar el servidor de formularios en una biblioteca de formularios.
  
Para obtener más información sobre cómo crear las partes de un formulario, vea [Developing MAPI Form Servers](developing-mapi-form-servers.md).
  
Los servidores de formulario se adhieren al modelo de objetos componentes (COM). Los servidores de formulario se ejecutan como ejecutables independientes, no como servidores en proceso. Para obtener más información, vea la sección COM y ActiveX Object Services en el SDK Windows.
  
Un identificador de clase único (CLSID) identifica cada servidor de formulario. Siempre hay una asignación uno a uno entre un identificador de clase y su clase de mensaje. Sin embargo, esto no significa que un servidor de formulario solo puede trabajar con mensajes de una clase de mensaje. Si no hay ningún servidor de formulario disponible para dar servicio a un mensaje de una clase determinada, el administrador de formularios que se está utilizando debe intentar buscar un servidor de formulario para una clase de mensaje superior en la jerarquía de clases de mensaje; el administrador de formularios predeterminado proporcionado con Windows SDK hace esto. Este servidor de formulario probablemente podrá representar solo un subconjunto de las propiedades del mensaje (las compatibles con la superclase), pero será mejor que nada. Lo que sucede cuando no se encuentra ningún servidor de formularios que coincida en absoluto es un detalle de implementación específico del administrador de formularios que se está utilizando; el administrador de formularios predeterminado no abre mensajes cuando esto sucede.
  
Para obtener más información, vea [Mapi Message Classes](mapi-message-classes.md).
  
## <a name="see-also"></a>Vea también



[Formularios MAPI](mapi-forms.md)

