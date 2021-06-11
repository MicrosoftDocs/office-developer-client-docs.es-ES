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
  
Los servidores de formulario crean dinámicamente objetos de formulario para mostrar mensajes específicos y permitir a los usuarios interactuar con ellos. Por lo tanto, un objeto de formulario es una instancia de la clase derivada de [IMAPIForm](imapiformiunknown.md) que implementa el servidor de formularios. Cuando una aplicación cliente abre un mensaje, el servidor de formulario de esa clase de mensaje crea un objeto de formulario para controlar el mensaje. A continuación, el objeto form crea su interfaz y muestra las propiedades del mensaje en ella. El objeto de formulario y su interfaz persisten hasta que el usuario lo cierra. El objeto form controla los cambios realizados en los valores de las propiedades del mensaje. 
  
Además, las interfaces de formulario MAPI definen un mecanismo mediante el cual un objeto de formulario puede cargar y mostrar una serie de mensajes. Se trata de un mecanismo de eficiencia, ya que evita la destrucción y la creación de objetos de mensaje y sus interfaces. Cuando el cliente de mensajería lo solicite para cargar un mensaje diferente, el objeto de formulario debe guardar cualquier cambio en las propiedades del mensaje actual.
  
Para obtener información sobre la perspectiva de objetos de formulario de una aplicación cliente, vea [Objetos de formulario personalizados MAPI](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Vea también



[Formularios MAPI](mapi-forms.md)

