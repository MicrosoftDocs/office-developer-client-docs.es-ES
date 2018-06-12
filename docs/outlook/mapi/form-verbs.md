---
title: Verbos de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 1ecc80feec2b0a86f35d03f1ca4f75ea9ff094e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816854"
---
# <a name="form-verbs"></a>Verbos de formulario

**Se aplica a**: Outlook 
  
Normalmente, la interfaz de usuario de un formulario ofrece los elementos de menú o los controles que permiten a los usuarios realizar algún tipo de acción con el formulario. Es del servidor formulario para controlar las acciones del usuario. Esta interfaz se implementa mediante las API de Win32 estándar; escribir uno es igual que escribir otras interfaces de programas de Win32 normales.
  
A menudo, las acciones del usuario se asocian con los verbos. Un verbo es el nombre de una acción que es específico de una determinada clase de mensaje. Por ejemplo, la **respuesta** es un verbo que se implementa mediante muchos servidores de formulario, cada uno de los cuales puede tener una interpretación diferente de ese verbo. A veces se hace referencia a verbos como comandos. 
  
> [!NOTE]
> No todos los elementos de menú y controles de un formulario se corresponden con un verbo. Por ejemplo, un botón **Cancelar** no corresponde a un verbo Cancelar dentro del servidor de formulario. Normalmente, los verbos están asociados con las acciones que son específicas de una clase de mensaje concreto o un conjunto de clases de mensajes. Aunque las clases de mensajes diferentes pueden admitir distintos conjuntos de verbos, todos admiten al menos el verbo Open, que muestra la interfaz de usuario del formulario y carga con valores de propiedad del mensaje. 
  
Los verbos no pueden tardar parámetros. Los formularios que exportación comandos con parámetros variables deben utilizar los mecanismos de automatización.
  
Los clientes pueden determinar qué verbos son compatibles con una clase de mensaje en particular a través del método [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) , que se implementa mediante el Administrador de formularios de MAPI. El Administrador de formulario obtiene esta información desde el archivo de configuración del formulario. El conjunto de verbos devueltos por este método se usa en el cliente para mostrar al usuario los comandos que se pueden ejecutar en un mensaje. Por ejemplo, un cliente es posible que permiten a los usuarios haga clic en el botón secundario del mouse a través de un mensaje para mostrar los verbos aplicables a ese mensaje. 
  
## <a name="see-also"></a>Ver también

- [Formularios MAPI](mapi-forms.md)

