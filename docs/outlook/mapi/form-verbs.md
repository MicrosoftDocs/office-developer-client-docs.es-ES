---
title: Verbos de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 27999c141fdeb3e1610213db128bc4ad3d049e6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594106"
---
# <a name="form-verbs"></a>Verbos de formulario

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Normalmente, la interfaz de usuario de un formulario ofrece los elementos de menú o los controles que permiten a los usuarios realizar algún tipo de acción con el formulario. Es del servidor formulario para controlar las acciones del usuario. Esta interfaz se implementa mediante las API de Win32 estándar; escribir uno es igual que escribir otras interfaces de programas de Win32 normales.
  
A menudo, las acciones del usuario se asocian con los verbos. Un verbo es el nombre de una acción que es específico de una determinada clase de mensaje. Por ejemplo, la **respuesta** es un verbo que se implementa mediante muchos servidores de formulario, cada uno de los cuales puede tener una interpretación diferente de ese verbo. A veces se hace referencia a verbos como comandos. 
  
> [!NOTE]
> No todos los elementos de menú y controles de un formulario se corresponden con un verbo. Por ejemplo, un botón **Cancelar** no corresponde a un verbo Cancelar dentro del servidor de formulario. Normalmente, los verbos están asociados con las acciones que son específicas de una clase de mensaje concreto o un conjunto de clases de mensajes. Aunque las clases de mensajes diferentes pueden admitir distintos conjuntos de verbos, todos admiten al menos el verbo Open, que muestra la interfaz de usuario del formulario y carga con valores de propiedad del mensaje. 
  
Los verbos no pueden tardar parámetros. Los formularios que exportación comandos con parámetros variables deben utilizar los mecanismos de automatización.
  
Los clientes pueden determinar qué verbos son compatibles con una clase de mensaje en particular a través del método [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) , que se implementa mediante el Administrador de formularios de MAPI. El Administrador de formulario obtiene esta información desde el archivo de configuración del formulario. El conjunto de verbos devueltos por este método se usa en el cliente para mostrar al usuario los comandos que se pueden ejecutar en un mensaje. Por ejemplo, un cliente es posible que permiten a los usuarios haga clic en el botón secundario del mouse a través de un mensaje para mostrar los verbos aplicables a ese mensaje. 
  
## <a name="see-also"></a>Recursos adicionales

- [Formularios MAPI](mapi-forms.md)

