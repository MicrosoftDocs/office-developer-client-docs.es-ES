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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351488"
---
# <a name="mapi-form-servers"></a>Servidores de formulario MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Desde el punto de vista del usuario, un formulario suele ser una hoja de propiedades para un mensaje o un formulario de entrada de datos que permite a los usuarios introducir información estructurada. Sin embargo, puede ser cualquier interfaz de usuario que esté asociada con una clase de mensaje. Desde el punto de vista del programador, un formulario consta de:
  
- Un tipo de mensaje MAPI con su propia clase de mensaje y un identificador OLE.
    
- El archivo ejecutable que implementa el servidor de formularios.
    
- Una colección de propiedades MAPI (personalizadas o de otro tipo) que usa el servidor de formularios. Algunas o todas ellas pueden estar disponibles para el uso de clientes de mensajería.
    
- El archivo de configuración que describe el formulario y lo usa el administrador de formularios.
    
Dado que los formularios son objetos [IMessage](imessageimapiprop.md) , muestran las propiedades y el comportamiento coherentes con los objetos de mensaje MAPI. Sin embargo, dado que los formularios pueden tener propiedades personalizadas, controles y una representación de presentación específica de la aplicación, las interfaces MAPI que usan los formularios son lo suficientemente genéricas como para permitir cualquier tipo de interfaz necesaria. La definición real de un formulario se almacena en una biblioteca de formularios, que se describe más adelante en esta sección. 
  
> [!NOTE]
> De forma más precisa, todos los mensajes son instancias de los formularios MAPI. Sin embargo, normalmente es más fácil pensar en los formularios personalizados como casos especiales de mensajes, ya que los formularios para redactar y leer mensajes de correo electrónico típicos son los formularios más usados. El hecho de que todos los mensajes sean realmente solo formularios da a los formularios personalizados el mismo estado que cualquier otro mensaje en el sistema MAPI. 
  
Cada formulario tiene un conjunto de propiedades, algunos de los cuales son visibles en la interfaz de usuario del formulario. Normalmente, las propiedades se corresponden con los campos de la interfaz de usuario del formulario. Por ejemplo, un formulario de pedido de compra podría tener los campos Item, deScription, Price, Tax y subtotal. Estos campos son simplemente representaciones visuales de propiedades de formulario con los mismos nombres. Los clientes determinen qué propiedades son compatibles con una clase de mensaje determinada a través del método [IMAPIFormInfo:: CalcFormPropSet](imapiforminfo-calcformpropset.md) , implementado por el administrador de formularios MAPI. 
  
Al igual que los mensajes básicos, los formularios MAPI pueden contener todas las propiedades estándar del mensaje, como el remitente, el destinatario deseado y el momento en que se envió el mensaje. Los formularios también pueden contener cualquier número de propiedades personalizadas específicas del formulario. Por ejemplo, un formulario de "informe de errores" puede contener propiedades personalizadas para el tipo de error, la gravedad del error y la versión del producto.
  
Para crear un formulario, debe implementar un servidor de formularios. El servidor de formularios es el archivo ejecutable que se carga cuando un cliente de mensajería necesita mostrar un mensaje que es del tipo compatible con el servidor de formularios. El servidor de formularios, a su vez, crea los objetos de formulario según sea necesario para mostrar mensajes específicos y controlar las interacciones del usuario con esos mensajes.
  
Cada servidor de formularios tiene asociado un archivo de configuración. Este archivo contiene información que describe el servidor de formularios en beneficio del administrador de formularios. El administrador de formularios usa esta información al instalar el servidor de formularios en una biblioteca de formularios.
  
Para obtener información detallada sobre cómo crear las partes de un formulario, consulte [developING MAPI Form Servers](developing-mapi-form-servers.md).
  
Los servidores de formularios se adhieran al modelo de objetos componentes (COM). Los servidores de formularios se ejecutan como ejecutables independientes, no como servidores en proceso. Para obtener más información, vea la sección servicios de objetos ActiveX y COM en el SDK de Windows.
  
Un identificador de clase único (CLSID) identifica cada servidor de formularios. Siempre hay una asignación uno a uno entre un identificador de clase y su clase de mensaje. Sin embargo, esto no significa que un servidor de formularios solo pueda trabajar con mensajes de una clase de mensaje. Si no hay ningún servidor de formularios disponible para atender un mensaje de una clase en particular, el administrador de formularios que se use debe intentar encontrar un servidor de formularios para una clase de mensaje superior en la jerarquía de clases de mensaje; el administrador de formularios predeterminado que se proporciona con el SDK de Windows hace esto. Es probable que dicho servidor de formularios pueda representar sólo un subconjunto de las propiedades del mensaje (las que admite la superclase), pero será mejor que nada. Lo que sucede cuando no se encuentra ningún servidor de formularios que coincida es un detalle de implementación específico del administrador de formularios que se usa; el administrador de formularios predeterminado no abre los mensajes cuando esto ocurre.
  
Para obtener más información, consulte [clases de mensajes MAPI](mapi-message-classes.md).
  
## <a name="see-also"></a>Vea también



[Formularios MAPI](mapi-forms.md)

