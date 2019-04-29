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
ms.openlocfilehash: 5a7c6c575f277a91a18f0d834e26d3d376613fba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404788"
---
# <a name="mapi-form-objects"></a>Objetos de formulario MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los servidores de formularios crean dinámicamente los objetos de formulario para mostrar mensajes específicos y permitir que los usuarios interactúen con ellos. Por lo tanto, un objeto Form es una instancia de la clase derivada de [IMAPIForm](imapiformiunknown.md) que se implementa en el servidor de formularios. Cuando una aplicación cliente abre un mensaje, el servidor de formularios para esa clase de mensaje crea un objeto de formulario para controlar el mensaje. A continuación, el objeto de formulario crea su interfaz y muestra las propiedades del mensaje en él. El objeto de formulario y su interfaz se conservan hasta que el usuario lo cierra. El objeto Form controla los cambios en los valores de las propiedades del mensaje. 
  
Además, las interfaces de formulario MAPI definen un mecanismo por el que un objeto Form puede cargar y mostrar una serie de mensajes. Se trata de un mecanismo de eficacia, ya que evita tener que destruir y crear objetos de mensaje y sus interfaces. Cuando el cliente de mensajería solicita que cargue un mensaje diferente, el objeto de formulario debe guardar los cambios en las propiedades del mensaje actual.
  
Para obtener información sobre la perspectiva de la aplicación cliente de los objetos de formulario, consulte [objetos de formulario personalizado MAPI](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Ver también



[Formularios MAPI](mapi-forms.md)

