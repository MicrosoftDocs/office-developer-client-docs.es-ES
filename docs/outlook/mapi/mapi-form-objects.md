---
title: Objetos de formulario MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 426d3d5787f4ef8cde2883c5e2eb3699dd664965
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818127"
---
# <a name="mapi-form-objects"></a>Objetos de formulario MAPI

  
  
**Hace referencia a**: Outlook 
  
Objetos de formulario se crean dinámicamente por los servidores de formulario a fin de mostrar mensajes específicos y permitir a los usuarios interactuar con ellos. Un objeto de formulario es, por lo tanto, una creación de instancias de la clase derivada de [IMAPIForm](imapiformiunknown.md) que se implementa mediante el servidor de formulario. Cuando una aplicación cliente abre un mensaje, el servidor de formulario para esa clase de mensaje crea un objeto de formulario para controlar el mensaje. A continuación, el objeto de formulario crea su interfaz y muestra las propiedades del mensaje en él. El objeto de formulario y su interfaz continúa hasta que el usuario lo cierre. El objeto de formulario controla los cambios realizados en los valores de las propiedades del mensaje. 
  
Además, las interfaces de formulario MAPI definen un mecanismo por el que puede cargar y mostrar una serie de mensajes de un objeto de formulario. Esto es un mecanismo de eficacia, ya que evita destrucción innecesaria y la creación de objetos de mensaje y sus interfaces. Cuando lo solicita el cliente de mensajería para cargar un mensaje distinto, el objeto de formulario debe guardar los cambios a las propiedades del mensaje actual.
  
Para obtener información sobre la perspectiva de la aplicación cliente de objetos de formulario, vea [Objetos de formulario personalizada de MAPI](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Vea también



[Formularios MAPI](mapi-forms.md)

